# Step 2: Start and Enable the Virtualization Service

With the tools installed, we need to turn on their engine. The `libvirtd` service is the daemon (background process) that manages the VMs, virtual networks, and storage. Without it, `virt-manager` has nothing to connect to.

# Step 3: Grant Permissions to the Creator

By default, only the root user can manage VMs. To simplify the process and follow security best practices, we add our normal user to the control groups. This gives us the power to create, delete, and manage VMs without needing sudo for every action in `virt-manager`.

**Attention**: This is a crucial step. After running this command, you must log out and log back in to your OS session for the new permissions to take effect.

# Step 4: Obtain the Ouroboros "Seed"

We need the raw material, from which the nodes of our cluster will be created. We will download the installation image of *Rocky Linux 9*.

Go to the official download site: ![OS](https://img.shields.io/badge/Guest_OS-Rocky_Linux_9-green?style=for-the-badge&logo=rockylinux)

Download the Minimal ISO image for the Rocky Linux 9 x86_64 architecture. The "Minimal" image is the professional choice for servers, as it contains only the essential operating system, without graphical interfaces or unnecessary packages. This results in lighter, more secure, and less resource-intensive VMs.

With the environment prepared and the seed in hand, we are ready to begin the creation.
