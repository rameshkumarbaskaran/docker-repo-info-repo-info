## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:7b188ad8073b6d02e78f4f74279385fa549a0e75620b573ea223a7313d56ad46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1668; amd64
	-	windows version 10.0.17763.4252; amd64

### `mongo:nanoserver` - windows version 10.0.20348.1668; amd64

```console
$ docker pull mongo@sha256:1c24dff743c64aadd979a5f391a94f178373924aa53928d929ab9a4d10ab994a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.0 MB (637043299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8cbe24580364e2031f74daaa4f31ff5dde02be5b40eb7d6a7465aa578cb5b1`
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
# Wed, 12 Apr 2023 00:22:26 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Wed, 12 Apr 2023 00:22:27 GMT
ENV MONGO_VERSION=6.0.5
# Wed, 12 Apr 2023 00:23:20 GMT
COPY dir:8cafabdc84824168ccb42f1fb38dd461d1f5833e45f22346735df9067c52e6a6 in C:\mongodb 
# Wed, 12 Apr 2023 00:23:35 GMT
RUN mongod --version
# Wed, 12 Apr 2023 00:23:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Apr 2023 00:23:37 GMT
EXPOSE 27017
# Wed, 12 Apr 2023 00:23:38 GMT
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
	-	`sha256:05b87324978199f43ba1655abb8095fc3903057632c3e993abbfa4f50c5c4e7a`  
		Last Modified: Wed, 12 Apr 2023 07:24:27 GMT  
		Size: 267.2 KB (267175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30e667ae48be41a18df9e2618d812417a48a9fd1ca04c10b4de8f5c8ab3ceb5`  
		Last Modified: Wed, 12 Apr 2023 07:24:26 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc8be245d52d614719359a8be7ebe379db0e0fc10805eaff86eac0d72ce1a45`  
		Last Modified: Wed, 12 Apr 2023 07:25:43 GMT  
		Size: 514.3 MB (514301867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690a612f16adb51dd620f947acdb1a8dc53a3bfca95e7cf0b569177b807136e1`  
		Last Modified: Wed, 12 Apr 2023 07:24:25 GMT  
		Size: 49.5 KB (49490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6b99a6a5089202152377ee049179be2d8862e4698d060e24c52e52d6af1a70`  
		Last Modified: Wed, 12 Apr 2023 07:24:25 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a243a97fb1510ab3f880ed9bdebbb0eec24e4dc8a3dcb85ed3b0c4a4457f685`  
		Last Modified: Wed, 12 Apr 2023 07:24:25 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95fd23659b3eaf6a8dfe282a780f4b72434d41c7f8b04485ab8b5a33e573a3e`  
		Last Modified: Wed, 12 Apr 2023 07:24:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:nanoserver` - windows version 10.0.17763.4252; amd64

```console
$ docker pull mongo@sha256:b468abc6a34468e976d98d441d688290bf8334688da04e14d34e6168cb9a2118
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.5 MB (621503499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377b8f391f2cfdaff4fdefe50716631c9e40f2a581ba6c96ff8c78261cf7e718`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Wed, 12 Apr 2023 00:23:53 GMT
SHELL [cmd /S /C]
# Wed, 12 Apr 2023 00:23:54 GMT
USER ContainerAdministrator
# Wed, 12 Apr 2023 00:24:05 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 12 Apr 2023 00:24:06 GMT
USER ContainerUser
# Wed, 12 Apr 2023 00:24:07 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Wed, 12 Apr 2023 00:24:08 GMT
ENV MONGO_VERSION=6.0.5
# Wed, 12 Apr 2023 00:25:03 GMT
COPY dir:8cafabdc84824168ccb42f1fb38dd461d1f5833e45f22346735df9067c52e6a6 in C:\mongodb 
# Wed, 12 Apr 2023 00:25:20 GMT
RUN mongod --version
# Wed, 12 Apr 2023 00:25:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Apr 2023 00:25:21 GMT
EXPOSE 27017
# Wed, 12 Apr 2023 00:25:22 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e9c90f3a763714533d4a634f7ab3d23374e5208e2ac8bae4288243917bd972`  
		Last Modified: Wed, 12 Apr 2023 02:34:36 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6552b5bd1c6568d6f39240a39a0344d31519e6acaf2437760d33a2f1bd16ebb4`  
		Last Modified: Wed, 12 Apr 2023 07:26:01 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb24d44a5b22599181c1f6c9ebdf5458cb1fc58facdffff33b51e656ba5a14b`  
		Last Modified: Wed, 12 Apr 2023 07:25:59 GMT  
		Size: 68.8 KB (68801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61d7e4579b59b23268c08766daece41ab2483fa4867cc1a017edcfc07642639`  
		Last Modified: Wed, 12 Apr 2023 07:25:59 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d55c5377c7d6bc38390274de33a30c25cec352bfbfedb225c3509ed2666a10a`  
		Last Modified: Wed, 12 Apr 2023 07:25:59 GMT  
		Size: 267.2 KB (267163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d808f77f3c1027f5d860824e6e481c1beb1fa35a4909ead21f408e540ea58730`  
		Last Modified: Wed, 12 Apr 2023 07:25:59 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3bbec4c461b6da9769372b8f64132d6ea89e19422fdc41e23c0d7504622059`  
		Last Modified: Wed, 12 Apr 2023 07:27:16 GMT  
		Size: 514.3 MB (514298495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b9e82a7a2f95a5abf61ac652004364d08e62d50dea0cfaec65555e9e33ce59`  
		Last Modified: Wed, 12 Apr 2023 07:25:57 GMT  
		Size: 72.0 KB (71964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950fc6fb51eb4d987b87b8fd0ec8b61d664b1f7d3d51fa9360f7a8f73ad0b3dc`  
		Last Modified: Wed, 12 Apr 2023 07:25:57 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043e36054f97bbe93cd083a574b424d7365bb9609db7a019e26fe2ae26857533`  
		Last Modified: Wed, 12 Apr 2023 07:25:57 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8da91649eb78754e2760fb2a50b0841e0b04ded43a4768359541eb69bc5474`  
		Last Modified: Wed, 12 Apr 2023 07:25:57 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
