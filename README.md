Hello, I’m Kian ebtekari 👋
  - I am building a site :smiley:
  - and I want to work on hacking a bit :balloon:
  - I want to become a good programmer :star:

<!-- BLOG-POST-LIST:START --><!-- BLOG-POST-LIST:END -->

name: Latest blog post workflow
on:
  schedule: # Run workflow automatically
    - cron: '0 * * * *' # Runs every hour, on the hour
  workflow_dispatch: # Run workflow manually (without waiting for the cron to be called), through the Github Actions Workflow page directly

jobs:
  update-readme-with-blog:
    name: Update this repo's README with latest blog posts
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: Pull in dev.to posts
        uses: gautamkrishnar/blog-post-workflow@master
        with:
          feed_list: "https://dev.to/feed/gautamkrishnar,https://www.kianebtekari.com/feed/"

<!---
KianEbtekari0/KianEbtekari0 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
