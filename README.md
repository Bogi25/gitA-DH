# Laravel Boilerplate using docker

[![license](https://img.shields.io/github/license/dec0dOS/amazing-github-template.svg?style=flat-square)](LICENSE)

<details open="open">
<summary>Table of Contents</summary>
  
- [About](#about)
- [Installation](#installation)
- [Additional action](#additional-action)
- [License](#license)
  
</details>

## About
The project is based on [Laravel Boilerplate](https://github.com/rappasoft/laravel-boilerplate?tab=readme-ov-file). Deployment of this project is automated using docker containers. 
Four docker containers are used:
- php
- node
- nginx
- mysql

## Installation

Download the project, be sure to use the --recurse-submodules flag to download the added submodule.
```sh
git clone --recurse-submodules https://github.com/Bogi25/gitA-DH.git .
```
Enter the project folder and run Docker Compose:
```sh
cd gitA-DH
docker compose up
```

## Additional action
Automatic push to DockerHub added through Git Actions.

In the project, one Docker image is built, so on Docker Hub, a repository needs to be prepared:

- _<DOCKER_USERNAME>/php-composer_

For pushing to Docker Hub, the secrets DOCKER_USERNAME and DOCKER_PASSWORD, which were added to GitHub, are used.
When executing the git push command to the repository, an image will automatically be pushed to Docker Hub. The build will be performed by GitHub Actions.

## License
This project is licensed under the MIT license. Feel free to edit and distribute this template as you like.

See [LICENSE](LICENSE) for more information.
