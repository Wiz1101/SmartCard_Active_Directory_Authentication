# Guide for a SmartCard User Logon in AD (Active Directory)

**This writeup guides you how to configure Windows server authentication with a SmardCard**
<p align="center">
  <img src="pics/smartcard.jpeg" />
</p>


## Step 1. Create a user in AD [1]
![step 1](pics/createUser1.png)
![step 1](pics/createUser2.png)
![step 1](pics/createUser3.png)

## Step 2. Manage certificates for SmartCard user
![step 2](pics/pic1.png)
![step 2](pics/pic2.png)

Choose the name for the template certificate
![step 2](pics/pic3.png)
![step 2](pics/pic4.png)

Give, Read/Write/Enroll permissions to both Authenticated and Administrators users
![step 2](pics/pic5.png)
![step 2](pics/pic6.png)

Finally configure Issuance Requirements
![step 2](pics/pic7.png)

## Step 3. Enable Enrollment Agent certificate and Smartcard user certificate you duplicated
![step 3](pics/pic8.png)
![step 3](pics/pic9.png)
![step 3](pics/pic10.png)
![step 3](pics/pic11.png)
![step 3](pics/pic12.png)


## Step 4. Add Enrollment Agent certificate in personal certificates 
First You have to open a certification manager utility by typing certmgr.msc in RUN and then you can request a new certificate
![step 4](pics/CertificateEnrollment/pic1.png)

Enroll "Enrollment agent" certificate
![step 4](pics/CertificateEnrollment/pic2.png)

Final result
![step 4](pics/CertificateEnrollment/pic3.png)

## Step 5. Enroll a certificate for a SmartCard user [1]. 
![step 5](pics/CertificateEnrollment/pic4.png)

Click Next
![step 5](pics/CertificateEnrollment/pic5.png)

Click Next
![step 5](pics/CertificateEnrollment/pic6.png)

Click Browse and accept certificate for Certificate Request Agent
![step 5](pics/CertificateEnrollment/pic7.png)

Click Next
![step 5](pics/CertificateEnrollment/pic8.png)

Select the SmartCard user duplicate certificate you created and click Next
![step 5](pics/CertificateEnrollment/pic9.png)

Select the test user you created for the certificate and click Enroll
![step 5](pics/CertificateEnrollment/pic10.png)

Connect your SmartCard
![step 5](pics/CertificateEnrollment/pic11.png)

Enter your SmartCard PIN, which should be 0000 by default
![step 5](pics/CertificateEnrollment/pic12.png)

Finally, Once you are logged in, you can change the SmartCard PIN by hitting ctlr+alt+delete and then changing a password ( Special thanks to https://github.com/th3Hellion )
![step 5](pics/CertificateEnrollment/pic13.png)

**THE END!**

## References

1. https://www.youtube.com/watch?v=zuOnoM6kfZY&t=1s&ab_channel=Tech%26ComputerStuff
