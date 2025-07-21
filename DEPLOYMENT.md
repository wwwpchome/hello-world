```auto-deploy script for GitHub Actions```

# Auto Deploy to Hostinger VPS

This project includes a GitHub Actions workflow for automatic deployment to your Hostinger VPS whenever you push to the `main` branch.

## Prerequisites

1. **SSH Access:**  
   Ensure your VPS allows SSH access with a private key (add the public key to `~/.ssh/authorized_keys` on your VPS).

2. **Secrets Setup:**  
   In your GitHub repo, go to **Settings > Secrets and variables > Actions** and add:
   - `VPS_HOST` – Your VPS IP or domain
   - `VPS_USER` – Your VPS username
   - `VPS_SSH_KEY` – Your private SSH key (no passphrase, PEM format)

3. **Directory:**  
   Code should be cloned to `/home/<VPS_USER>/calendar-stories-app` on your VPS.

4. **PM2:**  
   PM2 should be installed globally on your VPS (`npm install -g pm2`).

## How it works

- On push to `main`, the workflow will:
  - Install server and client dependencies
  - Build the frontend
  - Connect to VPS via SSH
  - Pull latest code, install deps, build frontend, restart PM2 process

## Customization

Edit `.github/workflows/deploy.yml` if your directory or process differs.

---

For questions or troubleshooting, see Hostinger docs or ask your devops engineer.