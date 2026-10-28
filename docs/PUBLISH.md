# Publish full SSHDesk sources

The local ZIP named `sshdesk-git-source.zip` includes an initialized Git repository with all SSHDesk source files, including Electron, Chromium extension, Python Native Messaging Host and documentation.

The GitHub repository already contains an initial README commit. To publish without force-pushing, unpack the archive, then from inside the `sshdesk` folder execute:

```bash
git fetch origin main
git merge origin/main --allow-unrelated-histories -s ours -m "chore: reconcile repository initialization"
git push -u origin main
```

The merge records the existing remote history while retaining the complete local SSHDesk tree. Use Git Credential Manager or your own securely stored GitHub credentials. Do **not** paste Personal Access Tokens into terminal commands or chats.

This is experimental software and is not security-audited or production-tested.
