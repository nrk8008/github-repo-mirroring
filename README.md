# GitHub Repo Mirroring via GitHub Actions (SSH-Based)

This project automates syncing from a source GitHub repository to a target repository using GitHub Actions and SSH authentication.

## 🔧 Features
- Mirrors all changes from `repo-source` to `repo-target`
- Supports file additions, updates, and deletions
- Excludes `.github/workflows/mirror.yml` to avoid recursive triggering
- Uses SSH deploy keys stored securely in GitHub Secrets

## 🛠 Tech Stack
- GitHub Actions
- rsync
- SSH Deploy Keys
- Git

## 📂 Structure
- `.github/workflows/mirror.yml`: GitHub Actions workflow
- README.md: Project overview

## 🔐 Security
- SSH private key stored as GitHub secret
- Public key added as deploy key in target repo with write access

## 🚀 How to Use
1. Generate SSH key pair
2. Add public key to target repo → Deploy Key (write access)
3. Add private key to source repo → GitHub Secret (`SSH_PRIVATE_KEY`)
4. Push changes to `main` branch of source repo
5. Workflow triggers and syncs to target repo
