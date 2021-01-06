# smartfix

When creating a new banner:

1. `git checkout master`
2. `git pull`
3. `git checkout -b my-new-banner` (replace `my-new-banner` with name of new banner).
4. Copy `banners/template` into a new directory under `banners/` with a descriptive name, e.g. `banners/my-banner-200x400`. *The name should not start with a number*.
5. Replace the `banner.json` file in the new directory with the new lottie JSON.
6. If applicable, replace the `images` directory in the new directory with the assets directory for the new banner.
7. Open the `index.html` file and edit the width/height, and replace the name (look for `var name = "..."`) in the `<script>` block.
8. Add the new banner to the `index.html` in the repo root, by copying the last entry and replacing the name and width/height as appropriate.
9. `git add . && git commit -m "Added my-new-banner"` (replace `my-new-banner` with banner name).
10. `git push`
11. Follow the link shown to open a new pull request. Open the PR and wait for the Netlify preview link to come up, then follow that link to test the new banner.
12. To publish, just merge the PR. It'll come up on `https://banners.smartfix.is` in a few minutes.
