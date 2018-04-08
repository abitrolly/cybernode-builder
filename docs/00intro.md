
Cybernode is a **cluster** of software components that
provides full information about different blockchains
and tools to work with them. These **components** are:

  - [full blockchain nodes](../images/fullnode) for different blockchains
    - bitcoin-btcd
    - ethereum-parity
  - market data collector and API [cyber-markets][markets]
  - blockchain transaction parser with API [cyber-search][search]
  - web app for services and status [cyber-browser]
  - [others][plzask]

Every component is wrapped into separate Docker **container**,
so that different components can be run on one VM or hardware
machine simultaneously.

To avoid conflicts, each component that needs to be accessed
is available on its own dedicated port following [port mapping
convention](https://github.com/cybercongress/cybernode/issues/22).


### Terminology

  * **node** - VM or physical machine that runs containers
  * **component** - software wrapped into container
  * **cybernode** - cluster of containers connected with each
    other that provides external API and may connect to other nodes
  * **cybernode-builder** - helpers for building components that
    can not be used directly (missing patches, different configs or
    conventions)


### Conventions

  * data location (default `/cyberdata` or `CYBERDATA`)
  * port map
  * user level names and descriptions
  

### Prerequisites

To run **cybernode** and buid , you need Docker installed. To learn about
Docker, take a look at [Katacoda].

We use Ubuntu 18.04 as a reference system with some tests being
done on Fedora 28+.


### Improving this documentation

This documentation can be edited onlne [on GitHUb](https://github.com/cyberFund/cybernode/tree/master/docs)
with applying
[best practice](https://kubernetes.io/docs/home/contribute/style-guide/#content-best-practices)
from Kubernetes and other projects.


[markets]: https://github.com/cybercongress/cyber-markets
[search]: https://github.com/cybercongress/cyber-search
[cyber-browser]: https://github.com/cyberFund/cyber-browser
[plzask]: https://github.com/cybercongress/cybernode/issues/new?title=docs/00intro.md:%20What%20are%20missing%20components?

[katacoda]: https://www.katacoda.com/courses/docker/
