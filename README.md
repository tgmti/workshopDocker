
# Workshop de Docker

![Docker](https://www.mundodocker.com.br/wp-content/uploads/2015/06/docker_facebook_share.png)

# Pauta

## O quê é?

Tenologia de gerenciamento de contêineres que fornece uma camada de abstração da infraestrutura e automação de vitualização do sistema operacionais e aplicações.


## O que é container?

Container é uma forma de isolar a aplicação do sistema operacional Host, em resumo reduzindo consideravelmente o tempo de deploy e as diferenças entre ambiente de desenvolvimento e produção.

Diferente de uma máquina virtual, o sistema operacional do Container não utiliza um hardware emulado, mas sim a camada de comunicação do próprio host para acessar o Hardware (Kernel).

![Diferenças entre Docker e Máquinas virtuais](assets/img/docker_x_vmachine.png)


Além disso, a tecnologia de contêineres permite que a máquina seja montada em camadas, chamadas de Layers.

[![Docker](https://img.youtube.com/vi/QFuOggpDAOw/0.jpg)](https://www.youtube.com/watch?v=QFuOggpDAOw)


## Imagens e Layers

A base para um novo container é chamada de imagem. Uma imagem contém a aplicação e todas as dependências que esta precisar para executar.

[Docker – Images vs Layers](https://gago.io/blog/docker-images-vs-layers/)


## Pra quê serve?

- Bases de Desenvolvimento
- Bases de Teste e Homologação
- Bases de Testes automatizados
- Bases de Demonstração
- Implantação rápida e padronizada
- Padronizar ambientes em produção
- Migrações e atualizações
- Agilidade na duplicação de ambientes


## Versões e Custo

- CE - Community edition: Gratuita e OpenSource
- EE - Enterprise edition
    - Suporte Dedicado
    - Validação de imagens
    - Somente imagens assinadas

Para Linux a versão EE é paga, no Windows Server 2016 e 2019 já vem embarcado (fora o suporte).

- No Windows Server, só funciona a Enterprise Edition.
- No Linux dá pra rodar a CE em produção normalmente.
- Se precisar de enterprise no Linux, é mais vantajoso migrar para uma nuvem

https://www.mundodocker.com.br/docker-ce-ee/

https://hub.docker.com/editions/enterprise/docker-ee-server-windows

https://www.mundodocker.com.br/docker-no-windows-server-2016/


## Portabilidade entre Hosts Linux e Windows

- Existem containers com SO Windows?
    - Sim, porém, imagens com base em Windows só podem ser utilizadas em Hosts Windows.

- Para rodar um container Linux dentro do Windows, é preciso uma Máquina Virtual?
    - Sim e não
    - Atualmente para Windows Server ou 10 Pro, roda sobre o WSL (Windows Subsystem for Linux). Que é um módulo padrão do sistema que permite a instalação de uma Distro Linux dentro do SO Windows, com acesso direto aos recursos de Hardware.
    - Para outros sistemas Windows (W8.1, W10 Home), vai rodar em modo de compatibilidade, sobre uma VM do VirtualBox
    - Já está liberado para W10 Insiders Preview o WSL 2. A segunda versão promete ser muito aprimorada e usará um Kernel real do Linux embarcado no Windows. Expectativa de performance aumenta em até 20x para o WSL 1.

Como o WSL 2 funciona no Windows 10 Home Edition, o Docker Desktop também funcionará.

[Docker ❤️️ WSL 2 - The Future of Docker Desktop for Windows - Docker Engineering Blog](https://engineering.docker.com/2019/06/docker-hearts-wsl-2/)

Lendo este artigo e as outras notícias é possível concluir: Para desktop, o Docker roda no Linux.
O que acontece é que agora a MS vai rodar Linux dentro do W10 mais integrado.

### Outras informações sobre WSL 2:

https://sempreupdate.com.br/microsoft-lanca-windows-subsystem-for-linux-2/

https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/

https://docs.microsoft.com/en-us/windows/wsl/wsl2-about

https://docs.microsoft.com/en-us/windows/wsl/wsl2-ux-changes

https://github.com/luizcarlosfaria/kb/wiki/Docker-no-Windows-vs-Docker-no-Linux


# Cursos e tutoriais

- https://github.com/luizcarlosfaria/kb/wiki

- [Docker Compose: simplificando o deployment de aplicações](https://gago.io/blog/2018-canal-dotnet-docker-compose/)

- [Como criar uma imagem Docker a partir de um Container utilizando o Docker commit](http://devopslab.com.br/docker-como-criar-uma-imagem-docker-a-partir-de-um-container-utilizando-o-docker-commit/)

- [How to commit changes to a docker image](https://www.techrepublic.com/article/how-to-commit-changes-to-a-docker-image/)

- [SQL Server for Linux](https://gago.io/blog/docker-de-az-16-sql-server-for-linux/)


#### Cursos de Docker (em Espanhol):

- [Curso Completo](https://www.youtube.com/playlist?list=PLn5IkU1ZhgiZl4EH7AFkqs-pqF6ZUz_iS)

- [Curso de Docker en Windows Server 2019](https://www.youtube.com/playlist?list=PLn5IkU1ZhgiZP8EewgFdxgnsIwN1q3Juo)

