# Referral

## notes
### how to use theme
Althought official recommend use `As a Hugo Module`, but if you want deploy it to [Vercel](https://vercel.com/guides/deploying-hugo-with-vercel), [As-git-submodule](https://github.com/theNewDynamic/gohugo-theme-ananke#as-git-submodule) is recommended, details [Need to install Go to use Hugo modules](https://github.com/vercel/community/discussions/38)!

### build error
If not set special Hugo version, when vercel build will get this message `Module "ananke" is not compatible with this Hugo version;`, the issue is [#7525](https://github.com/vercel/vercel/issues/7525)

the solutions:
- use `vercel.json`
set HUGO_VERSION
```json
{
  "build": {
    "env": {
      "HUGO_VERSION": "0.105.0"
    }
  }
}
```
- environment-variables
set env variable on vercel [project setting](https://vercel.com/docs/concepts/projects/environment-variables)

more details: [discussions#5834](https://github.com/vercel/vercel/discussions/5834)
