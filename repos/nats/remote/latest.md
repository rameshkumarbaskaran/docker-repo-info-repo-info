## `nats:latest`

```console
$ docker pull nats@sha256:a66bd53bc5fa8c23dc87b2d366d4e5d3987b75ad479a1c53e7f1dcfdf418d942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2686; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:5fd249efa75cf3eb595342175207fdbb390eee3034f7fe49355d7a479fa3ffe2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4499407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84de17b17b3458d2b6e6d4264ea6186c82bab718ca058f5d7738e53ca2759ac`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:8a814b0c66a47e63e5a7f4287478948812fe6e03c224d539f37ce3f950d2b6c6 in /nats-server 
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:21:14 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:21:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:277fae1baf41821774f7a2e1c3f465b28aa8693ee0cd77e0ad0bace55d9c616e`  
		Last Modified: Fri, 25 Feb 2022 02:22:04 GMT  
		Size: 4.5 MB (4498900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb932b4b3fbc873b56e996c6357055bb7700c701d17d7d87cdec31211142b49a`  
		Last Modified: Fri, 25 Feb 2022 02:22:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:2e3339e7e8d98e7bbab0613c7b7c3dd6f51fcf33ed3910a2e65e62fba7049337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc7bcc78dd550ace4def82e3db227e618d77e136274749f3bf55869e64be264`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:3a951d885f7bcec693f6fbf26a9ffd82b0c6218b6834fc6053e5812f7451b63e in /nats-server 
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:50:07 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:50:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:50:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6de87b4530f922b11edc08be8edeebc6ce0cb666907013348d4e1b9f5d51809`  
		Last Modified: Fri, 25 Feb 2022 02:52:29 GMT  
		Size: 4.2 MB (4165468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fa68b52226484e5870677184cdc47c93a7d453f334c144b5cb631346bc8111`  
		Last Modified: Fri, 25 Feb 2022 02:52:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:87cf3f8e33ebf28f35575ea083f8feb460d19fa9380d2622c82567ff3fa9d840
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eef99b95e572b23f90d60e6e157be90b05ab2f35dbcb10f83f96ece551945a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:3ee879939ad264e803dd4d6072181d968c4dd0fe076115159f70479c6309ef45 in /nats-server 
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:58:35 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:58:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67a3d8907097b9caffd9d1720b4fb2b1d2ac9dfda60a1d169abbf5494323d50a`  
		Last Modified: Fri, 25 Feb 2022 03:00:58 GMT  
		Size: 4.2 MB (4157409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5577f4846f032b281220b897161962481198ead0a1b9ad1d7c76cdd989747`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e970861a260709ae1e8c892eb36758c14323e81959ff4aaa1e9b7327b91d3e70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4414e48026697a15338f28dcb8e46ace9627ea7332559e1708f36ce62a5e327`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 03:01:42 GMT
COPY file:acd11e9a3a86f6f3da079c5155851337e747c3b31481ec05e2dd1e48e23becb2 in /nats-server 
# Fri, 25 Feb 2022 03:01:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 03:01:43 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 03:01:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6ad9fd47af885b43442590ad2c8171e4b4899caef84921ec73ba0540b9c03284`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 4.1 MB (4143299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7667f81936503f26a5ed657cfffdc9add626da8ae5bb78d691054cd3af7c3`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.2686; amd64

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
