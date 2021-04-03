# EJS:

- When creating quick on-the-fly Node applications, an easy and fast way to template our application is sometimes necessary.

- Jade comes as the view engine for Express by default but Jade syntax can be overly complex for many use cases. EJS is one alternative does that job well and is very easy to set up.

- To setup node:
- we have to check in our package.json file, it will have ejs and express.
- Then do npm install

- Create the EJS Partials:
- Like a lot of the applications we build, there will be a lot of code that is reused. We’ll call those partials and define three files we’ll use across all of our site: head.ejs, header.ejs, and footer.ejs.

- Conclusion:
- EJS lets us spin up quick applications when we don’t need anything too complex. By using partials and having the ability to easily pass variables to our views, we can build some great applications quickly.
