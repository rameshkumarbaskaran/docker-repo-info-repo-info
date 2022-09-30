## `nats:scratch`

```console
$ docker pull nats@sha256:a225a6051cf2cf25b3e018336e8a5b163deac67f394454772752ab082e732d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:73a511425369d8e883fc5784023028b7ed02c252e6db030e776b2e6a76bb90ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4907513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3ba31eb02c938f2ab28c2b60358ef903503ce4a2fb5e2df6f4714d04e74619`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 30 Sep 2022 00:25:01 GMT
COPY file:ef7d265008705c7f8da964d29a2883d21303aab4d4520c3327ca6ce57348e137 in /nats-server 
# Fri, 30 Sep 2022 00:25:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 30 Sep 2022 00:25:01 GMT
EXPOSE 4222 6222 8222
# Fri, 30 Sep 2022 00:25:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 30 Sep 2022 00:25:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 30 Sep 2022 00:25:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:325d5a714be1f0303eebb8d34c9b23e1b15c5e7e46eb29d0f90511112fb86894`  
		Last Modified: Fri, 30 Sep 2022 00:25:50 GMT  
		Size: 4.9 MB (4907005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b03a363308e84c4fc60d5ac2d5b9374e811456edecdb1e302e59198bfb1ca4`  
		Last Modified: Fri, 30 Sep 2022 00:25:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:22be654fd606d7db5e28383ce35794c881f25b77908c6f981c2442b117d7df19
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4671534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eeeee00c7520737eb3766018dde7f3dd63c971938d98ff49cca225f0e6c6990`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 30 Sep 2022 00:15:17 GMT
COPY file:2de52eed8721a4ef1e4c8adb2f046a7ffa8e689d614c704b329ef2bafc7dfe5c in /nats-server 
# Fri, 30 Sep 2022 00:15:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 30 Sep 2022 00:15:17 GMT
EXPOSE 4222 6222 8222
# Fri, 30 Sep 2022 00:15:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 30 Sep 2022 00:15:18 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 30 Sep 2022 00:15:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:948e55d9b8c745ce1f9007c64a6da65d66c0d554fa7e5808a04081a1d0754a6c`  
		Last Modified: Fri, 30 Sep 2022 00:16:49 GMT  
		Size: 4.7 MB (4671025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bdee3fcf17688810034aff56b746397e799579ff11654f2a2ec59274a9e161`  
		Last Modified: Fri, 30 Sep 2022 00:16:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:03a39590b94ba73f75c39970947a3ff276c7f37d7e6e8009ccf780251f6cbc81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4660097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35ae12fca7c133fb2e99616ac3d87777680804b3654472e9c4d78d28db4e965`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:8333f5a10c97b92118357725370604074ebcfef54b0d6e7d818b8a5280ac8fee in /nats-server 
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:58:10 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:58:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:131d7d99719c2d3afa300226a95a811f986eb26f05d0aa3bd08fda92824f90a7`  
		Last Modified: Thu, 22 Sep 2022 23:59:35 GMT  
		Size: 4.7 MB (4659588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b4198acf76381af038bfd14e9332c1ccd3a7235889f327c2d387fbd44b1b3`  
		Last Modified: Thu, 22 Sep 2022 23:59:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6d0d5cfcf4b908ca419719473183dd4000ebe2e77e9fb1088f51f2195324d865
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4495540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7069cf895c76381ff91ad174ed58ca07743ca741317f4a2c20ea3b1f1bae44ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 30 Sep 2022 01:50:11 GMT
COPY file:06300839e6ae56288247488999d2e96ee71c9bb64453bfa88faa4cbfc85a23e2 in /nats-server 
# Fri, 30 Sep 2022 01:50:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 30 Sep 2022 01:50:12 GMT
EXPOSE 4222 6222 8222
# Fri, 30 Sep 2022 01:50:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 30 Sep 2022 01:50:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 30 Sep 2022 01:50:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71fcb6de35d4d1378bd805b642a59de493c8957d351b1f521d05492db21c54d6`  
		Last Modified: Fri, 30 Sep 2022 01:51:31 GMT  
		Size: 4.5 MB (4495032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3be89d1242837970f7157774c5188f9046677dfb8c676155f7b2d268758d504`  
		Last Modified: Fri, 30 Sep 2022 01:51:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
