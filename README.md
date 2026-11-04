# ProtoLens

**Work with AI. Turn ideas into the outcomes you really want.**

ProtoLens is a platform for people and AI to align on goals and review plans. By reviewing concrete plans and interactive prototypes, people clarify requirements, goals, and trade-offs. Their AI publishes work through MCP, reads feedback, and iterates on versions, helping carry agreed plans through implementation and human verification.

[Product overview](https://www.myagenthubs.com/protolens/) · [中文介绍](https://www.myagenthubs.com/zh-CN/protolens/) · [Open ProtoLens](https://protolens.myagenthubs.com) · [MCP endpoint](https://protolens.myagenthubs.com/mcp)

## Why ProtoLens

You do not need a complete brief to begin. Let your AI turn an initial idea into a plan you can discuss and a prototype you can try, then publish them to ProtoLens. Give feedback and make choices in context; your AI adjusts the work. Each round helps clarify your goals and approach. Your AI then carries the agreed plan into implementation, and you verify the result.

ProtoLens holds the plans, prototypes, feedback, and version reviews. The AI you connect creates, revises, and implements the work.

## How It Works

1. **Share an idea.** Connect your AI client to ProtoLens and authorize access. Ask it to turn your idea into a plan and prototype and publish them to ProtoLens.
2. **Make the idea concrete.** Your AI publishes V1 and returns a private review link. Plans and interactive prototypes are presented as self-contained HTML.
3. **Review and choose.** Open the link, try the prototype, comment on specific content, answer decision questions, and submit feedback. Reviewers use a nickname and do not need an account.
4. **Refine and review again.** Ask your AI to read the submitted feedback, publish the next version, and explain how it handled each item. Verify the changes and repeat as your goals and trade-offs become clearer.
5. **Implement and verify.** Once you agree on the direction and plan, ask your AI to implement it in your development environment. You verify that the result meets your goals.

**An AI response is not human acceptance.** Reviewers verify whether the changes address their original feedback. Publishing a revision does not by itself mean the work is accepted.

The main publishing flow uses MCP and does not require a GitHub repository, GitHub App installation, or repository token.

## Who It Is For

ProtoLens is for people building with AI: individuals, small product teams, internal tool teams, and reviewers who need to clarify an idea before committing to an implementation. Use it when an initial request still leaves questions about the goal, the preferred approach, or what an acceptable result looks like.

## Connect Your AI

Use the remote MCP endpoint in a compatible client and complete the authorization flow:

```json
{
  "mcpServers": {
    "protolens": {
      "url": "https://protolens.myagenthubs.com/mcp"
    }
  }
}
```

Your connected AI can publish works, read submitted feedback, and publish revised versions. Reviewers only need the review link; they do not configure MCP.

Client support depends on the application, plan, and workspace settings. Connecting MCP is not a promise that every client can automatically resume a conversation when a review is submitted. The basic workflow is to ask your connected AI to read the feedback and continue. Implementation and deployment remain actions for your AI in the environment you authorize.

## Access, Security, And Privacy

ProtoLens is currently available through invitation-only early access. See the [product page](https://www.myagenthubs.com/protolens/) for availability and plan details.

- A private review link can be opened, used for comments, or forwarded by anyone who holds it. Owners can revoke a link to stop future access; already viewed or downloaded copies cannot be recalled.
- Review drafts are private until submission. People using the same link can see submitted feedback.
- AI connections and review links have separate access controls and can be revoked separately.
- Prototypes run in an isolated review sandbox. Use mock data; the review environment does not host your production application backend.

Read the current [Privacy Policy](https://protolens.myagenthubs.com/privacy), [Terms](https://protolens.myagenthubs.com/terms), and [Security Overview](https://protolens.myagenthubs.com/security).

## Public Repo Scope

This repository contains public product documentation and historical screenshots. It does not contain the production implementation, deployment configuration, secrets, or private user and review data.

The older guides under `docs/` describe the earlier GitHub-backed prototype-review workflow. They are historical reference material; use the workflow above and the product page for the current MCP publishing experience.

## Links

- Product overview: https://www.myagenthubs.com/protolens/
- Application: https://protolens.myagenthubs.com
- MCP: https://protolens.myagenthubs.com/mcp
- AI-readable product summary: [llms.txt](llms.txt)
- Contact: support@myagenthubs.com
