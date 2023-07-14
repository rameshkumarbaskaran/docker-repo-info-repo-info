## `nats:linux`

```console
$ docker pull nats@sha256:54beaa3c85e41593c8d7f235ac1ecea3c3dd2eeb63dc2f53e75a8094579ff7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

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

### `nats:linux` - linux; arm variant v6

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

### `nats:linux` - linux; arm variant v7

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

### `nats:linux` - linux; arm64 variant v8

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
