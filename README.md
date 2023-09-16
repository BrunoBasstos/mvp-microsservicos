# mvp-microsservicos
PUC-RIO - ENGENHARIA DE SOFTWARE - MVP III
![todo-app-diagrama](https://github.com/BrunoBasstos/mvp-microsservicos/assets/5402439/940bb453-9620-4fbb-b703-44795e7d268e)

Este é um MVP para conclusão da terceira sprint do curso de pós graduação em engenharia de software da PUC-Rio.

O escopo dete projeto é a criação de uma aplicação implementando arquitetura de microsserviços.

Para a implementação deste MVP, foram criadas três aplicações:

- [ToDo App](https://github.com/BrunoBasstos/mvp3-app-todo) é uma aplicação frontend desenvolvida em React;
- [ToDo API](https://github.com/BrunoBasstos/mvp3-api-todo), uma aplicação Flask para gerenciamento de usuários e tarefas;
- [Bridge API](https://github.com/BrunoBasstos/mvp3-api-bridge), uma aplicação Flask que intermedia a comunicação com a [OpenWeather API](http://openweathermap.org) para
obtenção de nomes de cidades e de previsão do tempo.

Para mais informações sobre cada uma das aplicações, consulte os respectivos repositórios.

## Sobre o projeto

Este repositório visa ser tão somente um facilitador para a execução do projeto como um todo, concentrando em um único docker-compose.yml a configuração de todos os containers necessários para a execução das aplicações.

Não é necessário utilizar este repositório para executar o projeto. Você pode clonar cada um dos repositórios das aplicações e executá-las individualmente.

## Como executar

1. Clone este repositório usando `git clone git@github.com:BrunoBasstos/mvp-microsservicos.git --recurse-submodules` para clonar os submódulos também.
    - Caso você já tenha clonado o repositório sem utilizar a flag `--recurse-submodules`, execute `git submodule update --init --recursive` para clonar os submódulos.
    - Isto criará as seguintes pastas:
        - `mvp3-app-todo` com o código da aplicação frontend;
        - `mvp3-api-todo` com o código da aplicação backend;
        - `mvp3-api-bridge` com o código da aplicação que intermedia a comunicação com a [OpenWeather API](http://openweathermap.org).
2. Acesse a pasta de cada aplicação e crie o arquivo .env para cada uma delas usando os respectivos arquivos .env.example como base.
3. Execute o comando `docker compose up -d --build` para criar as imagens e os containers e iniciar as aplicações.
4. Acesse a aplicação em `http://localhost:3000`.
    - Você poderá fazer um aesso inicial com o usuário `admin@mail.com` e senha `admin1234` ou registrar-se para iniciar como um usuário comum.

## Pré-requisitos
- Docker e Docker Compose instalados e configurados corretamente.

## Contribuições

Contribuições são sempre bem-vindas! Se você deseja contribuir com este projeto, por favor, abra uma issue para discutir
sua ideia antes de submeter um pull request.

## Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo [LICENSE](LICENSE) para mais detalhes.
