# Technical Seminar Website
## Environment Setup

- Install and setup [Docker](https://www.docker.com/) following [this instruction](https://gist.github.com/wataridori/5eed8c76cd6120b609d30d21f0785d45) for your local machine.
- **Restart your machine**
- `cd` to project folder.
- Create `.docker` folder inside project root folder and make it writeable.
- Make `storage/` and `bootstrap/cache/` folder writeable.
- Run command:
```
docker-compose up -d
// Run the following command to check docker status
docker ps
```
- SSH into `seminar_workspace` container:
```
docker exec -it seminar_workspace /bin/bash
```
    - Run `composer install` (for `vendor` directory).
    - Run `php artisan migrate` (for preparing database).
    - Run `gulp` (for compiling asset files).
- Check project working at:

```
http://localhost:8000/
```