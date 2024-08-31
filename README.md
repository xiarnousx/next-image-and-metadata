# Image Optimization

- Using `Image` component imported from `nextjs/image`:
- Optimize the size
- Visual stability
- Faster page load time
- Image resizing even if images are on remote servers
- Out of the box, `Image` component if images is imported from local file system there's no need for any additional attributes
- `Image` width and height are required to prevent layou shift thus visual stability
- srcset added automatically to load different images for different screens densities
- setting width and height on `Image` component is not recomended, setting sizes attribute is what nextjs recommends
- NextJs sets `lazy` on the `loading` attribute on the `img` element
- You can set `priority` flag on `Image` which disable `lazy` loading. It is helpful depends on the use case
- Checkout the documenations for `Image` component

# Optimizing Images With Unkown Sizes

- Set the `fill` flag on the image with src, the image fill the entire screen
- we don't know in advance the image size
- When using `Image` go to the container that has the `Image` component
- go to next.config.mjs see next.config.mjs
- The `Image` component takes `loader` prop that accept configs argument, this can help to manipulate the image

# Optimizing Page Metadata

- Metadata picked up by search engine crawlers
- Browse Metadata docs
- There are two types static and dynamic metadata
- Metadata must be in a page.js or a layout.js files
- You can add more than just title and description
- You can add open graph that allows sharing on social platforms
- nextjs looks for object const `metadata` or async function named `generateMetadata
- metadata set on pages either statically or dynamically
- Also, metadata can be set in `layout.js` files, will be used for all pages that do not have metadata object or merged with pages that have metadata
