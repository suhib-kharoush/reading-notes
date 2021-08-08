# Dynamic Routes

- In this lesson, we’ll talk about the case where each page path depends on external data. Next.js allows you to statically generate pages with paths that depend on external data. This enables dynamic URLs in Next.js.

![](https://nextjs.org/static/images/learn/dynamic-routes/page-path-external-data.png)

##### How to Statically Generate Pages with Dynamic Routes
- In our case, we want to create dynamic routes for blog posts:

- - We want each post to have the path `/posts/<id>`, where `<id>` is the name of the markdown file under the top-level `posts` directory.
- - Since we have `ssg-ssr.md` and `pre-rendering.md`, we’d like the paths to be `/posts/ssg-ssr` and `/posts/pre-rendering`.

- In `pages/posts/[id].js`, we’ll write code that will render a post page — just like other pages we’ve created.
```
import Layout from '../../components/layout'

export default function Post() {
  return <Layout>...</Layout>
}
```

- Now, here’s what’s new: We’ll export an async function called `getStaticPaths` from this page. In this function, we need to return a list of possible values for `id`.
```
import Layout from '../../components/layout'

export default function Post() {
  return <Layout>...</Layout>
}

export async function getStaticPaths() {
  // Return a list of possible value for id
}
```

- Finally, we need to implement `getStaticProps` again - this time, to fetch necessary data for the blog post with a given `id`. `getStaticProps` is given `params`, which contains `id` (because the file name is `[id].js`).
```
import Layout from '../../components/layout'

export default function Post() {
  return <Layout>...</Layout>
}

export async function getStaticPaths() {
  // Return a list of possible value for id
}

export async function getStaticProps({ params }) {
  // Fetch necessary data for the blog post using params.id
}
```

##### Implement getStaticPaths

- - Create a file called `[id].js` inside the `pages/posts` directory.
- - Also, remove `first-post.js` inside the `pages/posts` directory — we’ll no longer use this.

##### Implement getStaticProps
- We need to fetch necessary data to render the post with the given `id`.

- To do so, open `lib/posts.js` again and add the following `getPostData` function at the bottom. It will return the post data based on `id`:
```
export function getPostData(id) {
  const fullPath = path.join(postsDirectory, `${id}.md`)
  const fileContents = fs.readFileSync(fullPath, 'utf8')

  // Use gray-matter to parse the post metadata section
  const matterResult = matter(fileContents)

  // Combine the data with the id
  return {
    id,
    ...matterResult.data
  }
}
```

##### Render Markdown
- To render markdown content, we’ll use the `remark` library. First, let’s install it:
``npm install remark remark-html``

- Then, open `lib/posts.js` and add the following imports to the top of the file:
```
import remark from 'remark'
import html from 'remark-html'
```
- And update the `getPostData()` function in the same file as follows to use `remark`:
```
export async function getPostData(id) {
  const fullPath = path.join(postsDirectory, `${id}.md`)
  const fileContents = fs.readFileSync(fullPath, 'utf8')

  // Use gray-matter to parse the post metadata section
  const matterResult = matter(fileContents)

  // Use remark to convert markdown into HTML string
  const processedContent = await remark()
    .use(html)
    .process(matterResult.content)
  const contentHtml = processedContent.toString()

  // Combine the data with the id and contentHtml
  return {
    id,
    contentHtml,
    ...matterResult.data
  }
}
```


# Deploying Your Next.js App

##### Deploy to Vercel
- The easiest way to deploy Next.js to production is to use the Vercel platform developed by the creators of Next.js.

##### Create a Vercel Account
- First, go to https://vercel.com/signup to create a Vercel account. Choose Continue with GitHub and go through the sign up process.

##### Next.js and Vercel
- Vercel is made by the creators of Next.js and has first-class support for Next.js. When you deploy your Next.js app to Vercel, the following happens by default:
- - Pages that use Static Generation and assets (JS, CSS, images, fonts, etc) will automatically be served from the Vercel Edge Network, which is blazingly fast.
- - Pages that use Server-Side Rendering and API routes will automatically become isolated Serverless Functions. This allows page rendering and API requests to scale infinitely.