# Security And Privacy

ProtoLens is designed for static prototype review, not arbitrary application hosting.

## Data Boundary

ProtoLens uses GitHub as the source of truth for repository access and review data.

- Users authorize access through GitHub.
- Repository access follows the selected GitHub App installation.
- Prototype files are fetched by repo, ref, and path.
- Review comments are associated with the prototype file and exported as Markdown-oriented feedback.

The public `MyAgentHubs/protolens` repository contains only product documentation and screenshots. It does not contain production source code, secrets, deployment files, or user data.

## Static Review Model

ProtoLens focuses on HTML, SVG, and PNG prototypes.

For HTML review pages, the product is intended to render static prototypes in a constrained review environment. It is not meant to run untrusted build steps, clone repositories into a server runtime, install dependencies, or execute application backends.

## Practical Limits

To protect GitHub and Cloudflare usage, ProtoLens applies conservative limits during discovery and review creation.

Examples:

- Large files may be marked as too large.
- Unsupported file types may be skipped.
- Requests can be rate limited or retried when usage grows.

These limits keep the early product reliable while still supporting the common AI prototype workflow.

## MCP Tokens

ProtoLens supports MCP access for AI tools. Dashboard-generated token configurations are intended to be short lived.

Do not paste MCP bearer tokens into public issues, chats, screenshots, or repositories. If a token is exposed, regenerate it and revoke any related GitHub authorization if needed.
