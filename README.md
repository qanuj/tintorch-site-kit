# tintorch-site-kit

**This is not where the shared code lives. It is [`@tintorch/web`](https://github.com/qanuj/tintorch-web).**

This repo was created to hold the pieces the CMS sites share. It turned out
that package already existed, had four sites installing it, and was the wrong
size rather than the wrong place: it covered what the sites emit (sitemaps,
robots.txt, feeds, badges, analytics) and not what they read.

So the shared code grew there instead, in `@tintorch/web` v2:

| Subpath | What it holds |
|---|---|
| `@tintorch/web` | badges, analytics, verifications, sitemaps, robots, llms.txt, RSS |
| `@tintorch/web/cms` | the delivery client, CMS-defined forms, field readers |
| `@tintorch/web/markdown` | raw-HTML escaping, `:::faq` fences, the sanitiser allowlist |
| `@tintorch/web/slug-guard` | what a section publishes, for the edge to check |

```bash
npm install github:qanuj/tintorch-web#semver:^2.0.0
```

Nothing is planned for this repo. It is kept only so the name is not taken by
something else later.
