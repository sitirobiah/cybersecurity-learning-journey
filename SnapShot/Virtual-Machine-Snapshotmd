# Virtual Machine Snapshots — Kali Linux (VirtualBox)

## `1. Overview`

> This documentation covers the use of snapshots in Oracle VM VirtualBox with Kali Linux.
>
> A snapshot captures the state of a virtual machine at a specific point in time. It can preserve the system's configuration, installed tools, and current state.
>
> Snapshots are useful in cybersecurity labs because they allow me to experiment with system configurations and security tools while keeping a recovery point available if something goes wrong.

## `2. Creating a Snapshot`

### `Step 1: Ensure the VM Is Stable`

> Before creating a snapshot, it is recommended to shut down the virtual machine properly. This helps ensure a consistent system state.
>
> VirtualBox also supports snapshots while a VM is running, but the captured state may include its current memory state.

### `Step 2: Open Snapshot Manager`

> 1. Open Oracle VM VirtualBox.
> 2. Select the Kali Linux virtual machine.
> 3. Open the **Snapshots** tab.

### `Step 3: Take a Snapshot`

> 1. Click **Take** (the camera icon).
> 2. Enter a clear and descriptive snapshot name.
> 3. Add a description if needed.
> 4. Confirm the action to create the snapshot.

### `Step 4: Use Clear Naming Conventions`

> Descriptive names make snapshots easier to identify and manage.
>
> Examples:
>
> - `Clean-Install`
> - `Before-System-Update`
> - `Before-Installing-Tools`
> - `Pre-Pentest-Lab`

## `3. Restoring a Snapshot`

### `Step 1: Open Snapshot Manager`

> Open VirtualBox, select the Kali Linux virtual machine, and navigate to the **Snapshots** tab.

### `Step 2: Select a Snapshot`

> Select the snapshot you want to restore. Check its name and description to ensure you choose the correct recovery point.

### `Step 3: Restore the Snapshot`

> 1. Click **Restore**.
> 2. Review the confirmation prompt.
> 3. Choose whether to save the current VM state as a new snapshot before restoring, if this option is available.
>
> Select **Yes** if you want to preserve the current state. Select **No** if you do not need to keep it.
>
> Restoring a snapshot returns the VM to the selected state. Changes made after that snapshot may no longer be available in the restored VM.

## `4. Important Considerations`

> - Use clear and consistent names for snapshots.
> - Create snapshots before risky system changes.
> - Avoid keeping unnecessary snapshots because they can consume significant disk space.
> - Snapshots may include virtual machine memory when created from a running VM.
> - Snapshots are not a replacement for independent backups of important files.
> - Verify the selected snapshot before restoring it.

## `5. When I Use Snapshots`

> I use snapshots as recovery points before making significant changes to my Kali Linux environment.
>
> Common use cases include:
>
> - Before installing new tools.
> - Before performing system updates.
> - Before penetration testing labs.
> - Before changing network or system configurations.
> - Before experimenting with unfamiliar commands or settings.

## `6. Benefits of Snapshots in Cybersecurity Labs`

> **Safe Experimentation**
>
> Snapshots allow me to test tools and configurations in a controlled virtual environment.
>
> **Quick Recovery**
>
> I can return to a previous system state when an experiment causes unexpected problems.
>
> **Time Efficiency**
>
> Restoring a snapshot can save time compared with rebuilding the virtual machine from scratch.
>
> **Consistent Learning Environment**
>
> Snapshots help me maintain a known system state for different cybersecurity exercises.

## `7. Conclusion`

> Using snapshots in VirtualBox is a useful practice when learning cybersecurity with Kali Linux.
>
> By creating recovery points before major changes, I can experiment with system configurations, practice security tools, and recover from mistakes more efficiently.
>
> This is part of my ongoing effort to build a safer and more organized cybersecurity lab environment.
