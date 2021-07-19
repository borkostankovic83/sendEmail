# Send Email With Spring Boot
Send Email with Spring using username and password

Make sure less secure App is enabled for your E-mail id that you are going to use.To enable less secure App Click here https://myaccount.google.com/lesssecureapps !
Also Two-step verification should not be enabled for you E-mail Id.

**spring-boot-starter-mail**  is the important dependency that contains all the Java Mail Classes.

implementation 'org.springframework.boot:spring-boot-starter-mail'

**User.java**

This class contains E-mail id of the user on which mail is to be send.

**MailService.java**

This class contains two function sendEmail() and sendEmailWithAttachment().

Actually ,Java provides a two classes for sending mail.If you want to send simple mail without attachment then object of SimpleMailMessage is used otherwise an Object of MimeMessage is used.

_**ClassPathResource Class**_ is used to attach a file to the Java Program. Make sure you add an attachment file to src ->resources. That file will be sent as an attachment to the respective e-mail id.

**RegistrationController.java**

This controller class contains an API for sending mail. First API is developed for sending mail without attachment and the second API is for sending mail along with the attachment.

Make sure you write E-mail ID of the receiver in user.setEmailAddress(“your_email_id”); . I have written my email id above for an instance.

**The APIs are accessible at URL :**

For Simple Mail without attachment.

http://localhost:8080/send-mail

For Mail that contains an attachment.

http://localhost:8080/send-mail-attachment