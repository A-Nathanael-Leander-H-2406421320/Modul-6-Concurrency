# Modul-6-Concurrency

## Commit 1 Reflection notes

In this commit, I have implemented the basic structure of the project. For now, the app only prints the HTTP request to the console. The main focus of this commit was to establish a solid foundation for the development of the concurrency features in the upcoming commits. I am looking forward to implementing the actual concurrency mechanisms and seeing how they improve the performance and efficiency of this application. I need to familiarize myself with Rust more because this language has many unique features that will be useful in future.

## Commit 2 Reflection notes

![Commit 2 screen capture](/assets/images/commit2.png)

In this commit, I have made the web server actually display something in the browser. I have implemented a simple HTTP response that includes a status line, content length header, and the contents of an HTML file. As with knowledge gained from PBP course, i also styled the HTML page with Bootstrap. This is a significant step forward as it allows us to see the results of our work in a web browser, making it easier to test and debug our application. I am excited to continue building on this foundation and adding more features in the future commits.

## Commit 3 Reflection notes

![Commit 3 screen capture](/assets/images/commit3.png)

In this commit, I have implemented a simple Error 404 implementation. Now, if the user tries to access a page that does not exist, they will be presented with a user-friendly error message instead of a blank page or a generic browser error. To split between the 200 OK and 404 NOT FOUND responses, I have added a simple conditional statement that checks the request line and serves the appropriate HTML file based on the requested URL. [The tutorial](https://rust-book.cs.brown.edu/ch21-01-single-threaded.html#a-touch-of-refactoring) suggests using refactoring to minimize repetitive code and make the code more maintainable, so I followed that. This made use of a powerful Rust feature which you can use if-else block during variable initialization, something I familiar to do in Python but not in other languages such as Java because the lack of that feature. This is a great example of how Rust's unique features can help us write cleaner and more efficient code.

## Commit 4 Reflection notes

The slow network connection simulation via `/sleep` is a great example to show us how necessary concurrency and multithreading is in web servers. As we can see, when a thread is sleeping, it blocks the entire server, preventing it from handling any other incoming requests. This means that if multiple clients try to access the server while one thread is sleeping, they will all be blocked until the sleeping thread finishes its task. This can lead to a poor user experience and can significantly degrade the performance of the server.

## Commit 4 Reflection notes

In this commit, I have implemented a simple thread pool to handle incoming requests concurrently. A thread pool is a collection of pre-spawned threads ("worker threads") that can be reused to execute tasks. By using a thread pool, we can avoid the overhead of creating a new thread for each incoming request, which can improve the performance and scalability of our web server. With the thread pool in place, our server can now handle multiple requests simultaneously, even when one of the threads is sleeping. This allows us to provide a better user experience and ensures that our server remains responsive under heavy load.