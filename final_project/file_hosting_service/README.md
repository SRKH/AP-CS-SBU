# File Hosting Service

## Introduction

A **file hosting service, cloud storage service, online file storage provider**, or **cyberlocker** is an internet hosting service specifically designed to host user files. It allows users to upload files that could be accessed over the internet after a user name and password or another authentication is provided. Typically, the services allow HTTP access, and sometimes FTP access. 
Related services are content-displaying hosting services (i.e., video and image), virtual storage, and remote backup.

## Component 

### Client

1. Your app must be able to monitor user-defined folders for change and send changed files to the server .
2. Your app must provide a way to list and load data (files & folders) from the server to the client *.
3. Your app must provide a way to authenticate users*.
4. User should be able to add a comment for their files*
5. (extra point) User should be able to share files*
6. (extra point) your app should provide a content version manager for the text files and show changes in text file versions* 

 * : **User interface required**

#### notes: 
- You are free to use JavaFX
- You are free to use any protocol or way to send the file to your server
- A user interface that is visually more beautiful has an extra point

#### hints:

- https://docs.oracle.com/javase/tutorial/essential/io/notification.html
- https://youtu.be/siVt2sSsSNc
- https://examples.javacodegeeks.com/desktop-java/swing/java-swing-form-example/

