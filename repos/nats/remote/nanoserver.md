## `nats:nanoserver`

```console
$ docker pull nats@sha256:17a7ba92d7d9e30b2ade1940d64a5f64ea45274342f23bce8aec50f7c7c0079a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:90209bda1cad3ec772bc2677672f501958ee7d62c33edfa857dc1716bda9220b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107602854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07847f304e7f8ec4f2b589a503ef48b8ec40f915777bb525440734cb80354bfe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:d5609a37f534b519fa4326428362ea5398f7165ee90493fb7bdc8b810da33b0e in C:\nats-server.exe 
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:40:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:40:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:40:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faa5157704c1d4e58658a58ee4a6c9c9311a1d1fad5bed72177cbe21cf41dcb`  
		Last Modified: Wed, 09 Mar 2022 16:41:04 GMT  
		Size: 4.5 MB (4541860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa65daf1bc9817f903056d7a32becb96a3c4ae626707c391c115f9672dd19f9`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ca210f6c322c3169919cabf4b4814ab663aa766949d78aa18e5e52bbc9c7b7`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa906eba8a8100c8da6161e182387637cb7d3e7272ba27fb859f8c511abc7ba4`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a943f384f132c325e714fb870d67abbfbde1e4ffb1379784d990e39e0e3913`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
