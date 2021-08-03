# Assets, Metadata, and CSS

- The second page we added currently does not have styling. Let's add some CSS to style the page.

- Next.js has built-in support for CSS and Sass. For this course, we will use CSS.

##### Assets

- Next.js can serve static assets, like images, under the top-level `public directory`. Files inside `public` can be referenced from the root of the application similar to `pages`.

- The `public` directory is also useful for `robots.txt`, Google Site Verification, and any other static assets.

##### Unoptimized Image

- With regular HTML, you would add your profile picture as follows:

- ```<img src="/images/profile.jpg" alt="Your Name" />```

##### Image Component and Image Optimization

- `next/image` is an extension of the HTML `<img>` element, evolved for the modern web.

- Next.js also has support for Image Optimization by default. This allows for resizing, optimizing, and serving images in modern formats like WebP when the browser supports it. This avoids shipping large images to devices with a smaller viewport. It also allows Next.js to automatically adopt future image formats and serve them to browsers that support those formats.

##### Using the Image Component

- Instead of optimizing images at build time, Next.js optimizes images on-demand, as users request them. Unlike static site generators and static-only solutions, your build times aren't increased, whether shipping 10 images or 10 million images.

- Here's an example using next/image to display our profile picture. The height and width props should be the desired rendering size, with an aspect ratio identical to the source image.
```
import Image from 'next/image'

const YourComponent = () => (
  <Image
    src="/images/profile.jpg" // Route of the image file
    height={144} // Desired size with correct aspect ratio
    width={144} // Desired size with correct aspect ratio
    alt="Your Name"
  />
)
```

# Metadata

- What if we wanted to modify the metadata of the page, such as the `<title>` HTML tag?

- `<title>` is part of the `<head>` HTML tag, so let's dive into how we can modify the `<head>` tag in a Next.js page.

- Open `pages/index.js` in your editor and find the following lines:

```
<Head>
  <title>Create Next App</title>
  <link rel="icon" href="/favicon.ico" />
</Head>
```


# CSS Styling

- Let’s talk about CSS styling.
- As we can see, our index page (http://localhost:3000) already has some styles. If you take a look at `pages/index.js`, we should see code like this:
```
<style jsx>{`
  …
`}</style>
```

- This page is using a library called styled-jsx. It’s a “CSS-in-JS” library — it lets us write CSS within a React component, and the CSS styles will be scoped (other components won’t be affected).

##### Layout Component

- First, Let’s create a Layout component which will be shared across all pages.

- - Create a top-level directory called `components`.
- - Inside `components`, create a file called `layout.js` with the following content:

```
export default function Layout({ children }) {
  return <div>{children}</div>
}
```

- Then, open `pages/posts/first-post.js`, add an import for the `Layout` component, and make it the outermost component:

```
import Head from 'next/head'
import Link from 'next/link'
import Layout from '../../components/layout'

export default function FirstPost() {
  return (
    <Layout>
      <Head>
        <title>First Post</title>
      </Head>
      <h1>First Post</h1>
      <h2>
        <Link href="/">
          <a>Back to home</a>
        </Link>
      </h2>
    </Layout>
  )
}
```

##### Global Styles

- CSS Modules are useful for component-level styles. But if you want some CSS to be loaded by every page, Next.js has support for that as well.
- To load global CSS files, create a file called `pages/_app.js` with the following content:

```
export default function App({ Component, pageProps }) {
  return <Component {...pageProps} />
}
```

- This `App` component is the top-level component which will be common across all the different pages. You can use this `App` component to keep state when navigating between pages, for example.

##### Restart the Development Server

- Important: You need to restart the development server when you add `pages/_app.js`. Press ``Ctrl + c`` to stop the server and run:
`npm run dev`


##### Polishing Layout

- Update `components/layout.module.css`

- First, open components/layout.module.css and replace its content with the following more polished styles for the layout and profile picture:
```
.container {
  max-width: 36rem;
  padding: 0 1rem;
  margin: 3rem auto 6rem;
}

.header {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.backToHome {
  margin: 3rem 0 0;
}
```

##### Styling Tips

- Using `classnames` library to toggle classes

- `classnames` is a simple library that lets you toggle class names easily. You can install it using `npm install classnames` or `yarn add classnames`.

- We can first write a CSS module (e.g. alert.module.css) like this:
```
.success {
  color: green;
}
.error {
  color: red;
}
```

- And use `classnames` like this:
```
import styles from './alert.module.css'
import cn from 'classnames'

export default function Alert({ children, type }) {
  return (
    <div
      className={cn({
        [styles.success]: type === 'success',
        [styles.error]: type === 'error'
      })}
    >
      {children}
    </div>
  )
}
```

