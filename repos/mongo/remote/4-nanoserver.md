## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:7fc1e91d19c3a99c2388fe6104f9bcf78ae04da3ec5c05ede583ee44f9cfb2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1726; amd64
	-	windows version 10.0.17763.4377; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.1726; amd64

```console
$ docker pull mongo@sha256:e13ff62cc6388e9bb1271c75606ae04e69596e4ff717ef456132d0311316d455
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.4 MB (365449111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d967b2d64887ba9517ba1562f88060664770b4ae2802487daeff21e112394057`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 May 2023 12:52:54 GMT
RUN Apply image 10.0.20348.1726
# Wed, 10 May 2023 01:28:38 GMT
SHELL [cmd /S /C]
# Wed, 10 May 2023 01:59:56 GMT
USER ContainerAdministrator
# Wed, 10 May 2023 02:00:07 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 May 2023 02:00:08 GMT
USER ContainerUser
# Wed, 10 May 2023 02:07:18 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 24 May 2023 01:33:32 GMT
ENV MONGO_VERSION=4.4.22
# Wed, 24 May 2023 01:33:52 GMT
COPY dir:ba7da3b127dd995e6b5f5a8e9cc5f87caa3174d8a03e6b82fdeaa7d4f4b54ce8 in C:\mongodb 
# Wed, 24 May 2023 01:34:05 GMT
RUN mongo --version && mongod --version
# Wed, 24 May 2023 01:34:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 24 May 2023 01:34:07 GMT
EXPOSE 27017
# Wed, 24 May 2023 01:34:07 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7d382efe6974b94c05000b6a95c1fd28e1b8bb3e81cc4592b2aa1cc46b90192c`  
		Last Modified: Wed, 10 May 2023 01:48:23 GMT  
		Size: 120.0 MB (120001338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d879624716c16bfc9a9e8c219f4a25a8d311021e41efa6a951e95c4bb6fc44`  
		Last Modified: Wed, 10 May 2023 01:47:58 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91148a7dea4dbf3b1028e81c00818780ec56bdbb7563cc6100dacaf0aef85da2`  
		Last Modified: Wed, 10 May 2023 02:25:01 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35d61dd28046e22574977fb6b4d943048979c432dd7d414debb3684a58405c4`  
		Last Modified: Wed, 10 May 2023 02:24:59 GMT  
		Size: 78.2 KB (78198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2e0389b82941ae5dd46a94665227d43b3fea67bff14cbf6ecc35cd654bb269`  
		Last Modified: Wed, 10 May 2023 02:24:59 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53e50933b5a40ecf4eaa2a19612ca2e58cc04e97d929f370bcc5597615755bb`  
		Last Modified: Wed, 10 May 2023 02:29:57 GMT  
		Size: 263.4 KB (263408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a8f66bf9edacf1306f3b7fc2d8d451d56841516d6a96a688dab5bc9111e7aa`  
		Last Modified: Wed, 24 May 2023 01:48:48 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cd88cc547826f9d267352d477f181938182514a598d17442ef1194c5a5f524`  
		Last Modified: Wed, 24 May 2023 01:49:32 GMT  
		Size: 245.0 MB (245045827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09731a85812f2b3a2e79ad988903ecf97cb93e5a4124615d7214c583ea469b`  
		Last Modified: Wed, 24 May 2023 01:48:47 GMT  
		Size: 52.4 KB (52411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80830772a2241729af0ac4f271f66b7dda99262b130f29db71acff23838c2d3`  
		Last Modified: Wed, 24 May 2023 01:48:46 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1476aaf1c84e88b5e9e9105626ffed74f20393656f253e2d4601bdd84d268f4`  
		Last Modified: Wed, 24 May 2023 01:48:47 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45bbde570e791b1e4f8d92187025afdf1596c2b6908a101f62d2884dc988665`  
		Last Modified: Wed, 24 May 2023 01:48:46 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-nanoserver` - windows version 10.0.17763.4377; amd64

```console
$ docker pull mongo@sha256:df7bf209af7762fbf567a8c721bc82c34bf2717d2bcd0f939a562e777999c6e3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.8 MB (349840591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbb29ba2eaabfe84d5738c7228c9c8cf8a73dab99254674320e35e3b963997c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 01:31:05 GMT
SHELL [cmd /S /C]
# Wed, 10 May 2023 02:01:10 GMT
USER ContainerAdministrator
# Wed, 10 May 2023 02:01:23 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 May 2023 02:01:23 GMT
USER ContainerUser
# Wed, 10 May 2023 02:08:12 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 24 May 2023 01:34:16 GMT
ENV MONGO_VERSION=4.4.22
# Wed, 24 May 2023 01:34:38 GMT
COPY dir:ba7da3b127dd995e6b5f5a8e9cc5f87caa3174d8a03e6b82fdeaa7d4f4b54ce8 in C:\mongodb 
# Wed, 24 May 2023 01:34:53 GMT
RUN mongo --version && mongod --version
# Wed, 24 May 2023 01:34:53 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 24 May 2023 01:34:54 GMT
EXPOSE 27017
# Wed, 24 May 2023 01:34:55 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ddac9d33b62fa0bb37c6743a1992a622e53b5bb070758474e92416b5f031ba`  
		Last Modified: Wed, 10 May 2023 01:48:38 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca1a117e5be28c4247978f3dfd437fff6feffb4a11ea43d4338f5d2b068ac76`  
		Last Modified: Wed, 10 May 2023 02:26:28 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba404708f5c409a4327ef9a8ea3e3601dd2db287f5d90c7794dada10f4ae9e69`  
		Last Modified: Wed, 10 May 2023 02:26:26 GMT  
		Size: 62.9 KB (62943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc7f80cef905cfe3aae8cf8ef021d8f598871b9df0222b4cc3f5b66899cac64`  
		Last Modified: Wed, 10 May 2023 02:26:26 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd95f6c90520d7fe9349ffc114d55efdfc3d2a4675433070a2dd42eb6d76948`  
		Last Modified: Wed, 10 May 2023 02:31:00 GMT  
		Size: 263.4 KB (263441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb024004451fc0eb006c2bcf3bd57bb4d810bc50a220d86fbe99aee082611808`  
		Last Modified: Wed, 24 May 2023 01:49:46 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b72ffcb1ebd5b113e62e7a74d32003e65eac95d5c9c1a80135cb3276092931`  
		Last Modified: Wed, 24 May 2023 01:50:26 GMT  
		Size: 245.0 MB (245045907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b96686338b7511c017c1fd95e2e096ae77e6a6dbb6bf0e7906de860a41c1dfc`  
		Last Modified: Wed, 24 May 2023 01:49:44 GMT  
		Size: 76.5 KB (76481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343e9228e464dd372132cbcd58c92df94bf390b6bb91300c5f82c83c5a5196eb`  
		Last Modified: Wed, 24 May 2023 01:49:44 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65566c3fd973e671dfa64fffeac684e35c3d80004897b42d0ebc82ac79d12c15`  
		Last Modified: Wed, 24 May 2023 01:49:44 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373747d80a989ee3c2835d50eb472eb2a25515d12010ae756914e30b9def1664`  
		Last Modified: Wed, 24 May 2023 01:49:44 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
