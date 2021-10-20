## Welcome to SQLiteDevStudio

[Privacy Policy](PrivacyPolicy.md)

SQLiteDevStudio is a front end SQLite Database development and maintenance tool for Android. It has been primarily developed for developers to create databases specific to their own application needs which can then be exported into their own projects.

It can also be used to simply view and edit data. This is particuarly useful when wishing to see the current state of data during the testing phase of application development.

SQLiteDevStudio can access databases from a number of locations on a given device:
- **SQLiteDevStudio internal directory structure:** Datbases can be created and modified within SQLiteDevStudio's internal storage. Once complete can be exported to anothe project in the form of a DBHelper.java file.
- **External Shared Storage:** A database that is located in a devices shared storage can be imported into SQLiteDevStudio's internal storage where it can be viewed and edited. To push any changes made to the external version of the database a database restore will need to be done.
- **Access via Content Provider:** Another option when you are developing your own app is to include a content provider to allow SQLiteDevStudio to access the database(s) within your app's internal storage. The required content provider can be found [here](http://github.com/jonnybateman/SQLiteContentProvider.git) along with instructions on how to apply it. Since a content provider could allow apps other than SQLiteDevStudio to access your database a level of security has been added to the provider. Only database requests submitted to the content provider with the correct provider access code will be granted. On completion of your project and prior to release the content provider should be removed or the associated 'exported' variable in the manifest file set to false.
