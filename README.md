# terasology-repo - manifests for Terasology

This repository serves manifests for [Terasology](https://github.com/MovingBlocks/Terasology) compatible with the [repo](https://android.googlesource.com/tools/repo) tool.

## Getting Started

To get started with a Terasology workspace using `repo` you can use the following quick-start commands. Be sure to execute them in the folder where your workspace should reside. 

```shell
repo init -u https://github.com/skaldarnar/terasology-repo
repo sync
```

This will set up a local workspace based on [`default.xml`](./default.xml) which is a Iota module line-up and the [TeraNUI](https://github.com/MovingBlocks/TeraNUI) library.

## Alternatives

For a full line up including libraries such as [gesalt](https://github.com/MovingBlocks/gesalt) and all [tutorial modules](https://github.com/Terasology?q=Tutorial&type=source&language=&sort=) you can specify the `all.xml` manifest.

Once you've initialized the repo client, you can omit the URL (`-u`). We recommend to parallelize the `sync` operation by specifiying the number of parallel jobs.

```
repo init -m all.xml
repo sync --jobs 8
```

You can easily switch back to a smaller workspace the same way. `repo` will cache the repositories locally to speed up switching between line-ups. To switch back to the Iota line-up (without TeraNUI) run the following:

```
repo init -m iota.xml
repo sync --jobs 8
```

