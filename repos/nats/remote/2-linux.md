## `nats:2-linux`

```console
$ docker pull nats@sha256:c524e7a910ef6343d0106f820f1f00fbde8e639502a97e83c0f5e432d2732516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:1f5fd4c2667baa8706a01a5142ebfc7da4e54b40e836f6023c542e98a05d3633
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5473290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a627248b7b1c4d5c4c34458f79a9a3c8c3a9376ce38d013717a4f7c46e1be7c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 13 Oct 2023 20:20:56 GMT
COPY file:8348bba8fefe594deaff23a8e8d05c5fe8b20634309016cd157744d47b01e751 in /nats-server 
# Fri, 13 Oct 2023 20:20:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 13 Oct 2023 20:20:57 GMT
EXPOSE 4222 6222 8222
# Fri, 13 Oct 2023 20:20:57 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 13 Oct 2023 20:20:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f6c5282fce6f13ac2ac3b630b77fdf0eedb5f5bc51022facee92dfab0158a59`  
		Last Modified: Fri, 13 Oct 2023 20:22:22 GMT  
		Size: 5.5 MB (5472781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edccfbb89f4006d0b4c994aef2a537d6009ce16bd56e9ce65e5c3eb9bafb12bf`  
		Last Modified: Fri, 13 Oct 2023 20:22:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4311525539cb532e2215a0f0e6a97e456bf100aecae9df633068dce84725d3af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5189188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b74620a2c8b938dece7aba41cf3db596039ac4579268f2083d879dc0338e3d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Oct 2023 23:49:30 GMT
COPY file:78bf14fdba87d3f994b59ec64fa5f813ff988f0f91e4929c7aaf33d206d6e4e2 in /nats-server 
# Mon, 09 Oct 2023 23:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 09 Oct 2023 23:49:30 GMT
EXPOSE 4222 6222 8222
# Mon, 09 Oct 2023 23:49:30 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Oct 2023 23:49:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:541bfb4a7866a6fb7234b9fb133b37cc8a1fff7bcf10779570793f66bfa36cc5`  
		Last Modified: Mon, 09 Oct 2023 23:50:25 GMT  
		Size: 5.2 MB (5188681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e9969a228338f491f74c367e86a77a512ae318604d924fa624ef4e9b944a62`  
		Last Modified: Mon, 09 Oct 2023 23:50:24 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:72a048e9abb13148a5588dd1f556af5cf11e91369fd856d21e1b981e2f0f6aec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3f7200638809e9d2ec5971ab53b5a84b4413d7fce360c58f1d7381d739555e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Oct 2023 23:57:51 GMT
COPY file:dfba40eb121bd5821909fe10c59b498aec418c7224d18a7961e71444dc375765 in /nats-server 
# Mon, 09 Oct 2023 23:57:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 09 Oct 2023 23:57:51 GMT
EXPOSE 4222 6222 8222
# Mon, 09 Oct 2023 23:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Oct 2023 23:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c24b02c85cdfcd5bdce9a848ef068ff9e9535a6287fb7a00eb8e39b357c54ad0`  
		Last Modified: Mon, 09 Oct 2023 23:58:40 GMT  
		Size: 5.2 MB (5177978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d844de696d0e40f4aff106f51467e397619526062047fe60f4b692adda3bd736`  
		Last Modified: Mon, 09 Oct 2023 23:58:39 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4b167dea0c683971c7d06db669fbdebf2a8b3c01cb4d229bf5204c8fc6cab7e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5042145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966bdbd5f41b922365e541cf6121d6cf76a4ddb1f9c111e010656f7041d50c1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Oct 2023 23:39:55 GMT
COPY file:c0f257aca3b8b7405bb5549a368de7ae62c806fe4e75e189b405a7ce1f65fa4b in /nats-server 
# Mon, 09 Oct 2023 23:39:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 09 Oct 2023 23:39:55 GMT
EXPOSE 4222 6222 8222
# Mon, 09 Oct 2023 23:39:55 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Oct 2023 23:39:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12032ad6ebd443b7c142112d1df3d64b3deb3a403e0a99764593e5fe7843781b`  
		Last Modified: Mon, 09 Oct 2023 23:40:46 GMT  
		Size: 5.0 MB (5041638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7d34c174da06f5ab9c869a0197e492849a0d80fbf8f038f93e9e1ac634d1f7`  
		Last Modified: Mon, 09 Oct 2023 23:40:45 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
