# Projeto Final - Administração de Sistemas Abertos - 2022.2 

<p align="center">

<img alt="GitHub language count" src="https://img.shields.io/github/languages/count/AbranJames/EyesUp_Pipeline?color=%2304D361">

<img alt="Repository size" src="https://img.shields.io/github/repo-size/AbranJames/EyesUp_Pipeline">

<img alt="Made by AbranJames" src="https://img.shields.io/badge/made%20by-AbranJames-%2304D361">

</p>

# :pushpin:  Índice

<p align="center">
    <a href="#sobre-o-projeto">Sobre esta aplicação</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
    <a href="#como-funciona">Como funciona</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
    <a href="#tecnologias-utilizadas">Tecnologias utilizadas</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
    <a href="#como-rodar-o-projeto">Como rodar o projeto</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
    <a href="#como-rodar-o-projeto-docker">Como rodar o projeto (direto via container docker compose)</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
    <a href="#licença">Licença</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
    <a href="#contato">Contato</a>
</p>



<h1><a id="sobre-o-projeto"> :bulb:  Sobre esta aplicação </a></h1>

Projeto final da disciplina de Administração de Sistemas Abertos. 
Este repositório contém os arquivos de configuração do Vagrant, Ansible e Docker para a criação de uma VM versionado em Ansible que por sua vez executa o docker compose para instanciar containers de um servidor web (wordpress), banco de dados mysql e proxy reverso utilizando o nginx.


<h1><a id="como-funciona"> :wrench:  Como funciona </a></h1>

A pipeline do projeto é composta por 4 etapas, sendo elas descritas abaixo pelos seus respectivos arquivos:
- `Vagrantfile`: Criação de uma máquina virtual para a implantação do projeto
- `Playbook Ansible`: Instalação e configuração de todos os softwares necessários para a execução do projeto
- `Docker Compose`: Criação de um arquivo de configuração para a execução dos containers


<h1><a id="tecnologias-utilizadas"> :rocket:  Tecnologias utilizadas</a></h1>

- [Vagrant](https://www.vagrantup.com/)
- [Ansible](https://www.ansible.com/)
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

<h1><a id="pre-requisitos"> :warning:  Pré-requisitos para utilizar com o Vagrantfile</a></h1>

Antes de começar, o Vagrantfile utiliza o Provider VirtualBox, portanto é necessário que o mesmo esteja instalado em sua máquina. Caso não tenha, acesse o link abaixo e siga as instruções de instalação:

- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)


<h1><a id="como-rodar-o-projeto"> :computer:  Como rodar o projeto (Utilizando o Vagrantfile (VM))</a></h1>


```bash
# Clone este repositório
$ git clone https://github.com/AbranJames/project_asa.git

# Acesse a pasta do projeto no terminal/cmd
$ cd project_asa

# Execute o comando abaixo para criar a máquina virtual
$ vagrant up

# Nesse momento o Vagrantfile irá criar a máquina virtual e executar o playbook ansible para a instalação e configuração dos softwares necessários para a execução do projeto. Em seguida, o Docker Compose irá criar os containers e executar o projeto. Para acessar a aplicação, acesse a newtork da VM na porta 8080 digitando no navegador:
http://192.168.57.10:8080

# Para parar a execução do projeto, execute o comando abaixo:
$ vagrant halt
```

<h1><a id="como-rodar-o-projeto"> :computer:  Como rodar o projeto (direto via container docker compose)</a></h1>


```bash
# Clone este repositório
$ git clone https://github.com/AbranJames/EyesUp_Pipeline.git

# Acesse a pasta do projeto no terminal/cmd
$ cd EyesUp_Pipeline

# Execute o comando abaixo para criar o container e executar o projeto
$ docker compose up -d

# Nesse momento o Docker Compose irá criar os containers e executar o projeto. Para acessar a aplicação, coloque no navegador:
http://localhost:8080

# Para parar a execução do projeto, execute o comando abaixo:
$ docker compose down
```


<h1><a id="licença"> :pencil:  Licença</a></h1>


MIT License

Copyright (c) 2012-2022 Thiago Abrante de Souza

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

<h1><a id="contato"> :iphone:  Contato</a></h1>

- [Thiago A. Souza](mailto:thiago.abrante@academico.ifpb.edu.br)






