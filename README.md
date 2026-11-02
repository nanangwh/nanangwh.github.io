# nanangwh.github.io

Developer site for nnwh: portfolio, per-app privacy policies, and `app-ads.txt`.
Built by GitHub Pages' built-in Jekyll from the `main` branch. No build step needed.

| URL | Source |
|---|---|
| `/` | `index.html` (app list comes from `_data/apps.yml`) |
| `/privacy/` | `privacy/index.html` |
| `/privacy/<slug>/` | `privacy/<slug>.md` |
| `/app-ads.txt` | `app-ads.txt` (must stay at the root for AdMob) |

## Adding an app

1. Add an entry to `_data/apps.yml` (`slug`, `name`, `tagline`, `play`).
2. Add a 256×256 icon at `assets/icons/<slug>.png`.
3. Add `privacy/<slug>.md` with front matter:

   ```yaml
   ---
   layout: policy
   title: Privacy Policy for <App Name>
   app: <slug>
   permalink: /privacy/<slug>/
   ---
   ```

4. Use `https://nanangwh.github.io/privacy/<slug>/` as the privacy policy URL in Play Console / App Store Connect.

When a policy changes, edit the file and update its effective date. Git history keeps the earlier versions.

## Preview locally

```sh
gem install jekyll -v 3.10.0 kramdown-parser-gfm
jekyll serve
```
