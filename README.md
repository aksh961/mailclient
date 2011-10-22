During the summer term 2007 we had the task to create a Thunderbird like **mailclient**
in Java. This here is the collection of my code.



## Installation for Netbeans ##

- just get the [source from github](url "zip from github") and extract it
- also extract the *javamail-1.4.zip* => this package contains a Java library for handling emails
- create a new project under NetBeans and copy all files of the *Mail Client* directory in the *src*
  directory of you NetBeans project
- then you have to insert the *mail.jar* file in your project in the following way:
    - click right on Libraries in the near of the view of your NetBeans project and chose *Add JAR*
    - navigate to *javamail-1.4* folder and select the *mail.jar*
    - when you now select the files *GUIMailsend.java* and *GUIMailsget.java* should not show any
      errors
- now you have to adopt the paths in the file *GUIMain.java* `(static File f, String dir, FileReader
  file)` and *GUITree* `(File driveC, File source, File ziel)` to your NetBeans project folder
  through absolute paths => I know it's cumbersome but due to this date I couldn't do any other
- set the *GuiMain.java* as the main file in your project and start the program
- the standard account is *MG kontoinfos.kondat* which contains the necessary data to access my
  spam account (you can guess how to change the data)
- the directory *Inbox MG* saves all read mails of the user MG, further accounts have to be created
  each in an own directory
- *MailApi.java* is not necessary for the mailclient, this will just be used to check the
  correctness of the POP3 settings via the terminal
- main cause of error messages:
    - wrong paths to your project
    - POP3 and SMTP
    - *mail.jar* is not included correct in the project, but this will be shown in NetBeans