Мета проекту - тренування підняття проекту з використанням Laravel, docker, php, node.
Додано автоматичне відправка в DockerHub черз Git Actions.

Скачуємо проект, обов'язково з флагом --recurse-submodules для скачування доданного сабмодуля.
git clone --recurse-submodules https://github.com/Bogi25/gitA-DH.git .

Заходимо в папку з проектом cd gitA-DH
Запускаємо docker compose up
В проекті збирається два докер зліпки тому на Docker Hub треба підготувати два репозиторію
<DOCKER_USERNAME>/laravel-dock-php-one
<DOCKER_USERNAME>/laravel-dock-node-t

Для відпривки в DockerHab використано секрети DOCKER_USERNAME та DOCKER_PASSWORD які були додані в GitHub.
Опис знаходиться в файлі .github/workflows/docker-publish.yml
При виконанні команди git push до репозиторію автоматично буде відправка в DockerHub. Збірку буде виконувати Git Actions.
