# CompTIA Linux+ XK0-005/006 Study Guide

A comprehensive study guide for the CompTIA Linux+ certification exam, synthesized from course materials and official exam objectives. Built as a single dark-mode HTML file with full anchor navigation. Compatible with both XK0-005 and XK0-006 exam versions.

🔗 **[View the Study Guide](https://conwilso92.github.io/linux-plus-study-guide)**

---

## Coverage

All 16 lessons mapped to the 5 official exam domains:

| Domain | Weight | Lessons |
|---|---|---|
| System Management | 23% | L01, L02, L04, L05, L06, L07, L08 |
| Services and User Management | 20% | L03, L09 |
| Security | 18% | L04, L11, L12 |
| Automation, Orchestration & Scripting | 17% | L13, L14 |
| Troubleshooting | 22% | L16 |

### What's Inside

- **Lesson 01 — Linux Concepts & Distributions:** Kernel versions, FOSS and open-source licenses (GPL/Apache/Mozilla, copyleft vs permissive), Debian vs RPM distribution families, server architectures (x86/x86_64/AArch64/RISC-V), Filesystem Hierarchy Standard (all 12 FHS directories), GUI components (X11, Wayland, display managers, window managers, GNOME/KDE/Cinnamon), common shells (Bash/Zsh/Ksh), Bash command structure (syntax, case sensitivity, tab completion, history), man pages and built-in documentation
- **Lesson 02 — Boot Process & Installation:** Linux boot sequence (BIOS/UEFI → GRUB2 → kernel/initrd → systemd → default.target → shell), /boot directory files (vmlinuz, initrd/initramfs, grub.cfg), GRUB2 configuration (grub2-install, grub2-mkconfig, /etc/default/grub — never edit grub.cfg directly), PXE network boot, installation types (GUI, server core, bare metal, unattended/kickstart, live media, cloning), partition table types (MBR vs GPT), filesystem types (ext4, XFS, Btrfs, tmpfs, ZFS, VMFS, ReFS)
- **Lesson 03 — Users & Groups:** User config files (/etc/passwd, /etc/shadow, /etc/group field formats), user management (useradd/usermod/userdel/passwd/chage/chsh), password aging, group management (groupadd/groupmod/groupdel/usermod -aG), login commands (lastlog/last/w/id/groups/whoami), privilege escalation (sudo vs su vs su -, visudo, /etc/sudoers syntax), PolicyKit/pkexec
- **Lesson 04 — Implementing File Management:** Absolute vs relative paths (/, .., ~, .), essential file commands (ls/cd/pwd/tree/touch/mkdir/rmdir/cp/mv/rm/cat/less/more/head/tail/grep/find/locate/updatedb/which/stat/file/wc/sort/uniq/cut/awk/sed/df/du), hard links vs symbolic links (inode distinction, ln vs ln -s), command chaining operators (pipe, semicolon, &&, ||, !), I/O redirection (>, >>, <, 2>, /dev/null, tee, xargs), permissions and ACLs reference (chmod octal/symbolic, chown, SUID/SGID/sticky bit, chattr immutable flag, getfacl/setfacl)
- **Lesson 05 — Authoring Text Files:** Vim three modes (Command/Insert/Execute — ESC, i, :), Vim command mode navigation (gg/G, dd, /pattern, split screen), nano shortcuts (Ctrl+O/S/X/A/E, Alt keys), Gedit GUI editor, tar (create/extract/list options: -c/-x/-t/-v/-f/-r/-z/-j/-J), gzip/bzip2/xz/zip/cpio/dd/rsync, file integrity checking (md5sum/sha256sum/sha512sum)
- **Lesson 06 — Package Management:** RPM (rpm -ivh/-e/-qa/-qi), YUM (install/remove/update/list/info), DNF (default for RHEL 8+), repository config (/etc/yum.repos.d/, yum repolist), dpkg (-i/-r/-l/-s), APT (two-step: apt update then apt upgrade), APT repo config (/etc/apt/sources.list), Zypper (SUSE), language-specific managers (pip/cargo/npm), compiling from source (./configure → make → make install, GCC), wget vs curl distinction, Snaps/Flatpak/AppImage sandboxed packages
- **Lesson 07 — Storage Administration:** Partitioning tools (fdisk/gdisk/parted/partprobe/lsblk/blkid/growpart), filesystem tools (mkfs.ext4/fsck/e2label/resize2fs/tune2fs/dumpe2fs/xfs_repair/xfs_growfs), mounting (/etc/fstab six fields, /etc/mtab, /proc/mounts, autofs, mount options: ro/rw/noexec/nosuid/nodev/noatime/nofail), NFS and SMB/Samba network mounts, LVM full command set (pvcreate/vgcreate/lvcreate and all display/remove/resize variants), RAID (mdadm, /proc/mdstat), LUKS/cryptsetup encryption, disk quotas (usrquota/grpquota in fstab), iostat/ioping/fio performance tools
- **Lesson 08 — Devices, Processes & Kernel:** Device files (/dev/null, /dev/zero, /dev/urandom, block vs character devices, udev), hardware tools (lscpu/lsmem/lspci/lsusb/hwinfo/dmidecode/dmesg, /proc/cpuinfo, /proc/meminfo), process management (PID, process states — running/sleeping/stopped/zombie, ps/top/htop/pgrep/pidof/kill/killall/pstree/lsof/sar/uptime), job control (Ctrl+Z/C/D, fg/bg, jobs, nice/renice), memory and swap (free/vmstat, mkswap/swapon/swapoff, OOM killer), kernel modules (lsmod/modinfo/insmod/rmmod/modprobe/depmod), sysctl, uname -r/-a
- **Lesson 09 — Services & Daemons:** systemd vs SysVinit comparison (parallel vs sequential, unit files vs init scripts), SysVinit runlevels (1=single user, 3=CLI, 5=GUI), systemctl commands (status/start/stop/restart/reload/enable/disable/mask/get-default/set-default/list-units), unit file types (.service/.target/.timer/.mount/.socket), rsyslog vs journald, syslog severity levels 0–7 (mnemonic: Every Awesome Cat Eventually Wins Nice Indoor Dinners), log file locations by distro family, cron (crontab -e, five-field format), at command, service config files and ports (SSH 22, NTP 123, NFS 111+2049, Apache 80, CUPS 631, rsyslog 514)
- **Lesson 10 — Network Configuration:** ip vs ifconfig, NetworkManager (nmcli/nmtui/nmgui), Netplan (netplan apply/try/status, /etc/netplan/), network config files (/etc/hosts, /etc/resolv.conf, /etc/nsswitch.conf), hostnamectl, SSH key-based authentication (ssh-keygen, ssh-copy-id), ethtool, network diagnostic tools (ping/ping6, traceroute/tracepath, mtr, nslookup/dig/host/whois/resolvectl, arp, ss/netstat, nmap, iftop, iperf3, nc, scp/sftp/rsync)
- **Lesson 11 — Network Security & Firewalls:** iptables vs nftables vs firewalld vs UFW comparison, firewalld zones and firewall-cmd commands (--get-zones, --list-all, --add-service, --remove-port, --reload), network monitoring (tcpdump with examples, Wireshark, Nmap/Zenmap, netstat/ss/lsof -i, mtr), firewall selection criteria, common firewall troubleshooting
- **Lesson 12 — Cryptography & Identity Management:** Symmetric vs asymmetric encryption, public key encryption vs private key signing (confidentiality vs non-repudiation), PKI lifecycle (enrollment → issue → use → expiration/revocation), TLS/HTTPS and digital certificates, md5sum/sha256sum integrity commands, SSSD (connects Linux to AD/LDAP), LDAP authentication, PAM framework (/etc/pam.d/, password complexity, account lockout, MFA modules), server hardening checklist (disable root SSH, key-based auth only, firewall, SELinux/AppArmor, audit logging)
- **Lesson 13 — Shell Scripting:** Script basics (shebang #!/bin/bash, comments #, chmod +x, exit codes, echo $?), variables (VAR=value, $VAR, export), common environment variables ($PATH/$HOME/$USER/$SHELL/$HOSTNAME/$PS1/$DISPLAY), shell config files (.bashrc/.bash_profile/.profile), I/O redirection and here docs, conditionals (if/if-else/case/test), loops (while/until/for), comparison operators (-eq/-ne/-lt/-gt/==/!= /-z/-n/-f/-d/&&/||), useful commands (echo/read/exec/source/alias/test/sed/awk), cron scheduling from scripts
- **Lesson 14 — Infrastructure as Code & DevOps:** Automation vs orchestration distinction, configuration management (Ansible — agentless/YAML/SSH, Puppet — modules/agentless, Chef — agent-based/Ruby, SaltStack — both/Python, Terraform — infrastructure provisioning/HCL), Git commands (clone/add/commit/status/push/pull/log/branch), DevOps goals and CI/CD use cases, IaC benefits (version control, consistent configs, fewer errors), JSON vs YAML comparison
- **Lesson 15 — Containers & Virtualization:** VMs vs containers comparison table (isolation, OS, size, startup, persistence), Docker commands (pull/images/run/ps/container start-stop-restart-ls/build), Dockerfile, container registries (public/private, Docker Hub), persistent storage for stateless containers, Kubernetes (pods, sidecars, orchestration), Linux hypervisors (KVM/QEMU), virsh/virt-install CLI tools, VMM GUI, Type 1 vs Type 2 hypervisors, VirtualBox/VMware/Hyper-V
- **Lesson 16 — Troubleshooting:** CompTIA 7-step methodology (Identify → Theory → Test → Plan → Implement → Verify → Document), hardware/storage problems (SMART failures with smartctl, memory errors, zombie processes, high CPU, filesystem corruption, kernel panic), OS troubleshooting (login failures, file access issues, service failures, disk full, file integrity with rpm -V, slow performance, clock skew), network troubleshooting sequential steps (physical → IP config → gateway → remote IP → DNS → traceroute → tcpdump), key troubleshooting commands quick reference (journalctl -xe, dmesg, systemctl --failed, df/free, ss -tuln, /proc/mdstat, rpm -V)

---

## Related Study Tools

Part of a broader CompTIA certification study toolkit:

| Repo | Description |
|---|---|
| [CompTia-core1-flashcards](https://github.com/conwilso92/CompTia-core1-flashcards) | A+ Core 1 interactive flashcard app |
| [CompTia-core2-flashcards](https://github.com/conwilso92/CompTia-core2-flashcards) | A+ Core 2 interactive flashcard app |
| [network-plus-flashcards](https://github.com/conwilso92/network-plus-flashcards) | Network+ interactive flashcard app |
| [network-plus-study-guide](https://github.com/conwilso92/network-plus-study-guide) | Network+ N10-009 comprehensive study guide |
| [server-plus-study-guide](https://github.com/conwilso92/server-plus-study-guide) | Server+ SK0-005 comprehensive study guide |
| [security-plus-study-guide](https://github.com/conwilso92/security-plus-study-guide) | Security+ SY0-701 comprehensive study guide |
| [homelab](https://github.com/conwilso92/homelab) | Homelab documentation and configs |

---

## About

Built while studying for the CompTIA Linux+ certification at Star V Learning Centers, Jacksonville, FL. Materials synthesized from course slide decks (XK0-005) and the official XK0-006 exam objectives.

**Certifications:** CompTIA A+ (Core 1 & Core 2 passed) · Server+ (passed) · Network+ (in progress) · Security+ (in progress) · Linux+ (in progress)
