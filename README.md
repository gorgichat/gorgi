# Gorgi

Small, focused repository for a production-ready Gorgi Chat deployment.

Clone

- Clone including submodules in one step:

  ```bash
  git clone --recurse-submodules https://github.com/gorgichat/gorgi
  # or
  git clone --recurse-submodules git@github.com:gorgichat/gorgi.git  
  ```

- Or clone first, then fetch submodules:

  ```bash
  git clone https://github.com/gorgichat/gorgi
  cd gorgi
  git submodule update --init --recursive
  # or
  git clone git@github.com:gorgichat/gorgi.git
  cd gorgi
  git submodule update --init --recursive

  ```

## Quick commands

- Update submodules and push changes:

  ```bash
  git submodule foreach git pull
  git add .
  git commit -m "msg"
  git push
  ```

- Bring everything up (build):

  ```bash
  docker compose up --build
  ```

- Run in background (detached):

  ```bash
  docker compose up --build -d
  ```

- If images are already built:

  ```bash
  docker compose up
  ```

- Stop and remove containers/networks:

  ```bash
  docker compose down
  ```

## Notes

- This repo is intended for mainstream production deployment; keep secrets out of the tree and use environment variables or a secrets manager.
- Check `backend` and `frontend` folders for service-specific configuration.

That's it — simple, practical, and ready for production workflows.

