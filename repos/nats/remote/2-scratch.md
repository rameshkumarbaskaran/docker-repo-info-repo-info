## `nats:2-scratch`

```console
$ docker pull nats@sha256:3208778cf6c64114c84d0227bfd6fb282f1ba86b85f25c46c410c9e97b3a33ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:cf96338e314ee46e307626e8936dc31b9ef7c67e299b29b7753896d11b52fe8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5455cadbb1bd4919947f5a918491add0f2a8fe5d9aa4a801ca79a4ac8fb308f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:26:10 GMT
COPY file:975a38b1520c81a5e1d0876325548b4aefe0036b6deee1ae7ee20db6abbcc080 in /nats-server 
# Mon, 07 Aug 2023 19:26:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 07 Aug 2023 19:26:11 GMT
EXPOSE 4222 6222 8222
# Mon, 07 Aug 2023 19:26:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 07 Aug 2023 19:26:11 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 07 Aug 2023 19:26:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc02d5ba29398595681917073dcd141022b8ad8d0da9a18b6f5752e56c86ceea`  
		Last Modified: Mon, 07 Aug 2023 19:26:56 GMT  
		Size: 5.2 MB (5169747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9457cd0af5e7125dfe4a44e1d6d003e2bdaf42da9d1c5f7b313069a145e639`  
		Last Modified: Mon, 07 Aug 2023 19:26:55 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:3a3792aaaf193e57879f3594e95501c1372bd2a537965db2bc68fd85c13b8cb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966d4a644152a12918ae66827a94561e477b28d10bd2698612566a5c989612f1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:50:31 GMT
COPY file:447be8988a65ae095af689a396d155107ebc910fe545508c6e6af6f1c2d2c4d4 in /nats-server 
# Mon, 07 Aug 2023 19:50:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 07 Aug 2023 19:50:31 GMT
EXPOSE 4222 6222 8222
# Mon, 07 Aug 2023 19:50:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 07 Aug 2023 19:50:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 07 Aug 2023 19:50:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:590d3f4a49d783a9889465cc7862cf43dc4d3a60e0fb075544618efee1ef93e1`  
		Last Modified: Mon, 07 Aug 2023 19:51:13 GMT  
		Size: 4.9 MB (4932022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901e46e20099bb53f1d1b41e9f1cbf04d9af77173e45873723bd9d7825fbbcf0`  
		Last Modified: Mon, 07 Aug 2023 19:51:12 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:3be04f93d99a8e23e99fff2608d9c0d76a4ee2c9c301441f57a2d0b9225c16e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec722342be0e9d946cb8ac26674a30ff2854116e2e8e1ba75461b3f90d97ecc8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:32 GMT
COPY file:a28d4beb7d3acaa71be2e58ce3a707a2f5be041842f8a1e4eb4c54dd72e865eb in /nats-server 
# Mon, 07 Aug 2023 20:16:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 07 Aug 2023 20:16:33 GMT
EXPOSE 4222 6222 8222
# Mon, 07 Aug 2023 20:16:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 07 Aug 2023 20:16:33 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 07 Aug 2023 20:16:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68043f4483bff82380b8666c025686881f5483ff754784192f65aa4ec9b662fe`  
		Last Modified: Mon, 07 Aug 2023 20:17:27 GMT  
		Size: 4.9 MB (4924065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0443d8f0ff2c43f481bd49043e2c13423203b3a99754a3baff7df20850bf0e56`  
		Last Modified: Mon, 07 Aug 2023 20:17:26 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:24cb726cdaa647f5307f6d5fa448b299535141c96367b79636f23597407b5071
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4734399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2f013bc2559b3a905b049fd4b09738b17a4c87d62bed5a1830c6a6e13b1cda`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:44:14 GMT
COPY file:815b9c4a7d715138f02171cd656c9e8dc6d80e72107c92661c99f6dd24ae2721 in /nats-server 
# Mon, 07 Aug 2023 19:44:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 07 Aug 2023 19:44:14 GMT
EXPOSE 4222 6222 8222
# Mon, 07 Aug 2023 19:44:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 07 Aug 2023 19:44:14 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 07 Aug 2023 19:44:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:07116324214b64589e3a471932fe7f6b892068a7cd9cf9bb72a8ea25f8a92200`  
		Last Modified: Mon, 07 Aug 2023 19:44:57 GMT  
		Size: 4.7 MB (4733893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615975e7d25e46607f561d13c4c244d070bb41701a0ac2103df98dcb33e8a4eb`  
		Last Modified: Mon, 07 Aug 2023 19:44:56 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
