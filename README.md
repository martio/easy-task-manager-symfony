# Easy Task Manager

A [Docker](https://www.docker.com/)-based installer and runtime for the [Symfony](https://symfony.com) web framework,
with [FrankenPHP](https://frankenphp.dev) and [Caddy](https://caddyserver.com/) inside!

![CI](https://github.com/dunglas/symfony-docker/workflows/CI/badge.svg)

## Getting Started

1. If not already done, [install Docker Compose](https://docs.docker.com/compose/install/) (v2.10+)
2. Run `docker compose build --no-cache` to build fresh images
3. Run `docker compose up --pull always -d --wait` to start the project
4. Open `https://localhost` in your favorite web browser and [accept the auto-generated TLS certificate](https://stackoverflow.com/a/15076602/1352334)
5. Run `docker compose down --remove-orphans` to stop the Docker containers.

## Task Description

Your objective is to create a simple task management system. This system should enable operations such as adding, editing, deleting, and viewing tasks through a REST API interface. Each task in the system should be associated with a specific user and have a status (e.g., "to be done", "in progress", "completed"). An important aspect is also the verification of the ability to manage tasks of a particular user, which should be regulated by appropriate policies. Additionally, it is necessary to prepare a dedicated endpoint for importing user data (by ID) from the website https://dummyapi.io/docs/user and saving it in the system's database.

## Task Solution

Given the lack of complex business logic, the traditional DDD approach might seem excessive. Therefore, at first glance, the CRUD approach appears more fitting. However, aiming to implement several architectural and design patterns as well as best practices, I decided to use the DDD approach, Hexagonal Architecture, Bounded Context techniques, CQRS, and Event-Driven Architecture.

## Credits

- [Marcin Lewandowski](https://github.com/martio)
