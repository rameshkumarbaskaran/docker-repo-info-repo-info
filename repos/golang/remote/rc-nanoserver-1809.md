## `golang:rc-nanoserver-1809`

```console
$ docker pull golang@sha256:b5ea492c86b8c907e0212c86c15e7c1923b812499981d12185a11c7d64816153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `golang:rc-nanoserver-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull golang@sha256:81e5336bf13a2d9dd87474682cfbd626d61f6f0591041cf73e936166b75d64a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247884492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947570f31e0b8426d8352ada07c835f26c036182f3679406906ac81834d188df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 01:23:41 GMT
SHELL [cmd /S /C]
# Tue, 20 Jul 2021 18:26:46 GMT
ENV GOPATH=C:\go
# Tue, 20 Jul 2021 18:26:49 GMT
USER ContainerAdministrator
# Tue, 20 Jul 2021 18:27:28 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 20 Jul 2021 18:27:31 GMT
USER ContainerUser
# Tue, 03 Aug 2021 03:22:37 GMT
ENV GOLANG_VERSION=1.17rc2
# Tue, 03 Aug 2021 03:24:40 GMT
COPY dir:cd614221ba57e51c16a53a373b51f1a4aecca3bc44c7bb8aad976d0cfbb1b8e2 in C:\Program Files\Go 
# Tue, 03 Aug 2021 03:25:08 GMT
RUN go version
# Tue, 03 Aug 2021 03:25:10 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5307d56ac81f33a647e0ed6f4e0f70a39b207469fe0a28ab1b9f9379669e02b4`  
		Last Modified: Wed, 14 Jul 2021 02:04:59 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83405bb536089e13fd0501a2503e1823078fb9090aed935d6eb44c448a1a26a`  
		Last Modified: Tue, 20 Jul 2021 18:33:39 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83275ca5ff7629bf58f1b287f29bfa9bc8820b195f91f22b9678afb1308c8458`  
		Last Modified: Tue, 20 Jul 2021 18:33:39 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da59a5ba58e609884e84af7c652a2ce436a51d2b9188a353a2b8268ab42fb14`  
		Last Modified: Tue, 20 Jul 2021 18:33:39 GMT  
		Size: 65.8 KB (65825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82bb786232ee0c60d9c510231a27162f2858a02b82551e82c5fca0ad2d4170f6`  
		Last Modified: Tue, 20 Jul 2021 18:33:36 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5090abaf548d34dcdabd6fe10ba7e063ef0157236434c8de16a7ecffdd2b3332`  
		Last Modified: Tue, 03 Aug 2021 03:28:04 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bc8900f1241d414ef78bc2272a775d380e0e438149a00673274dd0db6bcac0`  
		Last Modified: Tue, 03 Aug 2021 03:28:33 GMT  
		Size: 145.0 MB (145021260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac1ca540e43dc565f402933c19ead04d80fe08d2291a514a796ad0e2da8d1da`  
		Last Modified: Tue, 03 Aug 2021 03:28:04 GMT  
		Size: 64.7 KB (64668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d7a3a00d0fcd2e2c823a6a3401c2c440fd53ae98814dfa80fad758d141e805`  
		Last Modified: Tue, 03 Aug 2021 03:28:04 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
