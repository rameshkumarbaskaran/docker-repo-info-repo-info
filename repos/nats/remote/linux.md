## `nats:linux`

```console
$ docker pull nats@sha256:464514526a41389cb8eba22f4222d1e44dbfbc570acdb09a32d557c9b9955a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:0008930d6f49b1c3a706f5e751756e25faa913eb0d24a4d1a3cc7111995c2cc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4907907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae8e0e40e5d6a88833150b7613d8c2af98aeeefd0da6dca3100722e12b19571`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:3f7f7d06c5f77e836d502f53de29b2d7a2e80853d13b4d9c75b6bda16857761b in /nats-server 
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:25:42 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:25:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d6d85ead114c982a0357d6002a45433e3f39494cdc0f3cc920d804a45cae35ee`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 4.9 MB (4907400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60865ecae70fb12a59e8579974bc3d65a97b7e84fcd8fe6445d275320879ea5`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:8f0d092d06af2710b06354ee677b81f10f6251a0e8efb0421d8d3f86d1000677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4675550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbbb2f82c0829a2a87cd2ea49c73284638f5861690c6b230951c2b6ca549d06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:65c01e5e1e16c3f3b2d7df9541699c9363f45a0a991482d97d24193d7e1bb29a in /nats-server 
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:49:34 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4db83ef5484b7db61a63b554c60491f4a902ca94cce6b612d3aa32aa92888ec6`  
		Last Modified: Tue, 11 Oct 2022 17:51:01 GMT  
		Size: 4.7 MB (4675041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb93982fc62459387f27a9bde43633a8c758cec8404805cd92613cad4436f4d`  
		Last Modified: Tue, 11 Oct 2022 17:51:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:14a5c2b109967d3adb793cd0ab698648bc10a969bff48575c619a09e6e5ad232
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4664630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7884a65e2ecb2f9f6974f0b17533ba58e8845ff3d4e2f58f62762e8980ddbc5b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:34c532093a5dbef0c1af4a815d6c675cdb6125f12b5f44a7f2b662696b571b90 in /nats-server 
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:58:03 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:58:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:58:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:58:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:03af04ed4c28e4580e7b4c3a5ea1484aae440ba7d2dd4e9a656d77d82dd54b98`  
		Last Modified: Tue, 11 Oct 2022 17:59:30 GMT  
		Size: 4.7 MB (4664122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7148a4d5aff61489f0013cd47ecaf37fcf9a49f79472e42dd389601319be9422`  
		Last Modified: Tue, 11 Oct 2022 17:59:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc4ef43bc1c7b49a3550af75cf1940321e1f5565da18e0f178bde6acd5a36bdd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f962526ab017817241bd3fbee96aff03c8852436cf5bcdc0a58b5e3fe5a09d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:40:23 GMT
COPY file:bc86ca7535653a0512f71a856c462b418bdf59420e8fa4ca2103093ecb5bf96e in /nats-server 
# Tue, 11 Oct 2022 17:40:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:40:24 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:40:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:40:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a147f8167144f46b22ee755fdae458d8e5b2fa34cb9a04d5b0393033d9044e08`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 4.5 MB (4497202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720a4acb8f391823b838f963c0b4de61247a73c4721a3224829968b7b7c0e4c`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
