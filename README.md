# Simple Markdown Renderer

## Summary

This is a single-page static web application that renders a predefined Markdown string into styled HTML. It utilizes the `marked.js` library for Markdown-to-HTML conversion and `highlight.js` for syntax highlighting within code blocks. The application features a clean, dark-themed presentation for the rendered content.

## Setup

This is a standalone static HTML file. No installation or build process is required.

1.  Save the code as `index.html`.
2.  Open the `index.html` file directly in any modern web browser.

## Usage

To change the content that gets rendered, you need to edit the `index.html` file:

1.  Open `index.html` in a text editor.
2.  Locate the `<script>` tag at the bottom of the file.
3.  Modify the content of the `markdownInput` constant with your own Markdown text.
    javascript
    const markdownInput = `# Your Title Here
    
    Your content here.
    
    \`\`\`javascript
    console.log("Hello, world!");
    \`\`\``;
    
4.  Save the file and refresh it in your browser to see the updated content.

## Code Explanation

The entire application is contained within a single `index.html` file, which is structured as follows:

*   **HTML:** The `<body>` contains a single `<div>` element with the ID `markdown-output`, which serves as the container for the rendered HTML.
*   **CSS:** Styles are embedded within the `<head>` in a `<style>` tag. They provide a dark theme, responsive layout, and formatting for common Markdown elements like headings, paragraphs, and code blocks.
*   **JavaScript:**
    1.  **Dependencies:** The application loads `marked.js` and `highlight.js` (along with a theme CSS for it) from a CDN.
    2.  **Execution:** An event listener on `DOMContentLoaded` ensures the script runs only after the full page has been loaded.
    3.  **Logic:** The script takes a hardcoded Markdown string, converts it to HTML using `marked.parse()`, injects the result into the `#markdown-output` div, and then calls `hljs.highlightAll()` to apply syntax highlighting to all code elements.

## License

This project is licensed under the MIT License.