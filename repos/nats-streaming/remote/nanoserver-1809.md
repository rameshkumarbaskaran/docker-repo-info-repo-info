## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:3cc0e52c1cb44fc5a90b9700182bfa9c89b1ac66467df20bdcab1ab04d6e0891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull nats-streaming@sha256:f2a55f70ee492ea8558418b26a10b4bab14502b221829bba37fc14f1ad1a52f6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107723872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaffa70349c9b3d0962938d3d354b287074d9f2a3ca53f3f880b0f2c4348372`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 30 Sep 2020 11:25:56 GMT
RUN Apply image 1809-amd64
# Wed, 14 Oct 2020 16:26:27 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:28:17 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Tue, 03 Nov 2020 00:28:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:aab6118ce69c93410df7fa15842a6e3b3c7ff20b639c779b5d5f78e7653eaa07`  
		Size: 101.2 MB (101205155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:93b9a3c3e46fc1677426e3be7ce449b91d540c5ae2147380034cc4e1dc7445c3`  
		Last Modified: Wed, 14 Oct 2020 16:31:12 GMT  
		Size: 910.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80c5ff22001aef46c227bbdf3bb49e81d719eaabb98e05f489316336046c353`  
		Last Modified: Tue, 03 Nov 2020 00:32:50 GMT  
		Size: 6.5 MB (6515148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bab211499304d94ab254d507f765f27913f9f1d2c2a7f144c8fb339b90255f`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1b35db78e25d5e897749f516159111a429e7ff0a22bcdc8f2090bce6aa5d6c`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ffc7f1df369d7406946da80c5cea7b9338075a8e9975e92297d67b9d581f13`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
