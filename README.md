## Welcome to SQLiteDevStudio

### Overview

[Privacy Policy](PrivacyPolicy.md)

SQLiteDevStudio is a front end SQLite Database development and maintenance tool for Android. It has been primarily developed for developers to create databases specific to their own application needs which can then be exported into their own projects.

It can also be used to simply view and edit data. This is particuarly useful when wishing to see the current state of data during the testing phase of application development.

SQLiteDevStudio can access databases from a number of locations on a given device:
- **SQLiteDevStudio Internal Storage:** Datbases can be created and modified within SQLiteDevStudio's internal storage. Once complete can be exported to anothe project in the form of a DBHelper.java file.
- **External Shared Storage:** A database that is located in a devices shared storage can be imported into SQLiteDevStudio's internal storage where it can be viewed and edited. To push any changes made to the external version of the database a database restore will need to be done.
- **Access via Content Provider:** Another option when you are developing your own app is to include a content provider to allow SQLiteDevStudio to access the database(s) within your app's internal storage. The required content provider can be found [here](http://github.com/jonnybateman/SQLiteContentProvider.git) along with instructions on how to apply it. Since a content provider could allow apps other than SQLiteDevStudio to access your database a level of security has been added to the provider. Only database requests submitted to the content provider with the correct provider access code will be granted. On completion of your project and prior to release the content provider should be removed or the associated 'exported' variable in the manifest file set to false.
- **Third-Party App Internal Storage:** To access databases of third-party apps the device needs to be rooted. If this is the case then the databases can be accessed, viewed, and modified directly. SQLiteDevStudio has a built in file explorer for navigating to the required database.

After install a user account needs to be set up to access the application. User will be prompted for an email address. This is used only in the event that the user has forgotten their password. Password will be sent to the email address that was used during account setup. Email address is encrypted and only stored locally on the device. It is not shared amongst any other parties.

### Functionality

SQLiteDevStudio has the following functionality:
- Create/Delete database
- Open exisiting databases
- Restore external database
- Export database (exported as a DBHelper .java file for applying to your own projects, note: data not exported)
- Write and execute your own SQL statements with the built in editor
- SQL keywords/data types/functions/etc are highlighted within the editor
- Previously executed statements can be re-called through the SQL History dialog
- View, update, delete, and insert data
- View existing foreign keys
- Enable/Disable foreign key constraints
- Limit number of rows returned
- Sort the rows returned
- Describe table
- Create, alter, and drop tables
- Create and drop triggers
- Display database indexes
- Create and drop indexes
- Extract the SQL for database objects and display code in the SQL Editor
- Import table data in the form of a CSV file
- Export table data to a CSV file
