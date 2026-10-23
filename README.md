# Windows in GitHub Codespaces

Click the button, wait, and Windows opens in your browser.

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/YOUR-USERNAME/YOUR-REPO-NAME)

> Replace `YOUR-USERNAME/YOUR-REPO-NAME` in the link above with this repo's path.

## How to use

1. Click **Code → Codespaces → Create codespace on main** (or use the badge above).
2. Choose a machine with **4 cores or more**.
3. When the codespace starts, a browser tab for port **8006** opens. If it doesn't, open the **Ports** tab and click the globe icon next to 8006.
4. The first boot downloads and installs Windows automatically. This takes roughly 10 to 20 minutes. When you see the desktop, it's ready.

Later starts are much faster because the Windows disk is kept in a Docker volume.

## Settings

Edit `.devcontainer/codespaces.yml` before creating the codespace:

| Setting | What it does |
|---|---|
| `VERSION` | `11`, `10`, `11l`, `10l`, `tiny11`, `tiny10`, `2022`, `2025` and more |
| `RAM_SIZE` / `CPU_CORES` | Resources given to Windows (keep them below the Codespace machine size) |
| `DISK_SIZE` | Virtual disk size |
| `USERNAME` / `PASSWORD` | Windows login (defaults: `Docker` / `admin`) |

## Notes

- Codespaces stop after 30 minutes of inactivity by default. You can change this in your GitHub Codespaces settings.
- Free GitHub accounts get a limited monthly allowance of compute hours and storage. Windows uses a lot of both, so check your Codespaces usage page.
- Windows itself is downloaded from Microsoft's servers at first boot. You are responsible for having a valid Windows license.
- Built on [dockur/windows](https://github.com/dockur/windows).
