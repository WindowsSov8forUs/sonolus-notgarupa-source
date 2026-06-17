# sonolus-notgarupa-source

This repository stores the `source/` resource tree through Git LFS and publishes versioned resource archives through GitHub Releases.

Release archives are generated as:

```text
sonolus-notgarupa-source.tar.gz
└── source/
```

GitHub Release assets are split into parts smaller than 2 GiB:

```text
sonolus-notgarupa-source.tar.gz.part-000
sonolus-notgarupa-source.tar.gz.part-001
sonolus-notgarupa-source.tar.gz.sha256
sonolus-notgarupa-source.tar.gz.parts.sha256
```

To restore on Linux:

```bash
cat sonolus-notgarupa-source.tar.gz.part-* > sonolus-notgarupa-source.tar.gz
sha256sum -c sonolus-notgarupa-source.tar.gz.sha256
tar -xzf sonolus-notgarupa-source.tar.gz
```
