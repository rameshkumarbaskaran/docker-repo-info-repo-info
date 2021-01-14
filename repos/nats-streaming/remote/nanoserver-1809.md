## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:c7b60cb7eb50b0454d787676660cbb52ebc25457d367cc91f7f6219eb3cdc861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats-streaming@sha256:131f9c39ac29e11d0dc81c1c26cc0fbbb50b832eaba8715c6504d1dac8418435
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107365498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef855a422d4be3f13d838208fd85955fd7768b3567bd89861a6d67df15122d4a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:06:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Jan 2021 00:16:51 GMT
RUN cmd /S /C #(nop) COPY file:f2450ffeda74e33f820191eccf78b6647ce56865170e966bfa8e72afe6e46c36 in C:\nats-streaming-server.exe 
# Thu, 14 Jan 2021 00:16:52 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 14 Jan 2021 00:16:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 14 Jan 2021 00:16:54 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a89b73109217060f51d51b7d3a7eda3a9ac0de9c5f76db54addb98b7f1c24c1`  
		Last Modified: Wed, 13 Jan 2021 19:10:49 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b689a2a270a9c8e1ec741a7297ca14c2001e9a7ab5c9ea3d06f4cf834b8261`  
		Last Modified: Thu, 14 Jan 2021 00:21:28 GMT  
		Size: 6.0 MB (6021918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9339c8634418d855b08dc20f472d3906160f6010ee4b4f1c803e0e9cc4f6d6e3`  
		Last Modified: Thu, 14 Jan 2021 00:21:23 GMT  
		Size: 877.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de47275056946f9394ba060e89e9ab1710aa73977d6485df317ed346a3c6ed1`  
		Last Modified: Thu, 14 Jan 2021 00:21:25 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b4ebb72cdd066de0407bdd35275fc5528023c450322d57a92f6527fc42b931`  
		Last Modified: Thu, 14 Jan 2021 00:21:24 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
