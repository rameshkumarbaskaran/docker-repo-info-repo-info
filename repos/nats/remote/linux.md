## `nats:linux`

```console
$ docker pull nats@sha256:9b9aa89b597057340e5f650e14e5d18d2e0a3015e9e819f278b513731ba89a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:14c9e59858014179012e8927685606b7c0f5f2b1da7604570b33612a269dd91f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5473290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8f8ddb57e634e8b5275f19920ed6ca9267362abaab9efc02cd82dc5c85e902`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 02:39:46 GMT
COPY file:8348bba8fefe594deaff23a8e8d05c5fe8b20634309016cd157744d47b01e751 in /nats-server 
# Sat, 21 Oct 2023 02:39:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 02:39:46 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:39:46 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 02:39:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f6c5282fce6f13ac2ac3b630b77fdf0eedb5f5bc51022facee92dfab0158a59`  
		Last Modified: Fri, 13 Oct 2023 20:22:22 GMT  
		Size: 5.5 MB (5472781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448bddbf3cec75233a72d2ab1e1894e88b0c6d4174c957aa6c72dcb0d21e0318`  
		Last Modified: Sat, 21 Oct 2023 02:40:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:b21a2cf73ec0cc217a3aac6a4f6c59ff1b153e885afcb8f3817c1bebb5891cc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b390cff9226558aafab260dcdb1fde3f9dbcccf23fe00a445a5b077ead4a0c4b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 00:29:30 GMT
COPY file:8dacc397b23c5135d4de7bf3f45ab027ff2c86caa3aad1e15af7be5f04d445ad in /nats-server 
# Sat, 21 Oct 2023 00:29:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 00:29:30 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 00:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:19ec1fbe1f08c131312370f7ea60d44458bc6ab6071134407e6e4ae56aabd35c`  
		Last Modified: Fri, 13 Oct 2023 20:50:56 GMT  
		Size: 5.2 MB (5190079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09507aa79b4534f24fc4278fad2ce0afbefca54c60292f08bf32d5891e891685`  
		Last Modified: Sat, 21 Oct 2023 00:30:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:6ff3c1a07e817b1f578769a295c435ac5567ed963d1eb00c3b3b6ca2c2b3d90e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5181140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db97d66c9797fedaa1557bdfc62ef08481c108ea79d6d7372a103aae9202321`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 00:53:35 GMT
COPY file:7c0c4073772c48f768f2e91bfa31b0c5d556879520ae0ea32fc6935bf412dc00 in /nats-server 
# Sat, 21 Oct 2023 00:53:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 00:53:35 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:53:35 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 00:53:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:31d2c5aa698d33f10bc977a89c17f3061f738bcf64b2a5da150959029f61cf0d`  
		Last Modified: Fri, 13 Oct 2023 20:59:21 GMT  
		Size: 5.2 MB (5180631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c2d1241097295580e2bd3340f11ffd8c8fda3a1c4dc998a6d12a83ca08a631`  
		Last Modified: Sat, 21 Oct 2023 00:54:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8e213d0b22132cd7751ab9f124a755d9a1d24277b0bfa69c66599c4ac88559b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5045078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e91b7fd42507f6e0b27ccf9cf910a829fa558fdf50d47b5366d0c432eed612`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 02:14:08 GMT
COPY file:19248ff038b76e97dd2ecca66b4c7405f937e42b4333f3145ccd80bf7163d961 in /nats-server 
# Sat, 21 Oct 2023 02:14:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 02:14:08 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:14:08 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 02:14:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e53370f26f56fa38d3df795930e6aff84ff23630dcb11457890c5a66f697b145`  
		Last Modified: Fri, 13 Oct 2023 20:42:28 GMT  
		Size: 5.0 MB (5044570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1288b621249b90e483c5249100fde3ba3de8a0ab7b8a3970de56de21c9729172`  
		Last Modified: Sat, 21 Oct 2023 02:15:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
