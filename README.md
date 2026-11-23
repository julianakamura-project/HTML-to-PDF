# LocalHTML2PDF

A simple, privacy-focused HTML-to-PDF converter that runs locally in your browser.

Load an HTML, HTM, or TXT file (or paste HTML directly), optionally decode escaped HTML, preview the result, and use your browser's print dialog to save it as a PDF.

## Try it online

[**Open LocalHTML2PDF**](https://julianakamura-project.github.io/HTML-to-PDF/)

No installation required! Use the converter directly in your browser.

## Features

- **Client-side processing:** The application reads and processes the selected file in your browser.
- **No application upload:** The converter does not send your document contents to a conversion server.
- **No accounts or API keys:** Open the page and use the tool.
- **No third-party JavaScript libraries:** The converter uses native browser functionality.
- **File input:** Select or drag and drop `.html`, `.htm`, and `.txt` files.
- **HTML unescaping:** Decode one layer or multiple layers of escaped HTML entities.
- **Preview:** Review the rendered document before printing.
- **PDF output:** Use the browser's native print dialog and choose **Save as PDF**.
- **File-size limit:** Files up to 20 MB are accepted.

## How to use

1. Download or clone this repository.
2. Open `converter_privacy_hardened.html` in a modern web browser.
3. Select an HTML, HTM, or TXT file, or paste HTML into the source editor.
4. If the content contains escaped HTML entities, choose the unescape depth and click **Unescape HTML**.
5. Click **Update preview** to render the document.
6. Click **Print / Save PDF**.
7. In the browser's print dialog, choose **Save as PDF** and select where to save the PDF.

No installation or account is required.

## Privacy

The converter is designed to process document content locally in the browser.

- The application contains no document-upload feature or conversion backend.
- It does not intentionally transmit document contents to an external server.
- It does not use application-managed cookies, local storage, session storage, or a database to save document contents.
- It does not include analytics or tracking code.
- The preview is sandboxed, and its Content Security Policy blocks network connections and external resource loading.

**Important:** This privacy description applies to the application code. If you host the page online, your hosting provider may independently collect ordinary website access information, such as IP addresses and request logs. Also, the browser itself and any browser extensions are outside the application's control. The preview's restrictive security policy may prevent HTML documents that depend on remote images, stylesheets, fonts, scripts, or other external resources from displaying exactly as they would on their original website.

## Security notes

- The preview iframe runs with a sandbox that does not enable JavaScript.
- The preview uses a restrictive Content Security Policy to block network connections and external resources.
- Files larger than 20 MB are rejected by the file loader.
- Treat HTML files from unknown sources with care, as the browser may interpret their markup when rendering the preview.

The converter is provided as-is. No security review can guarantee protection against every browser vulnerability or every possible input file.

## Compatibility

Use a modern browser with support for HTML `iframe` sandboxing, `srcdoc`, the File API, and the browser print dialog. PDF saving depends on the browser and operating system.

## Project structure

```text
.
└── index.html
└── README.md
└── LICENCE
```

## License

No license has been specified yet. If you want others to reuse, modify, and redistribute this project, add a license file (for example, an MIT License) and update this section accordingly.
