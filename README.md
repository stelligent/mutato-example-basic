# mutato-example-basic

Mutato's Basic Example

Deploy with:

```bash
$ cd /path/to/your/github/repo
$ echo "GITHUB_TOKEN=$GITHUB_TOKEN" > mutato.env
$ aws-vault exec <profile name> -- env | grep AWS_ >> mutato.env
$ docker run -it --rm --env-file mutato.env -v `pwd`:/project stelligent/mutato bootstrap
$ docker run -it --rm --env-file mutato.env -v `pwd`:/project stelligent/mutato deploy
```

For more info look at: [stelligent.github.io/mutato](https://stelligent.github.io/mutato)
