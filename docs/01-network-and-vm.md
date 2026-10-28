# 01 — Virtual Network and Windows Server VM

Goal: one resource group, one virtual network, and one small Windows Server VM you can connect to by Remote Desktop.

## Steps

1. **Create a resource group** — Azure portal > Resource groups > Create. Name it something clear like `rg-homelab`. Pick the region closest to you. Everything in the lab goes in this group so cleanup is one delete at the end.
2. **Create a virtual network** — Create a resource > Virtual network. Attach it to `rg-homelab`, use the default address space (for example `10.0.0.0/16`) and one subnet (`10.0.0.0/24`). For a beginner lab, the defaults are fine.
3. **Create the VM** — Create a resource > Virtual machine:
   - Image: Windows Server (a current Datacenter edition)
   - Size: the smallest burstable size available in your region (for example a B-series size with 2 vCPUs) — enough for learning, much cheaper than standard sizes
   - Administrator account: create a username and a strong password and store them in a password manager, never in this repo
   - Inbound ports: allow RDP (3389) for setup. Note the security point below.
   - Networking: place the VM in the virtual network and subnet from step 2
4. **Connect** — On the VM's Connect page, download the RDP file and sign in with the administrator account from step 3.
5. **Check it worked** — Inside the VM, open Settings > System > About to confirm the Windows Server version, and run `ipconfig` to see it received an address from your subnet range.

## Security note

Leaving RDP open to the whole internet is a real risk. For learning beyond day one, restrict the network security group rule for port 3389 to your own public IP only, and shut the VM down when you are not using it (see guide 05).

## Cleanup note

If you stop here, deallocate the VM (Stop in the portal) so compute charges stop. Storage for the disk still costs a small amount until the resource group is deleted.
