# Local storage for web application:
- local storage is one of areas where native client applications hve held an advantage over web applications.
- For native applications, the operating system typically provides an abstraction layer for storing and retrieving application-specific data like preferences or runtime state. These values may be stored in the registry, INI files, XML files, or some other place according to platform convention.

- There are three potentially dealbreaking downsides:
- 1. cookies are included with every HTTP request, thereby showing down our web application by needlessly transmitting the same data over and over.

- 2. Cookies are included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over SSL).

3. Cookies are limited to about 4 KB of data — enough to slow down your application (see above), but not enough to be terribly useful.

### Introduction HTML5 storage:
- what is HTML storage?
- it's a way for web pages to store named key or value paires locally withen the client web browser.

### Using HTML storage:
- HTML5 Storage is based on named key or value pairs. we store data based on a named key, then you can retrieve that data with the same key. The named key is a string. The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats.

### Reacking changes to the HTML5 storage area:
- If we want to keep track programmatically of when the storage area changes, we can trap the storage event. The storage event is fired on the window object whenever setItem(), removeItem(), or clear() is called and actually changes something.

