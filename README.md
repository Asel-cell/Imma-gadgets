# IMMA GADGETS — GitHub + Netlify

This is the page-by-page frontend/backend starter for IMMA GADGETS.

1. Upload the folder to GitHub and connect the repo to Netlify.
2. Netlify automatically reads netlify.toml.
3. Add the secret `ADMIN_PASSWORD` in Netlify Environment Variables. Never commit it.
4. Products are persisted through Netlify Blobs via `netlify/functions/products.mjs`.
5. The 50 MB image field validates the limit in the browser. Large images must upload directly to object storage, not through a Netlify Function. Configure the provider in `upload-url.mjs` before using real uploads.
6. Put the supplied store logo at `/imma-logo.png`.

The project deliberately does not fake a 50 MB storage provider. It returns a clear configuration error until a real object-storage presigned-upload endpoint is connected.
