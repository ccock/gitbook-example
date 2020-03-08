# publish to github


- create github repo and push book

Create github repo and push book to master branch;

github support 3 ways to publish pages: master branch, docs folder in master branch, gh-pages branch;

- build book

```sh
$ gitbook build
```

- push book to `gh-pages` branch

```sh
$ git subtree push --prefix=_book origin gh-pages

$ git push origin master
```



