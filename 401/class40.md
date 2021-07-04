# Dynamic Routes

## Download Starter Code (Optional)

        npx create-next-app nextjs-blog --use-npm --example "https://github.com/vercel/next-learn-starter/tree/master/dynamic-routes-starter"

### You should also update the following files:

- `public/images/profile.jpg` with your photo (Recommended: 400px width/height).
- `const name = '[Your Name]'` in components/layout.js with your name.
- `<p>[Your Self Introduction]</p>` in pages/index.js with your self introduction.

## Page Path Depends on External Data

### How to Statically Generate Pages with Dynamic Routes

- We want each post to have the path /posts/<id>, where <id> is the name of the markdown file under the top-level posts directory.
- Since we have ssg-ssr.md and pre-rendering.md, we’d like the paths to be /posts/ssg-ssr and /posts/pre-rendering.

## Implement getStaticPaths

 we'll import the getAllPostIds function and use it inside getStaticPaths.

        import { getAllPostIds } from '../../lib/posts'

        export async function getStaticPaths() {
        const paths = getAllPostIds()
        return {
            paths,
            fallback: false
        }
        }


## Render Markdown

- To render markdown content, we’ll use the remark library. First, let’s install it:

        npm install remark remark-html

- Then, open lib/posts.js and add the following imports to the top of the file:

        import remark from 'remark'
        import html from 'remark-html'

- And update the getPostData() function in the same file as follows to use remark:

## Polishing the Post Page

- Adding title to the Post Page

In pages/posts/[id].js, let’s add the title tag using the post data. You'll need to add an import for next/head at the top of the file and add the title tag by updating the Post component.

- Formatting the Date

To format the date, we’ll use the date-fns library. First, install it:

        npm install date-fns    

- Adding CSS

Finally, let’s add some CSS using the file styles/utils.module.css we added before. Open pages/posts/[id].js, then add an import for the CSS file, and replace the Post component with the following code:

        // Add this import at the top of the file
        import utilStyles from '../../styles/utils.module.css'
        export default function Post({ postData }) {
    return (
        <Layout>
        <Head>
            <title>{postData.title}</title>
        </Head>
        <article>
            <h1 className={utilStyles.headingXl}>{postData.title}</h1>
            <div className={utilStyles.lightText}>
            <Date dateString={postData.date} />
            </div>
            <div dangerouslySetInnerHTML={{ __html: postData.contentHtml }} />
        </article>
        </Layout>
        )
    }



# Deploying Your Next.js App

1. Push to GitHub

        git remote add origin https://github.com/<username>/nextjs-blog.git
        git push -u origin main

2. Deploy to Vercel

    - import your project 

    - Vercel automatically detects that you have a Next.js app and chooses optimal build settings for you.

    1. Project Name
    2. Root Directory
    3. Build Command
    4. Output Directory
    5. Development Command

    - When it’s done, you’ll get deployment URLs.