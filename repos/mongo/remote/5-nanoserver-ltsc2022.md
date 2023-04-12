## `mongo:5-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:9ff86fef800b9ab94f3c89badde6bf005b5150c8a5e832e752a1d7c0fd7bed61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1668; amd64

### `mongo:5-nanoserver-ltsc2022` - windows version 10.0.20348.1668; amd64

```console
$ docker pull mongo@sha256:b7788443859f6aa2c3f6b2b9798b30e5547e4f8fcd10d3267c8c2aad23b6a7a8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.1 MB (435076179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1310366b615b5d42b675436e8d945e91d95144e780207d523979cbb9ae59a5bf`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:16 GMT
RUN Apply image 10.0.20348.1668
# Wed, 12 Apr 2023 00:22:09 GMT
SHELL [cmd /S /C]
# Wed, 12 Apr 2023 00:22:09 GMT
USER ContainerAdministrator
# Wed, 12 Apr 2023 00:22:24 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 12 Apr 2023 00:22:25 GMT
USER ContainerUser
# Wed, 12 Apr 2023 00:30:22 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 12 Apr 2023 00:30:23 GMT
ENV MONGO_VERSION=5.0.16
# Wed, 12 Apr 2023 00:30:56 GMT
COPY dir:075c117c846ecae2a4dae09c1251726c18757124193e63e7a862c7fb794f695e in C:\mongodb 
# Wed, 12 Apr 2023 00:31:11 GMT
RUN mongo --version && mongod --version
# Wed, 12 Apr 2023 00:31:12 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Apr 2023 00:31:12 GMT
EXPOSE 27017
# Wed, 12 Apr 2023 00:31:13 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:e06b772d586b58466a653b72002aee7c59496110e9ae402ff58f026e44452506`  
		Last Modified: Wed, 12 Apr 2023 02:34:14 GMT  
		Size: 122.3 MB (122328782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329579f5fc95fa89293545a20f4e45221db45261002e7012b86c4d3233edd1f8`  
		Last Modified: Wed, 12 Apr 2023 02:33:39 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ffee768115c8d7d69b2fd027383a36010ef0fdee82af33f03b9d4cd96300e0`  
		Last Modified: Wed, 12 Apr 2023 07:24:29 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b01eaee96d583c766fda2075c2b3f0d0ecbaae5f80349e49fd0231ded90b88c`  
		Last Modified: Wed, 12 Apr 2023 07:24:27 GMT  
		Size: 87.9 KB (87861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8632bd61e3a0f1116d090e2b6cafc76d6bb3c3b5cf14ac1fc393c94e4a1bc6`  
		Last Modified: Wed, 12 Apr 2023 07:24:27 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec487c1ab7e5a979f4fbd7e80f7bb8436646e0494b27aceb9005ca7e57dbba4`  
		Last Modified: Wed, 12 Apr 2023 07:29:50 GMT  
		Size: 263.5 KB (263515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbfdec1a927a7fcbd914c6e7cd713ffb605f9bb8360d99d8f6355c09fe15e74`  
		Last Modified: Wed, 12 Apr 2023 07:29:49 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e9b5a7233f7e650caf4264e5d194e2735680b20b12d50a971d80c0a5f26a34`  
		Last Modified: Wed, 12 Apr 2023 07:30:44 GMT  
		Size: 312.3 MB (312338638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f7a4003aa0b8cb856feea3f343c213bc235218beac0435888fc06b9208d011`  
		Last Modified: Wed, 12 Apr 2023 07:29:48 GMT  
		Size: 49.7 KB (49713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a235716f2b2feaa1f50431948398bfd77fcabf1fb9a25de7990043b9154a848f`  
		Last Modified: Wed, 12 Apr 2023 07:29:48 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b07db3ed1a9ee18d7735459a9895a9391a189f48a2d6af41a4036dbaec836f`  
		Last Modified: Wed, 12 Apr 2023 07:29:48 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db08fe6e6e43fddbfefef8a795314df14f71bf5dff1fec3f5dd429b927473685`  
		Last Modified: Wed, 12 Apr 2023 07:29:48 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
