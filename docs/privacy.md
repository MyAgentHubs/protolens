# Privacy Notes

ProtoLens is built for teams that care about repository and prototype privacy.

The core privacy idea is simple: use GitHub as the access boundary and avoid turning ProtoLens into a general-purpose file hosting or build server.

## What ProtoLens Needs

ProtoLens needs enough access to:

- read selected static prototype files,
- create stable review links,
- store or export review comments associated with those prototypes,
- let authorized owners retrieve review feedback.

## What ProtoLens Avoids

ProtoLens avoids:

- cloning and building arbitrary user repositories in production,
- installing dependencies from user repositories,
- running user application backends,
- publishing private prototype files as open public assets outside the review URL model.

## Public Repository

This repository is intentionally limited to public product documentation and screenshots. It should not contain customer data, private prototype files, tokens, secrets, internal deployment instructions, or production source code.
