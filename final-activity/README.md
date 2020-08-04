# Redes Neurais Artificiais

**Atividade Final**: Nesta atividade em grupo, vocês devem determinar o problema e a abordagem.

É esperada a comparação de, ao menos, **dois** modelos de machine learning, sendo um deles `Redes Neurais Artificiais` (`MLP` ou qualquer modelo de `Deep Learning`) e, o outro, algum modelo **não visto** em sala de aula: `Algoritmos de otimização` em geral (`Genéticos`, baseados em enxames ou colônia de formigas), `GANs`, técnicas de `Aprendizado por Reforço`, etc.

Espera-se que o problema escolhido tenha dificuldade/complexidade de acordo com o nível final da disciplina e com o tamanho dos grupos. Problemas atuais, desafiadores e públicos serão bonificados na avaliação. Desafios competitivos e com recompensa do kaggle são recomendados!

Como resultado, além de todo o código, o grupo deve apresentar o trabalho feito utilizando os recursos que julgar necessários (apresentação, notebook, código, gráficos, etc). A técnica não vista em sala (modelo de Deep Learning ou outro escolhido)  deve ter seus conceitos e implementação apresentados para que todos a aprendam - conversem entre si para que uma mesma técnica não seja apresentada duas vezes.

## Instruções Gerais

**Apresentação**: segunda, dia 06/07/2020, 8:45 - 20min por equipe, tolerância de 2 minutos.

**Premissas**:

- Os grupos podem ter até 4 integrantes, podendo ser os mesmos grupos da disciplina de projeto
- Os resultados devem ser proporcionais a quantidade de integrantes
- Não é permito mais de um grupo com o mesmo problema (dados)
- É incentivada a utilização de técnicas diferentes e mais diversas possíveis

**Critérios**:

- Definição do problema (complexidade / desafio / atualidade / etc)
- Entendimento, tratamento e visualização dos dados
- Escolha, modelagem e aplicação das técnicas
- Código
- Resultados e Avaliação
- Apresentação geral
- Apresentação da técnica utilizada

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
