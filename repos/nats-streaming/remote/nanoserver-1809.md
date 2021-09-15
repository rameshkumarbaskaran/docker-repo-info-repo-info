## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:d825481c4d8339d300a56d9f3eeaecf48ae0c071064bfa5ccfb1d9393ff52765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats-streaming@sha256:f7300d49f73a0e5451f68fcf439d1e5b75b5a891aa04e8ff537b523b15d45fc6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110001330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa93dcd937d8cd2009cb8f123551ce0f46c671f91465df126ce8475110a4f6cd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 15:43:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 Sep 2021 18:51:57 GMT
RUN cmd /S /C #(nop) COPY file:9670e5d1fe5a71e47c78fde01235a0bcbcafcfdeeacf96a7669f6e49343fb03b in C:\nats-streaming-server.exe 
# Wed, 15 Sep 2021 18:51:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 15 Sep 2021 18:51:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 15 Sep 2021 18:51:59 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:66dbf96361e9ec1f64f66e255a947eab476edef46c3f9a3b4ede943fa8b87699`  
		Last Modified: Wed, 15 Sep 2021 15:46:11 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e5a8a8a1823e7ab1aab125064b8d7d94f6dacefba9d82b815174cb4c32a833`  
		Last Modified: Wed, 15 Sep 2021 18:55:12 GMT  
		Size: 7.3 MB (7293261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16df1d39830ccb4fa2828c96b6c6ec476f1f3a292bdbd01053a21c6c9457750b`  
		Last Modified: Wed, 15 Sep 2021 18:55:04 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f99c367ebf7f75f5e675f26e18195abf8826890c87d26039e2c58b38a681d6`  
		Last Modified: Wed, 15 Sep 2021 18:55:04 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3052f7738f8821f9a96f777624d74a7b0b9c7fe0bcecce51d3586ea05479556d`  
		Last Modified: Wed, 15 Sep 2021 18:55:04 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
