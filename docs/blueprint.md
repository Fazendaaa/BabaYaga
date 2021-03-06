{{ template:title }}

{{ template:logo }}

{{ template:badges }}

{{ template:description }}

Welcome to Fazendaaa's {{ pkg.name }}. This is version {{ pkg.version }}!

Made with:

- [Go](https://golang.org/)
- [Docker](https://www.docker.com/)

## Ideia

Currently, in the company that I work for we have a CLI (Command Line Interface) made in [Python](https://www.python.org/) called `estat` that you can read more about it right [here](https://github.com/Fazendaaa/Succubus). But one of its features is cloud integrations in services based on containers, like in Azure, AWS, GCP and your own Kubernetes (K8s) cluster; the idea is to allow the developer to allocate resources based in without ever needing to open a web based or needing to handeling many CLIs to do so or having to waste time doing so.

The main ideia is that you have a `baba.yaml` like the following describing the resources to deploy them later on -- probably as CI/CD but easily created, managed and configured rather than copying and pasting some other config:

```yaml
azure:
  web-app:
    resource-group: myResourceName
    instances:
      - myInstanceA:
        storage: true
      - myInstanceB:
        storage: false
      - myInstanceC:
        storage: true
...
```

As `estat` have grown so much and making it available as FOSS (Free and open-source software) was always the idea but the project still in development and not having a properly defined scope, I decided to break its main features in other projects:

- [Succubus](https://github.com/Fazendaaa/Succubus): universal package manager based on cloud-native
- [Jinn](https://github.com/Fazendaaa/Jinn): universal project manager built to expand Succubus capabilities
- [Baba Yaga](https://github.com/Fazendaaa/BabaYaga): universal cloud-native manager built to expand Jinn and Succubus capabilities
- [Wendigo](https://github.com/Fazendaaa/Wendigo): universal project translator from cloud-native projects to other infra technologies
- [Shōjō](https://github.com/Fazendaaa/Shojo): LaTex package manager
- [Hellhound](github.com/Fazendaaa/Hellhound): VSCode extension to integrate Jinn recipes
- [Crocotta](github.com/Fazendaaa/Crocotta): SOC assisted guider

## Components

### init

```shell
baba init
```

### new

```shell
baba new
```

### del

```shell
baba del
```

## Installing

You don't need to install Go to run this tool, just Docker. And to do so to give it a try, you can do it just by running the following line in your terminal:

```shell
alias baba='docker run -it --volume $(pwd):/project --workdir /project fazenda/babayaga'
```

And then running the following to check whether or not is working properly:

```shell
baba --help
```

## Running

## Author

Only [me](https://github.com/Fazendaaa) because the aforementioned project was implemented by yours only. By knowing each line of that code wrote doing the port would be more easily done this way.

## Contributing

Check more about this in [CONTRIBUTING.md](CONTRIBUTING.md). Here we have a list of some of our contributors:

{{ template:contributors }}

## TODO

## References

{{ template:license }}
