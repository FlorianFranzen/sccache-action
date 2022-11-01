sccache for GitHub Actions - speedup your Rust project build
============================================================

**This is a fork of [visvirial/sccache-action](https://github.com/visvirial/sccache-action) with the sole purpose of [using Node.js 16 instead of 12](https://github.com/visvirial/sccache-action/pull/2) in anticipation of the [removal of Node.js 12 support](https://github.blog/changelog/2022-09-22-github-actions-all-actions-will-begin-running-on-node16-instead-of-node12/) from GitHub Actions.**  

This repository provides GitHub Actions which enables projects to cache the compiled ouotput using
[sccache](https://github.com/mozilla/sccache).

Usage
-----

```yaml
- name: Configure sccache
  uses: FlorianFranzen/sccache-action@v2
  with:
    # Optional
    cache-key: sccache-ubuntu-latest
    # Optional
    release-name: latest
    # Optional
    arch: x86_64-unknown-linux-musl
```

- The `release-name` parameter is the version name listed in [sccache's release page](https://github.com/mozilla/sccache/releases).
- The `arch` parameter is the string included in the binary release `.tar.gz`. For ubuntu, use "x86\_64-unknown-linux-musl".
