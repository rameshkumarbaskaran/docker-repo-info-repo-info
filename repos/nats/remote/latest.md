## `nats:latest`

```console
$ docker pull nats@sha256:8e0fb53c305217c0f29f21e8176fce1f4f11648c96543f0970666d8596e2d69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4645; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:700a4b586eb96ff46eef5a949c50297d689f8b31d62ea1ca773dd6895c3f039d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5126531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5907f5a08f299f1dacf051a9fc09fb9189deb2b0dce45877975471766b706954`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:83ff3835bde68ad26982d2ccc535db9982a508facc29fdbcbbfb9675666fbdc6 in /nats-server 
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:29:32 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:29:33 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:29:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67e402a9bce54a5dfde340b14dba6b73ef42a3b94cb337301bf4374e77ec7040`  
		Last Modified: Thu, 13 Jul 2023 22:30:12 GMT  
		Size: 5.1 MB (5126023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a9f6e59497aefb2b8a64f61ee04f476641f2b25c8c62c37e5fdfaab68f8f7e`  
		Last Modified: Thu, 13 Jul 2023 22:30:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:6fd7bfb33bbf19e7ccb75c6ac3fcdc072b6120923fdb4e96e29492a5e7b89289
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4890101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d7fa51b81b0dcfb6ee49a1b74a5881dbf8163021afff101d2002b70686142a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:b5f9cb21b49e06d0ef4d044cf5d2fa6f64bbabb0cfb73701be4fa9d1e7c16c56 in /nats-server 
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 21:49:27 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:505fc4baba759223316e40a0109c61f162bb1d1acafb25bbc8e92b684cd58c5e`  
		Last Modified: Thu, 13 Jul 2023 21:50:07 GMT  
		Size: 4.9 MB (4889594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc06a01182930b7a494867f205f3a02b099200299bffa49031f3085b8952f64`  
		Last Modified: Thu, 13 Jul 2023 21:50:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ec4eab4197d5b340c7bcbbfda1e3bca6ac9874273362a95cb4f58157884759e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab94676f2d9fc59f778cd1526e8664a87db5a1b0741b2053991fb0fb00a2a16a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:53:11 GMT
COPY file:b1a666d296b7b01c216ccd9e1f03715958de83d192993bc8ab769d7998b1703f in /nats-server 
# Thu, 13 Jul 2023 22:53:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:53:12 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:775e6a1e06f337eb4fc74b89e37d008aac2e092d4bfd8d25f944b5b8d257bf8e`  
		Last Modified: Thu, 13 Jul 2023 22:53:52 GMT  
		Size: 4.9 MB (4880250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e8a9e7894a37f644a39457db86f9e94f7b92aadfeac1fd47ee846be3c7eb8f`  
		Last Modified: Thu, 13 Jul 2023 22:53:51 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb5aafaa1c1ada08d1342efaacdbbc72351ea5fa9ed825ec83c84c194a1793aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411f554cbcd46eb35b3ba4cd400a5e29132ded085f6ec4efaccaa6121a464db9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 23:11:18 GMT
COPY file:75a8428ab964e430ddc475b81bfe8411c8a1a8487d06f66b7b2be85ebca4c05f in /nats-server 
# Thu, 13 Jul 2023 23:11:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 23:11:19 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 23:11:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 23:11:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff35e5a1c81a5e14fcb0cddaf7b6bb7a86d01c91297fc204d6f59f81ab699f42`  
		Last Modified: Thu, 13 Jul 2023 23:11:55 GMT  
		Size: 4.7 MB (4694032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ddd8ff8791364717d428b048bce331ac51b1654fac486b5b5d64c7f9a6bd1`  
		Last Modified: Thu, 13 Jul 2023 23:11:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:63c26578744b038b074f43eb6c0b3958667480b48bfe2a74c675fa52295f6767
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109612796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7071df68a96690f5443acb6ef9a47cea84abc3e0dd4a92efaa064a3144b56ed2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Fri, 14 Jul 2023 00:03:16 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:a5074ddde966142308b669c647979e812040bd9a0280cfce51a983385df577ec in C:\nats-server.exe 
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:03:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4bad9bf846d07362d8295a4479f8f2965dfb5934a9a032b335ce3cb086bdf7`  
		Last Modified: Fri, 14 Jul 2023 00:04:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7b0789d7cd0ee38c3d2d6f0d8d4662e4e4f242055fa09752c571e9e0b12b25`  
		Last Modified: Fri, 14 Jul 2023 00:04:05 GMT  
		Size: 5.2 MB (5198141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7714f1d09ea353a9769c79f15345a77c802214a0d24c3ed987cf9bc90fa67933`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4710eb1eae23febe62cd19d1e08fda4c2417972b715e389b5078de0796c915f`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2187cbf833c204e29fc58f360a3c3c572ea7fe8140d088f10f16abeb6666d374`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f146e585d072cd21e48a1fd715a9e5ba5233a54652a5494c2efe8216b210ade`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
