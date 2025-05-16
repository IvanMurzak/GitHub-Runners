# Self hosted GitHub runner setup

It is ready to go setup with minimal required modification to launch it.

## Setup

1. Create `.env-token` file in the root folder.
   ```txt
   GITHUB_ACCESS_TOKEN="11111111111111111111111111111111111"
   ```
2. Replace the token with your real token. [Make a new one](https://github.com/settings/tokens/new). It should have `repo` permissions.
3. Modify `GITHUB_OWNER` in the file `.env` to your GitHub username.
4. Modify `GITHUB_REPOSITORY` in the file `.env` to your repository path.
5. Launch using the command line.
   ```bash
   docker-compose up -d
   ```

## Customization

- Feel free to modify docker-compose files in any way you need.
- Scale instances amount
   ```bash
   docker-compose up -d --scale github-runner=6
   ```
