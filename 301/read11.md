# EJS:

- When creating quick on-the-fly Node applications, an easy and fast way to template our application is sometimes necessary.

![](https://th.bing.com/th/id/OIP.rvovX0wgGXSXTYvIuv2FggHaHa?w=183&h=183&c=7&o=5&dpr=1.25&pid=1.7)

- Jade comes as the view engine for Express by default but Jade syntax can be overly complex for many use cases. EJS is one alternative does that job well and is very easy to set up.

- To setup node:
- we have to check in our package.json file, it will have ejs and express.
- Then do npm install

- Create the EJS Partials:
- Like a lot of the applications we build, there will be a lot of code that is reused. We’ll call those partials and define three files we’ll use across all of our site: head.ejs, header.ejs, and footer.ejs.

- Conclusion:
- EJS lets us spin up quick applications when we don’t need anything too complex. By using partials and having the ability to easily pass variables to our views, we can build some great applications quickly.

- # Using the API:
- 
#### Authorizing requests and identifying your application:
- Every request your application sends to the Books API needs to identify your application to Google. There are two ways to identify your application: using an OAuth 2.0 token (which also authorizes the request) and/or using the application's API key. Here's how to determine which of those options to use:

- If the request requires authorization (such as a request for an individual's private data), then the application must provide an OAuth 2.0 token with the request. The application may also provide the API key, but it doesn't have to.
If the request doesn't require authorization (such as a request for public data), then the application must provide either the API key or an OAuth 2.0 token, or both—whatever option is most convenient for you.


#### Working with volumes:

- q - Search for volumes that contain this text string. There are special keywords you can specify in the search terms to search in particular fields, such as:

 - intitle: Returns results where the text following this keyword is found in the title.
  - inauthor: Returns results where the text following this keyword is found in the author.
  - inpublisher: Returns results where the text following this keyword is found in the publisher.
  - subject: Returns results where the text following this keyword is listed in the category list of the volume.
  - isbn: Returns results where the text following this keyword is the ISBN number.
  - lccn: Returns results where the text following this keyword is the Library of Congress Control Number.
  - oclc: Returns results where the text following this keyword is the Online Computer Library Center number.

#### Filtering:

- We can use the filter parameter to restrict the returned results further by setting it the to one of the following values:

 - partial - Returns results where at least parts of the text are previewable.
 - full - Only returns results where all of the text is viewable.
 - free-ebooks - Only returns results that are free Google eBooks.
 - paid-ebooks - Only returns results that are Google eBooks with a price.
 - ebooks - Only returns results that are Google eBooks, paid or free. Examples of non-eBooks would be publisher content that is available in limited preview and not for sale, or magazines.