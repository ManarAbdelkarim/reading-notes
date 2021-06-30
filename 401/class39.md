# Readings: React 3

## Assets
Next.js can serve static assets, like images, under the top-level public directory. Files inside public can be referenced from the root of the application similar to pages.

The public directory is also useful for robots.txt, Google Site Verification, and any other static assets. Check out the documentation for Static File Serving to learn more.

### Download Your Profile Picture:

- Download your profile picture in .jpg format (or use this file).
- Create an images directory inside of the public directory.
- Save the picture as profile.jpg in the public/images directory.
- The image size can be around 400px by 400px.
- You may remove the unused SVG logo file directly under the public directory.

### Using the Image Component:

        import Image from 'next/image'

        const YourComponent = () => (
        <Image
            src="/images/profile.jpg" // Route of the image file
            height={144} // Desired size with correct aspect ratio
            width={144} // Desired size with correct aspect ratio
            alt="Your Name"
        />
        )

## Metadata

        export default function FirstPost() {
        return (
            <>
            <Head>
                <title>First Post</title>
            </Head>
            <h1>First Post</h1>
            <h2>
                <Link href="/">
                <a>Back to home</a>
                </Link>
            </h2>
            </>
        )
        }

## CSS Styling

        <style jsx>{`
        …
        `}</style>


### Writing and Importing CSS:

Next.js has built-in support for CSS and Sass which allows you to import .css and .scss files.
Using popular CSS libraries like Tailwind CSS is also supported.