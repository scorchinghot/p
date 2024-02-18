Project Name: Travel UI UX Landing Page

Description: This landing page is designed for a travel website, emphasizing speed, responsiveness, and a clean, beautiful UI/UX.

Tech Stack: TypeScript, Next.js, Tailwind CSS

Installation: First, I created a new folder for this Travel UI UX Landing Page project. Using the command line, then navigated to this folder and ran npx create-next-app@latest ./ to set up our project with TypeScript and Tailwind CSS. Once installed, I started the development server with npm run dev to begin working on our project locally. Finally for deployment, I used npm run build to generate optimized files ready for hosting on any server.

Project Structure: The project revolves around four primary directories: app, components, constants, and public. The layout.js (or Main.js) file within app serves as the backbone, providing the overall HTML structure for the website. The pages.tsx file, located in app, represents the homepage and defines its layout. Components housed in the components directory contribute to various parts of the webpage. Data used throughout the project is stored in constants, while static assets reside in public. This structured organization facilitates seamless connectivity and simplifies maintenance.

Usage: This webpage serves as a landing page for a travel website, focusing on UI/UX design and responsiveness. It does not include full-stack functionality. The project aimed to learn the fundamentals of Next.js, Tailwind CSS, TypeScript, UI/UX design, and landing page development.

Key Features: The webpage boasts a clean UI/UX design and excellent responsiveness across different devices.

Lesson Learned: The project facilitated learning various best practices, including implementing media queries for different device sizes, using Next.js's Link and Image components for optimized images and links, and leveraging the .map method for component-based rendering.

Credits: Special thanks to JavaScript Mastery for their invaluable courses that provided hands-on experience with real-world projects. You can find their tutorials and more on their YouTube channel: https://youtube.com/@javascriptmastery?si=lxy1L3qu9xzbPKSv

Code Snippets:

export default function RootLayout({children,}: Readonly<{children: React.ReactNode;}>) {return (<html lang="en"><body><Navbar /><main className="relative overflow-hidden">{children}</main><Footer /></body></html>);}

RootLayout Component: This component serves as a layout wrapper for the entire application. It encapsulates common layout elements such as the Navbar and Footer. The children prop represents the content to be rendered within the layout, like other components or pages.

export default function Home() {return (<><Hero /><Camp /> <Guide /><Features /><GetApp /></>);}

The Home function is exported as the default export. This function serves as the entry point for the home page.

type ButtonProps = {type: 'button' | 'submit';title: string;icon?: string;variant: string;full?: boolean;}

This section defines a TypeScript type ButtonProps, specifying the expected props for the Button component. It ensures type safety and provides clear documentation for the props that the Button component accepts.

<ul className="hidden h-full gap-12 lg:flex">{NAV_LINKS.map((link) => (<Link href={link.href} key={link.key}className="regular-16 text-gray-50 flexCenter cursor-pointer pb-1.5 transition-all hover:font-bold">{link.label}</Link>))}</ul>

The navbar consists of elements such as a logo (Image wrapped in a Link), navigation links (Link elements mapped from NAV_LINKS), a login button (Button), and a menu icon (Image). The navigation links are generated dynamically using the NAV_LINKS constant. Each link is wrapped in a Link component and styled accordingly.

{Array(5).fill(1).map((_, index) => (<Image src="/star.svg"key={index} alt="star"width={24}height={24}/>))}

This snippet showcases dynamic rendering of star icons based on an array's length. By using the map method on an array filled with a placeholder value, it generates a variable number of star icons. This approach allows for flexible and dynamic rendering of content, useful for cases where the content may vary dynamically.
