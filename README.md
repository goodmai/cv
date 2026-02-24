# React CV Application

This repository contains two variants of a React-based CV (Resume) application. The project is structured to be automatically recognized and deployed by Vercel for the Node.js variant, while also providing a simple, standalone CDN variant for quick sharing.

## Variant 1: Node.js Build (Recommended for Vercel / GitHub Pages)

This variant uses the modern frontend build tool **Vite**, along with React and Tailwind CSS. This setup allows platforms like Vercel to automatically build and deploy your site seamlessly.

### Prerequisites
- **Node.js**: Please ensure you have the latest version of Node.js installed (>= 22.0.0 is required).

### How to Run Locally
1. Clone the repository and navigate to the project root directory.
2. Install the dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm run dev
   ```
4. To create a production build:
   ```bash
   npm run build
   ```

### Vercel Deployment Guide
You don't need any manual configuration to deploy this to Vercel. 
When you import the repository, Vercel will automatically detect the `package.json`, install the necessary dependencies via `npm install`, and run the `npm run build` command (which compiles your application into the `dist` folder using Vite). The application will then be live without any extra steps.

---

## Variant 2: CDN Version (No Build Required, Single File)

The **`index-cdn.html`** file contains a fully monolithic version of your application.
In this file, everything works directly within the browser using CDNs (Content Delivery Networks).

### How to Use
1. Simply open the `index-cdn.html` file in any modern web browser.
2. No Node.js or npm installation is required.

**How it works:**
* **Babel Standalone** is included via a `<script>` tag to compile JSX and modern JavaScript features directly in the browser on the fly.
* **React** and **Lucide-react** libraries are imported over the network via `esm.sh` (using native ES module `import` syntax).
* **Tailwind CSS** is included via CDN and automatically styles elements on the page by parsing the applied utility classes.

This variant is ideal for sharing your interactive CV as a single file. You can send it directly to anyone, and they can open it locally from their hard drive without setting up a development environment.