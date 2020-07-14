# underfs-bos

This repository contains extensions to core [Alluxio](https://github.com/Alluxio/alluxio).

BOS under storage implementation accessing BOS using the `bos://` scheme.

### build

```bash
mvn package
```

### Deploy

```bash
./bin/alluxio extensions install <path>/alluxio-underfs-bos-<version>.jar
```

### Run Under Storage Contract Tests

The following runs tests to verify that the under storage satisfies the contract with Alluxio.

```bash
./bin/alluxio runUfsTests --path obs://<bucket> -Dfs.obs.accessKey=<access_key> -Dfs.obs.secretKey=<secret_key> -Dfs.obs.endpoint=<endpoint>
```

### Mount

```bash
./bin/alluxio fs mount /mnt/obs obs://<bucket>
```
