## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:5cd37215ff336d5088132aa1b7ab5181672cc9cfb98449c8939d9e76527d5b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull traefik@sha256:27294c1a1d580b0163e45a21d41436ddd407923adfa55fc5cc9d66a045b4778a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296630581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e41d46f735bd1ea7414451f7b43be56d2226358fd157fd26845bf4f22c8e3b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 21:19:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 15 Apr 2020 21:19:27 GMT
EXPOSE 80
# Wed, 15 Apr 2020 21:19:29 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Apr 2020 21:19:29 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6882ac7e421413d744527f8e3436836a9975061deb9f09982b57422ab7b015`  
		Last Modified: Wed, 15 Apr 2020 21:20:58 GMT  
		Size: 25.9 MB (25918816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423691ba5eccfd282fbcfaa475cc5068b4ab4eb2a5e9a33af84dfa9024b11b00`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a00a51e357ead2b0d9cc5279dbfe48f31b56c62a5204963e430445265270f8`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d82edeef8498bbfccea22d382d39fae344616a8f745e704f914ddb6cd3e0d6`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
