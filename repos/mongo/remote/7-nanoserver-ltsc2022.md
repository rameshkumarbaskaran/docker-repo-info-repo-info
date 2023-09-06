## `mongo:7-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:e338a6fcc9ce2405aab8d349dbdeec35b7c3c89bdc5f38912ebabcbf478f2685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `mongo:7-nanoserver-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull mongo@sha256:01336e65096598d05fb81329810e4758fe8dd4e34f3bdbdde1ed89929b930913
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **732.5 MB (732504064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e0e5f1d690a75751707f2983919b40cca5e5155b5367702a3f385bec61e9f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 03 Aug 2023 09:40:19 GMT
RUN Apply image 10.0.20348.1906
# Thu, 10 Aug 2023 00:45:25 GMT
SHELL [cmd /S /C]
# Thu, 10 Aug 2023 01:14:21 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 01:14:29 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 10 Aug 2023 01:14:30 GMT
USER ContainerUser
# Thu, 10 Aug 2023 01:14:31 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Wed, 06 Sep 2023 00:40:47 GMT
ENV MONGO_VERSION=7.0.1
# Wed, 06 Sep 2023 00:41:34 GMT
COPY dir:dd7e8197ac0171161d6946ee93a67cf7f770b5ce539a9dc154869493c9e2623b in C:\mongodb 
# Wed, 06 Sep 2023 00:41:54 GMT
RUN mongod --version
# Wed, 06 Sep 2023 00:41:55 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 06 Sep 2023 00:42:12 GMT
EXPOSE 27017
# Wed, 06 Sep 2023 00:42:12 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:ea9613880997b3ab2284a37c0c14a403553457b0c331b41c6bd6d1cc7838a222`  
		Last Modified: Tue, 08 Aug 2023 18:47:21 GMT  
		Size: 120.5 MB (120500677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a528e77cf0bef98e15c3b4194ee340960485498ac4c1bdcbab44307858ecfc4`  
		Last Modified: Thu, 10 Aug 2023 01:03:26 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0247382dbd5864284425d3942427091871bf5f10629f0608efbc6b3303d067`  
		Last Modified: Thu, 10 Aug 2023 01:59:00 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ffaf70bb154004aa4faefa8b8926380d11a591157ac5074e2438ce1696d3ac`  
		Last Modified: Thu, 10 Aug 2023 01:58:58 GMT  
		Size: 77.9 KB (77932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54933f30fc7826d81c7a7731e98cb5ea37dd377d70a605f59fda57f3a196506c`  
		Last Modified: Thu, 10 Aug 2023 01:58:58 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa6daf2a597ffb630f230ca7808bb850f20a800b5ffaf16207e74b4405ba9ff`  
		Last Modified: Thu, 10 Aug 2023 01:58:58 GMT  
		Size: 267.2 KB (267199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d56266ac1b207442be3ec1b115c1164ea6d7cd1e8443f4ecac163712b77209`  
		Last Modified: Wed, 06 Sep 2023 00:58:01 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfef75868e0077d4f6edca6107ab8e0093a392830c3ac99aaf95eff7542eaf0`  
		Last Modified: Wed, 06 Sep 2023 00:59:27 GMT  
		Size: 611.6 MB (611589334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014a7d2f887841286c11cb496338234dc3d3e96b3a3ce2f6fe3a8d4cee285ed3`  
		Last Modified: Wed, 06 Sep 2023 00:57:59 GMT  
		Size: 60.8 KB (60783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924a3fe8ff0f7a1c51957596d29fa98ab765554df10dc95e029ffdecd60d81c8`  
		Last Modified: Wed, 06 Sep 2023 00:57:59 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e064f427217b2784c57081eadc0ca81b17961c3b8a2257c1308e1726fbc03a`  
		Last Modified: Wed, 06 Sep 2023 00:57:59 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1c71547c49d34deade60d32fc56b752b362ded53f3d6899b139a2e3e62c74a`  
		Last Modified: Wed, 06 Sep 2023 00:57:59 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
