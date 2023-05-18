# To make one of this
```
git init <folder>
cd <folder>
npm init --yes
npm install honkit --save-dev
npx honkit init
```
Localser  `npx honkit serve`
Build `npx honkit build`

# For GitHub
```
# important
on: [push]
permissions:
  contents: write
# end important

jobs:
  job_name:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Run a multi-line script
        run: |
          npx honkit build
          echo "hello"
 
      - name: Deploy 🚀
        uses: JamesIves/github-pages-deploy-action@4.1.5
        with:
          branch: gh-pages # pointer 01
          folder: "_book"  the build output folder
```
Then github setting pages to branch `/gh-pages` #pointer 01
