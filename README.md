# Tailwind CSS Classes Not Applied Due to Premature Rendering in SSR Environment

This repository demonstrates a common bug encountered when using Tailwind CSS with server-side rendering (SSR) frameworks like Next.js or Nuxt.js. The issue stems from applying Tailwind classes to elements before Tailwind's post-processing step, leading to missing or incorrect styles.

## The Problem

In frameworks employing SSR, components might render on the server before the client-side JavaScript fully initializes Tailwind.  If you attempt to style elements during this early server-side rendering phase, Tailwind's transformation may not have yet occurred. This results in the server rendering the HTML with raw Tailwind classes instead of the actual CSS styles.

## Steps to Reproduce

1. Clone the repository.
2. Run `npm install`.
3. Run the development server (instructions may vary based on the framework).
4. Observe the rendered output in your browser's developer tools. You'll notice the absence or incorrect application of expected styles.

## Solution

This repository contains a solution demonstrating how to address this issue by ensuring that Tailwind's post-processing happens before the component is rendered to the client.

## Contributing

Contributions are welcome!