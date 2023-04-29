# learnNextJs-Blog

Creating a mini-blog to understand the workings of NextJs.
The doc below documents the steps I went through during the creation and learning process.

## Setup

Creating a basic env.

1. Created a Next.Js app using `create-next-app` command.
2. Command used - `npx create-next-app@latest nextjs-blog --use-npm --example "https://github.com/vercel/next-learn/tree/master/basics/learn-starter"`
3. Open/Enter the nextjs-blog directory with `cd nextjs-blog`.
4. Run the Web-App on localhost using `npm run dev`.
5. Visit your Web-App on `localhost:3000`.

## Basics

Learning the basics of the NextJS.

### Navigating Between Pages

1. You can create new routes and pages by adding files and folders in `pages` folder.
2. For Example. `pages/posts/first-post.js` will create new page at route `localhost:3000/posts/first-post`

### Link Component

1. `<Link>` component from `next/link` allows for client-side navigation and accepts props.
2. Simply import it to your jsx file using `import Link from 'next/link';`.
3. `<Link>` is quite similar to `<a>` tag.
4. The difference is that `<Link>` allow `client-side navigation`.
5. Which basically means that, it uses javascript to load/transition to next page.
6. This allow for transition without fully reloding the page, providing a seamless experience.
7. `<Link>` also helps in `code-splitting` and `prefetching`.

### Assets, Metadata, and CSS

#### Assets

1. You can store all your assets inside `public` folder which can be accessed from root directory.
2. NextJS provides `<Image>` component out-of-the-box that provides various features like:
   a.Ensuring your image is responsive on different screen sizes
   b.Optimizing your images with a third-party tool or library
   c.Only loading images when they enter the viewport.
3. Import `<Image>` from `next/image`.

#### Metadata

1. In case you need to edit the head of the document, like changing `title`, then you can use `<Head>` component from `next/head`.
2. NextJS also provides `<Script>` tag form `next/script` that allow to include external Javascript.
3. This `<Script>` tag provides options like `lazyOnLoad` and `OnLoad` that effciently load the script in background.

#### CSS

1. Components can be shared between pages. To create components, add you code to `components` directory in `root` dir.
2. CSS modules in nextJS can be used to locally scope CSS at component level. They automatically generate unique class names to avoid class name collision.
3. To use CSS modules just add `module.css` at end of the file name. Then import it your JSX file as `styles` or any name of your preference. To use classes prefix it with `styles.` or the name of your choice. eg. `styles.container`.
4. There is also feature for Global CSS. For this you have to create `pages/_app.jsx`.
5. `_app.jsx` is a top-level React component that wraps all pages and allows to keep state when navigating pages or add global styles. (YOU NEED TO RESTART SERVER AFTER ADDING \_app.jsx)
6. You can only import global css in \_app.jsx.
