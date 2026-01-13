# linux-hardened – v6.18.* Rebase Experiment

⚠️ **EXPERIMENTAL – NOT OFFICIAL – DO NOT RELY ON THIS TREE** ⚠️

This branch contains an **experimental, manual rebase** of the
[linux-hardened](https://github.com/anthraxx/linux-hardened) `6.18` patchset
onto the upstream Linux **v6.18.5** release.

This work exists **purely as a learning and comparison exercise** and is **not**
an official linux-hardened release.

---

## ❗ IMPORTANT DISCLAIMER

- **This is NOT an official linux-hardened branch**
- **This is NOT reviewed or endorsed by the linux-hardened maintainers**
- **This may be incomplete, incorrect, or unsafe**
- **DO NOT deploy or rely on this kernel**

👉 **Always use official linux-hardened releases instead**:  
https://github.com/anthraxx/linux-hardened

---

## 📌 What this branch is

- A rebase of linux-hardened `6.18` commits onto Linux **v6.18.5**
- Intended to:
  - Study how linux-hardened patchsets evolve
  - Compare against the eventual official hardened point release
  - Experiment with kernel hardening workflows
- Built for **personal learning and curiosity**

---

## 🚫 What this branch is NOT

- ❌ Not a stable kernel
- ❌ Not security-audited
- ❌ Not suitable for production
- ❌ Not a replacement for linux-hardened

---

## 🔍 Rebase details

- **Upstream base:** Linux v6.18.5
- **Source patchset:** linux-hardened `6.18`
- **Rebase method:** manual git rebase
- **Approximate commit count:** ~102 commits

Note: The upstream `EXTRAVERSION` change is intentionally **not included** and
should be handled manually at build time by using `vim Makefile` and changing the
EXTRAVERSION to something like "-hardened0". If you clone the repo, you'll have to
change the Makefile and manually add back using `git add Makefile`

---

## 📦 Patches

This branch may be used to generate patch files for **comparison only**

## 👉 Credit

All credit for hardening work goes to anthraxx/linux-hardened maintainers and contributors
