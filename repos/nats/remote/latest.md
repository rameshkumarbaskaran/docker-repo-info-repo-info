## `nats:latest`

```console
$ docker pull nats@sha256:a348aeedd60212d689e11948c800444d1d88a8b2bd177c0cd6a8bd55c082facd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3650; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:79830eec98d1dc2f6acd4c63fee41a3434bc47a1b7f31cab9477de1bb3336100
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4922852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce49f767b1c3e8d858ddf7390fb3dad1b4fdebd12784b1fe33719a5a1a7993`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:d13bbefb978757216c59b4e4aba99770a0d4abdac594ab77282fb8cd6b85b588 in /nats-server 
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:35:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:35:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:35:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7692aeb9660d6587db50a4ea4f287699e633f61600a28a2d22092a82846129ce`  
		Last Modified: Thu, 08 Dec 2022 20:36:28 GMT  
		Size: 4.9 MB (4922345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022161875246986f560f72a1c52a359c684e6760487fe8f04a353168edfd2ac7`  
		Last Modified: Thu, 08 Dec 2022 20:36:27 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:24970d929b8d8ecf8887fb00bd92ce687fa3b252218c033614bbc892eec3c380
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4684937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac2c7d543ae2d436c8f9381f98b0bf06c08e5995d33fe8bdebd74699cfc1635`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:00:11 GMT
COPY file:5143a8dee5d00da934937a160852ff57e854ce11c42fdd4828e47d5bb4df42da in /nats-server 
# Thu, 08 Dec 2022 20:00:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:00:12 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:00:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:00:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fedc572ae49bd720399deeb6a36a9250630afd1a477e3c36b0afa73c9106ee50`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 4.7 MB (4684431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8cd5d76c140f074a437a1a67876d7ccd749d332dc6908ccb8fe301cd5dde0a`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:e0e6a65a6d9b16c6fc02bc5eb03804447975e81aab5cb4ef6de5ae0e7b490c54
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2439be95ff20e36b9fc19dd178f16c99ae8deb74465c167849bbff1ae4e66612`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:4c080655f46dbff5713191574af1df195a38d3dc3d3835f7eb875699a8e32d0b in /nats-server 
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:31:19 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:31:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:31:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221d437a3d6581cb4a83aada6c1cd3cb9d173cc07d5d0e9be2c801fb03fa9abe`  
		Last Modified: Thu, 08 Dec 2022 20:32:52 GMT  
		Size: 4.7 MB (4680919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5146fbe1772138448df3c1eb3444c5077d2cdac62bc7b082c112ac5ee4be14b2`  
		Last Modified: Thu, 08 Dec 2022 20:32:51 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:95318d8cd0e5ac24a3070af64056187f97cfb83673bb66a0fd5402f484912bc2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60599b58e21ba05f3bb06c0c373f7f8e213ea6861ad81399a4472fff4a90dbad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:5e130ace514500d49e7ad10785f48a1123d8992953cabcf51a55abf452f854f0 in /nats-server 
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 19:57:18 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:57:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 19:57:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 19:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8935bb735107ae5954afbbd1ce8b5d61ad9a102c82ba176ee5fcc00d437cc63`  
		Last Modified: Thu, 08 Dec 2022 19:58:05 GMT  
		Size: 4.5 MB (4506356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e3d737971cded626be61eca795945c4a04518d6c2dc737dbd7342cac026be`  
		Last Modified: Thu, 08 Dec 2022 19:58:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats@sha256:fc69eebe9e88c4b4b95ac8f1df62d575429a3f4dfd8a0202d3d800169417237b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111706134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052d3f915f0bb8e134494126fbabc015cc06ec4807d264b13fc02440d0893d31`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Wed, 09 Nov 2022 16:47:43 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 08 Dec 2022 20:17:44 GMT
RUN cmd /S /C #(nop) COPY file:8d03b51c4d2105411f3161f01ef7aad45804539a633733d4a8a5eb9f07e4970a in C:\nats-server.exe 
# Thu, 08 Dec 2022 20:17:45 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 08 Dec 2022 20:17:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:17:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 08 Dec 2022 20:17:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6708525607bc7a2985c6a423e6cb63d6175e3ad60d997873c4519fab371772fe`  
		Last Modified: Wed, 09 Nov 2022 16:48:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429112a6e14f23a3eeff9bc07dc613ab0a17f57bddad91d104b23a9cef026438`  
		Last Modified: Thu, 08 Dec 2022 20:18:36 GMT  
		Size: 5.0 MB (4976119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05e93fd22ca6397342e1df6f909c75c4e3bf570717d5e6a0be4d586db85434f`  
		Last Modified: Thu, 08 Dec 2022 20:18:35 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49aac79ae8da7ab4f2f72467554dc97efbbd557e178613cd736a23e71e98c0ab`  
		Last Modified: Thu, 08 Dec 2022 20:18:35 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290244be79a70ceb99ecfcaaecc9e6e92245113c8fb55bb0fdc15061e5efde53`  
		Last Modified: Thu, 08 Dec 2022 20:18:35 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a3bcf86c0fe7de9196df0b8d9216b3c0b6c2fbc1083d8697282cb16d719061`  
		Last Modified: Thu, 08 Dec 2022 20:18:35 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
