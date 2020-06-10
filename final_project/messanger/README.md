# Messanger

You should implement a messenger with 
private chat, group chat, and channels
Your app should support file sharing


## Component

## Client 

1. Your app must provide a way to authenticate users*
2. Your app must be able to show the user's status (online/offline)*
3. Your app must be able to send messages in text or file*
4. Your app must provide a way to create new groups and channels*
5. (extra point) your app must be able to sort chats by their last activity*
6. (extra point) your app must be able to show images in the user interface
7. (extra point) your app must provide multi administrator for channels

  * : **User interface required**
  
### Notes
- You are free to use JavaFX
- You are free to use any protocol or way to send the file to your server
- A user interface that is visually more beautiful has an extra point

### Hints
- https://winterbe.com/posts/2014/07/31/java8-stream-tutorial-examples/
- https://www.youtube.com/watch?v=TVj5mR3flO8
- https://www.youtube.com/watch?v=BErFK2DkaPw


## Server 

1. Your server must support multi-user simultaneously (Multi-Thread Server)
2. Your server must provide a way to authenticate users
3. Your server must save user information, data, and messages
4. Your server must monitor your socket status and set the offline or online flag for user
5. (extra point) Encrypting user data
6. (extra point) Using SQL databases
7. (extra point) Using Elastic Search for storing messages point (NoSQL)

### Note
- You are free to use libraries for your low-level components like: 
    - Database client library (JDBC)
    - JSON parser(GSON)
    - ...

### Hints
- https://www.codejava.net/coding/file-encryption-and-decryption-simple-example
- https://winterbe.com/posts/2014/07/31/java8-stream-tutorial-examples/


Good Luck
