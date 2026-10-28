# 03 — Azure Files Share

Goal: create a cloud file share and map it as a drive from Windows, like the shared drives users ask the service desk about.

## Steps

1. **Create a storage account** — Create a resource > Storage account, in `rg-homelab`. For learning, choose standard performance and locally redundant storage (the cheapest options).
2. **Create a file share** — Inside the storage account, open File shares > New file share. Give it a name like `labshare` and a small quota (for example 5 GB).
3. **Get the connect details** — Select the share and choose Connect. Azure shows a Windows connection script/command that includes the storage account key.
   - Security note: that key is a secret. Run it on your own PC only — never paste it into this repo, a ticket, or chat.
4. **Map the drive** — Run the connection command in PowerShell on your Windows PC, then check File Explorer: the share appears as a mapped drive.
5. **Check it worked** — Create a test text file on the mapped drive, then view the share in the portal to confirm the file is listed there too.

## Troubleshooting notes (the Tier 1 view)

- Mapping fails with an access error: check the key was copied completely and the PC can reach the internet.
- Port note: Azure Files uses SMB on port 445. Some home/internet providers block it; if mapping fails on one network, test from another before assuming the share is broken.

## Cleanup note

Delete the test files, then the share (or the whole storage account at final cleanup) so storage charges stop.
