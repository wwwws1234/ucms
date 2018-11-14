#ucms
##1.1
Ucms version 1.47, download address http://uuu.la/

##1.2
After downloading, build your own local web environment.Create management admin password is 123456
![image](https://github.com/wwwws1234/ucms/blob/master/1.png)

##1.3
Login the background system with admin and add a background user test.
![image](https://github.com/wwwws1234/ucms/blob/master/2.png)


Use test account login background, password 654321
![image](https://github.com/wwwws1234/ucms/blob/master/3.png)


Using test user login to enter their personal information modification interface, test is a background user.
![image](https://github.com/wwwws1234/ucms/blob/master/4.png)



The input password is abab and debugged using Phpstorm.In the if of the mypost.php file, the breakpoint is seen, and we see the value we transmitted in cookie.
![image](https://github.com/wwwws1234/ucms/blob/master/5.png)
![image](https://github.com/wwwws1234/ucms/blob/master/6.png)

Now we change the test to admin, and continue to follow up.
![image](https://github.com/wwwws1234/ucms/blob/master/7.png)
![image](https://github.com/wwwws1234/ucms/blob/master/8.png)

Debugging to 15 lines of code, this place is the place to get the user name.

![image](https://github.com/wwwws1234/ucms/blob/master/9.png)
Follow up to 56 lines, find that 56 lines of code knowledge simply judge whether the value in cookie is set and not empty, and then directly assign the admin_cookiehash in cookie to username. It can be seen that this place is the cause of the vulnerability, without verifying the legitimacy of the user. Follow up

![image](https://github.com/wwwws1234/ucms/blob/master/10.png)
![image](https://github.com/wwwws1234/ucms/blob/master/11.png)


Found that the return value is admin. Continue to follow up.

