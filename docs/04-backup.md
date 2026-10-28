# 04 — Backup

Goal: protect the lab VM with Azure Backup using a Recovery Services vault and a simple daily policy.

## Steps

1. **Create a Recovery Services vault** — Create a resource > Recovery Services vault, in `rg-homelab` and the same region as the VM.
2. **Configure backup** — In the vault, choose Backup, set the workload to Azure / Virtual Machine, and select the lab VM from guide 01.
3. **Create a backup policy** — Daily backup at a time the VM might be on (for example early evening), with short retention for a lab (for example 7 days). Short retention keeps costs down while still proving the process.
4. **Run the first backup** — Choose Backup now instead of waiting for the schedule, and watch the job complete under Backup jobs in the vault.
5. **Check it worked** — Under Backup items, confirm the VM shows a recovery point with today's date. Optionally, practise the restore screens up to (but not through) an actual restore, so you know where the options live.

## Why this matters for IT support

"Is it backed up?" is one of the first questions on data-loss tickets. Knowing where backups are configured, how to confirm a recovery point exists, and how retention affects what can be restored is core service desk knowledge.

## Cleanup note

Before deleting the resource group at the very end, stop backup protection on the VM and delete the recovery points, or the vault can block deletion until that is done.
