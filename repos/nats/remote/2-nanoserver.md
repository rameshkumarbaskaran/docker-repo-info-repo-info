## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:e93c53dfa92b3aa8a99b0b82e1e065c6180489121d90d447fbbe352bb04d4334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:983d25974e771f9316c9e4a5bb71b449518805ddb52e6c7878e171bcccecc945
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105081331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dac43460097cf1c43ccb252c52bbba61b8d41b4a7e413763329d909f5d4f89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 06 May 2020 12:39:06 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 14:50:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:41 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Fri, 15 May 2020 20:15:43 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e6fec25718aef5ed18d499b27e43adb524f9ee4f2eb3f0fffaea018e7e86b0`  
		Size: 101.0 MB (101019852 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eafb3f3d63d93b402dfcc428e091787a4242326bc71283a6e3ad40046a60cba0`  
		Last Modified: Wed, 13 May 2020 14:55:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516b6f4ab70976d0f6eefe7345d23e3384290ec3d07e5fd84e86a38a9355f2af`  
		Last Modified: Fri, 15 May 2020 20:20:01 GMT  
		Size: 4.1 MB (4056463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63162a0c7c0aaa22ee2b6ad6d892c8fc4e3d3a0b8ddbf7bd7f2b43b97178540b`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84857e1674bb786ff63ae8a8ddc3a7af87297c5623e8649378c6cd00f404f023`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd47e8ce84e533b8e666ae64628d761d36656664b77077b25b1c1b629f37af6`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470ec79ba35428ffa62bae3a80bfa890befff422d5089eed1ec724da29df0ab2`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
