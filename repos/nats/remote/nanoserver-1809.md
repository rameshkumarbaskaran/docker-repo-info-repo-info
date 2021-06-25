## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:4ebe0f8afa0791f4642839c39904f87117ae2b491ef7cc3af12fe3ea313999b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats@sha256:c3d85580c0f97e9e7525ac25ff6dd2b46e30d0a28d8eae5922200f692c5f5420
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107067292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60db2a891b8d4acaed25bf0dfdd41e93f36804395b740b4fdc1e2bb452c6c1b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 15:55:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 24 Jun 2021 18:16:39 GMT
RUN cmd /S /C #(nop) COPY file:bac1db2af96d2ddad22da9ae2b1252ad143dce10623146a5898a15a4e3f18d81 in C:\nats-server.exe 
# Thu, 24 Jun 2021 18:16:42 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 24 Jun 2021 18:16:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:16:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 24 Jun 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:80d93ce19113bbf944b699f12e59395e0eabeb00ccd1fd5dc7df46bb115eba2f`  
		Last Modified: Wed, 09 Jun 2021 15:59:58 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec670391ee18da96972d36cee7981927664f13e0189b3d1f31b2c62e5ca0d4b`  
		Last Modified: Thu, 24 Jun 2021 18:21:31 GMT  
		Size: 4.4 MB (4389381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ee48b932f6c168a30dd680d51235836a69ad93983a5aa6ae510649498009d`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47216eb523d03d9b262b596ac92cdee9995cea672a4b3914a9f02a41a5ff422`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26d8e3fee7dfa3f7bf9b8af44b5f640be79d646bbcb96459100b6b39fe7bda`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348ad20da8616571c92e671840d54b660df38b670f5bf015aeaa2f6bed084657`  
		Last Modified: Thu, 24 Jun 2021 18:21:29 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
