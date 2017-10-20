Running in development with fresh:
  ```
    $ docker-compose up --build
  ```
Production build:
  ```
    $ docker build ./service --build-args app_env=production
  ```

See docker-compose.yml for details.