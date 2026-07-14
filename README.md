name: Update posts
on:
  schedule:
    - cron: '0 */6 * * *'   # every 6 hours
  workflow_dispatch:
jobs:
  update:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: gautamkrishnar/blog-post-workflow@master
        with:
          feed_list: "https://medium.com/feed/@mohitparmar22584"
