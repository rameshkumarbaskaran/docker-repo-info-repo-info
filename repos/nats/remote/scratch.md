## `nats:scratch`

```console
$ docker pull nats@sha256:8371b3bfc468a2294efb247531c2252c592398a98b574c2e81268d8c7f865d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:d7a57514cf7a0949ab8e63985f040f1fbaa01aa70aa50d8485f796a9a8dead08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd1a8b681814e86af7f1b07aa7178abd74163b5101ad1f855420c25d4afae5e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:19:59 GMT
COPY file:a3e4cfa40e3f87cbc1a2427fe9e77a182eed251b7a2f3037b894ac919acda56d in /nats-server 
# Thu, 18 May 2023 21:19:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:19:59 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:19:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:19:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e7f86c5b152db9b1815749cb2d298d36014c2905070ae66128b67029b4b31780`  
		Last Modified: Thu, 18 May 2023 21:20:38 GMT  
		Size: 5.1 MB (5116621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ce2c40f365197112db5bf1e3ed9b09b631da2058b456f99a50a5890fdda44`  
		Last Modified: Thu, 18 May 2023 21:20:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b93fec72f4aff1d673fd6ead1e244e694e4919368e246cc29e0d7d120e59ed77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4881364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab660f64e3aad0f8f74d3a08909fe9013543eb07b61a9f8c6862b5db7d457d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:49:31 GMT
COPY file:6e54deb4ba87d6bff1f230123320fc7c9eee49d9a7456888efc872a22b9bd9ba in /nats-server 
# Thu, 18 May 2023 21:49:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:49:32 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:49:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41da3c5a1624a52c52a67beaa7b94c8c85a26f53b81e82e6dc05ae661adfebc1`  
		Last Modified: Thu, 18 May 2023 21:50:09 GMT  
		Size: 4.9 MB (4880856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df51ab38f5ab934d23f3b5429532106ef6baa2f64572f07ce9e5718e3f27374b`  
		Last Modified: Thu, 18 May 2023 21:50:08 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:94bf4a62f52fd647adb621d2d584e9c48aea06b124fb81cd59afed50252071bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4874864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8b8de1397d0af96648a1d02610dc54a066633c75eb548fc6be7e0d15497c3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:57:50 GMT
COPY file:31e26234e2abf1c16cd5869033f07320118e6dc458af341f37a27a3d12ffbc65 in /nats-server 
# Thu, 18 May 2023 21:57:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b6209c6f59228d4816baef6c05a38f68693937e6c86969581c57a1c7b68ccb40`  
		Last Modified: Thu, 18 May 2023 21:58:28 GMT  
		Size: 4.9 MB (4874355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69c5a4696da201d78c2dae749a6bce01c3a924afbdfa7e87c6797b8db238d4d`  
		Last Modified: Thu, 18 May 2023 21:58:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c4a7f923864c688cb5cc324df620960febd829b8d1f7074e4af3805caf5d5ceb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4685324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c4d84878abd37db0a2ba71386d26a2aaea2e989b4c3fc5f5930194da2e95c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:39:47 GMT
COPY file:b639df8cca07607378826468450a651a2cab9fb1be759ac266bf356bbfa2ac8c in /nats-server 
# Thu, 18 May 2023 21:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:39:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:39:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:39:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8e3bc385de2fea9fcd87e3f5b9809c6c133578671c906d0c1df657657c34664`  
		Last Modified: Thu, 18 May 2023 21:40:23 GMT  
		Size: 4.7 MB (4684816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d538df43ba01d77f25e465d3cce0829b2fbcf2a5ff131e1a42fda47b5c6c64`  
		Last Modified: Thu, 18 May 2023 21:40:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
