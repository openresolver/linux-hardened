# Linux-Hardened Rebase Fork

This repository is my personal fork for **rebasing the linux-hardened patches onto clean upstream Linux stable releases**. Its primary purpose is to maintain a rolling rebase for **all point releases**, including one LTS release (6.12), and to generate patches used for building `.deb` packages in my hardened-kernel project.

## Purpose

- Keep a personal rebase of linux-hardened patches up-to-date with every upstream point release.
- Generate a patch for inspection or application elsewhere.
- Serve as the source for building **GPG-signed hardened kernel packages** in my other repository.

> ⚠️ This fork does **not preserve history**. The goal is to maintain a rolling branch for each point release for reproducible builds, rather than mirroring the original linux-hardened history.

## How This Repo Works

1. Track a linux-hardened branch for a given upstream release series.
2. Rebase all linux-hardened commits onto the corresponding clean upstream kernel tag (`vX.Y.Z`).
3. Use the resulting branch to generate a patch via `git diff`.
4. Apply that patch in my build automation workflow to produce `.deb` packages.

**PLEASE NOTE**: I have started to build the patch with `git format-patch` to make life easier for conflicts, etc... Please use `git am` to apply the patch from this fork.


## For Ready-to-Use Builds

If you are **just looking for the patched source** or a **premade, GPG-signed `.deb` kernel**, please visit the [`hardened-kernel`](https://github.com/openresolver/hardened-kernel) repository on my profile. Please note, the "hardened-kernel" repo contains a custom patch - if you would simply like to use the linux-hardened source, you may `git clone` the appropriate branch from here and you will not need to apply the linux-hardened patch. Configs can be found on my "hardened-kernel" repo (server and desktop variants) and may eventually be moved to their own repo for version control.

---

This fork exists purely for maintaining a **personal, point-release-aligned rebase workflow** to support my kernel builds. All patches and branch updates are created, tagged, and pushed here for traceability and reproducibility.

Credit to: https://github.com/anthraxx/linux-hardened
