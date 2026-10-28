# 05 — Cost Controls

Goal: keep a learning lab close to free. These are the habits I used throughout this build.

## 1. Auto-shutdown on the VM

On the VM page, open Auto-shutdown, turn it on, and set a daily time (for example 19:00) with an email notification. A forgotten running VM is the most common cause of a surprise lab bill.

## 2. Choose small and free where possible

- Pick burstable B-series VM sizes and standard, locally redundant storage for learning.
- Prefer services and tiers included in a free/student subscription, and read the pricing note on each create screen before confirming.
- Keep backup retention short (guide 04 uses 7 days).

## 3. Budgets and alerts

In Cost Management + Billing, create a small monthly budget for the subscription with alerts at 50%, 80%, and 100%. The alert email is your early warning — act on the first one, not the last.

## 4. Stop vs delete — know the difference

- **Stop (deallocate)** the VM when not using it: compute charges stop, the disk still costs a small amount.
- **Delete the resource group** at the end of the lab: removes everything in it (VM, network, storage, vault) in one action. Remember guide 04's note: remove backup protection first or deletion can be blocked.

## 5. Weekly tidy-up checklist

- [ ] VM deallocated or on auto-shutdown
- [ ] No test users or groups left active in Entra ID (guide 02)
- [ ] Test files removed from the file share (guide 03)
- [ ] Cost chart checked for anything unexpected
- [ ] Anything created outside `rg-homelab` noted, so it is not forgotten

## Check it worked

Open Cost Management > Cost analysis and confirm the lab's daily cost drops to near zero on days the VM is deallocated. That graph is the proof the controls are working.
