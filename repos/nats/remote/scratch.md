## `nats:scratch`

```console
$ docker pull nats@sha256:e14b590231d5474417f0a53ee7741b26b3a896d1d9bc6f030e1a12081968f650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:e22bfb7fdf9006c8d295782e24a70c2197e340f216b649650ea67288ef841319
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4580124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913890b0a2d48e5c381bcf8b123528904a57150fa69138277620e0ff995dff8b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:3454a426bcdf428c59f748013f6bd917cddf529f8a5032532fee8e7783f2d5e4 in /nats-server 
# Fri, 22 Apr 2022 16:22:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:22:23 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:22:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:22:23 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:22:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:804b81b2249803c39d50d8d9262ec5bdb230411989987b9116527a02dbf021a8`  
		Last Modified: Fri, 22 Apr 2022 16:23:12 GMT  
		Size: 4.6 MB (4579616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebd8666e9d6549b9ab43c6349958c6dbb767c779117f02d727d356e3daaf3d`  
		Last Modified: Fri, 22 Apr 2022 16:23:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:bb39905ea888630c30250ffee5dc2c940c3b95d2a2898b74a7aa139a7007f159
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ce28f90865945806936cfae5ee78d8f2f2598db1ac7086ad1929992f0b3c3a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:50:00 GMT
COPY file:3de61978a9e8a2b166b752a33898d5f146479cdb1ce6ed9df10727fe98f55f51 in /nats-server 
# Fri, 22 Apr 2022 16:50:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:50:01 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:50:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:50:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:50:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a90933979a2530bf92d8ed3112add5a8debe6da238f9becc07b90b414323e402`  
		Last Modified: Fri, 22 Apr 2022 16:52:22 GMT  
		Size: 4.2 MB (4237584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd95754400d2efb409a2eeed76406fade3b92c929c465f6a5c2189183a4e072`  
		Last Modified: Fri, 22 Apr 2022 16:52:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:3c8ce819721153ec2da8805ad16a87b94081820a66038d13707555ff80b1ca13
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4230403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2c0a899028f7cf702974f52380f0741fc608d28ab732b8d24fc5d20699dfae`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Apr 2022 05:27:08 GMT
COPY file:5c7701affc9850ddb3cd433350e1cd6540048bc78ccd1085a478dc905a62bd64 in /nats-server 
# Tue, 19 Apr 2022 05:27:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Apr 2022 05:27:09 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Apr 2022 05:27:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Apr 2022 05:27:10 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Apr 2022 05:27:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b93faeabffe266939f160859e4fe954b65004d463416d6c943b83f17ea1a07c7`  
		Last Modified: Tue, 19 Apr 2022 05:29:29 GMT  
		Size: 4.2 MB (4229895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa486673456029146cdeb5aa24b79d59fbb46ceae19c2085f244a4f540a936c3`  
		Last Modified: Tue, 19 Apr 2022 05:29:26 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc2a7ab98b1adfcf8b16328efe3416e98bbed6146cffb9289d48b7f1d710f399
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4217735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd22baaa9b7fcf519609324f45785cad127c98aa25e6945ec3bd9144c6b100c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 22 Apr 2022 16:40:25 GMT
COPY file:a82c07c2e7d51d414d1e87aec6f9d2718447b772505fba86d5ea7617fc1992ac in /nats-server 
# Fri, 22 Apr 2022 16:40:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 22 Apr 2022 16:40:26 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:40:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 22 Apr 2022 16:40:28 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 22 Apr 2022 16:40:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:308394282a0e57ba139c96f20347213771c895947b7f9625212d7d91ac26cffd`  
		Last Modified: Fri, 22 Apr 2022 16:41:46 GMT  
		Size: 4.2 MB (4217229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a021323d331516d6b6519db1b4d42a2e922c74d6a39588a87e4859c26a9bd85`  
		Last Modified: Fri, 22 Apr 2022 16:41:45 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
