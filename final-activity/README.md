# Artifical Neural Networks

**Final Activity**: On this group activity, you should determine the problem and approach.

It is expected the comparison of, at least, **two** models of machine learning, being one of them `Artifical Neural Networks` (`MLP` or any other `Deep Learning` model) and another, **unseen** model: `Optimization Algorithms` in general (`Genetics`, based on swarms of bees or ant colonies), `GANs`, `Reinforcement Learning` techniques, etc.

It is expected that the problem choosen has a difficulty accordingly to the final activity of the course. Actual problems, challenging and public will have a bonus. Competitive challenges and challenges with a reward from Kaggle are recommended!

As a result, besides all the coding, the group should present the work that was done using all the resources that they feel that are necessary (presentation, notebook, coding, graphs, etc). The technique unseen on class should have the concepts and implementation presented, so everyone can learn from it.

## General instructions

**Presentation**: Monday, 06/07/2020, 8:45AM - 20min per team

**Criteria**

- Problem definition (complexity / challenge / if the problem is up-to-date / etc)
- Understanding, data processing and visualization
- Choice, modeling and application of the techniques
- Code
- Results and Evaluation
- General presentation
- Presentation of the technique that was used


## 🐳 Docker installation and usage

### Requirements

- [Docker](https://docs.docker.com/get-docker/)
- [Docker-compose](https://docs.docker.com/compose/install/)

### Building and running

First, make sure you are inside this repository's directory:

```bash
cd <path/to/repo>
```

Then, start the container:

```bash
# start the container in the background of your terminal
docker-compose up --detach
```

At this point, the Jupyter Notebook will be running at `http://localhost:8888`.

### Installing new packages

There are a few ways you may install new packages to the container. It'll depend on your goal and needs.

#### Pip

If you need to do update or add packages via `pip`, execute the following command **inside your jupyter notebook**:

```bash
import sys

# install a pip package in the current Jupyter kernel
!{sys.executable} -m pip install <package>
```

> _**note**_: the `!` notation is used to run `pip` directly as a shell command from the notebook. Also, take a look [here](https://jakevdp.github.io/blog/2017/12/05/installing-python-packages-from-jupyter/) to see why you should NOT use `!pip install <package>`.

#### Conda

If you need to do update or add packages via `conda`, execute the following command **inside your jupyter notebook**:

```bash
import sys

# install a conda package in the current Jupyter kernel
!conda install --yes --prefix {sys.prefix} <package>
```

> _**note**_: the `!` notation is used to run `conda` directly as a shell command from the notebook. Also, take a look [here](https://jakevdp.github.io/blog/2017/12/05/installing-python-packages-from-jupyter/) to see why you should NOT use `!conda install --yes <package>`.

#### System

To add or update system packages, you will need `root` user permissions. To achieve this, use the following command:

```bash
# execute the container's shell
docker exec -it --user root tensorflow_notebook /bin/bash

# install a package to the system the container runs on
sudo apt install <package>
```

### Wrapping up

Once you're done, you may remove what was created by `up` with the following command:

```bash
# stop containers and removes containers, networks, volumes, and images created by `up`
docker-compose down
```
