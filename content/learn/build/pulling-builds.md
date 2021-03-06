## Pulling builds

After you've run your builds on the wercker platform you're able to pull these
pipeline artifacts to your local machine in order to run and introspect them. To
do this, you again need a working
[local docker environment](/learn/basics/the-wercker-cli.html).

There are two ways to retrieve the Docker container. You can either reference a
build-id directly, or you can query wercker.

In order to pull a build you need a `build-id` and of course the right
permissions to a project. You can pull builds with the following
command:

```no-highlight
wercker pull build-id
```

You can also query for a certain build. In order to do this, you need the name
of the owner and project-name on wercker. Then you can optionally give some
extra queries such as branch or result.

```no-highlight
wercker pull owner/project-name [query flags]
```

Checkout the all available flags in the help page:

```no-highlight
wercker pull --help
```

If you have a working Docker environment and you want to load the container
after download, than use the `--load` flag.

- - -
> Want to start pulling builds? Read more about this on the
> [docs](/docs/using-the-cli/pulling-containers.html)

[&lsaquo; Local builds](/learn/build/local-builds.html "nav previous build")
[Introspecting builds &rsaquo;](/learn/build/introspecting-builds.html "nav next build")
