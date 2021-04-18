# Docker rails tuto

- `docker build -t rails-toolbox --build-arg USER_ID=$(id -u) --build-arg GROUP_ID=$(id -g) -f Dockerfile.rails .`
- `docker run -it -v $PWD:/opt/app rails-toolbox rails new --skip-bundle [*project-name*]`
- `rm -rf [*project-name*]/.git`
- `docker-compose up`
- `docker-compose up --build`
- `docker-compose run [*project-name*] rails hotwire:install`
- `docker-compose up --build`
- `docker-compose run chat rails g scaffold room name:string`
- `docker-compose run chat rails db:migrate`
- `docker-compose up`