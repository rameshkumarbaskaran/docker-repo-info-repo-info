## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:f9a1c0d2e748517f42868cf5a415f6d237a615dfd8b6b16f31ba50cca449d74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1726; amd64
	-	windows version 10.0.17763.4377; amd64

### `mongo:nanoserver` - windows version 10.0.20348.1726; amd64

```console
$ docker pull mongo@sha256:84b8dfa655e810ec64afe97c5967166a71fbdc947d2d8ebc9ac0e0d82a941515
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.7 MB (634705442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c520fff00e6903974fbcc48bc1fdb2ff74022b07ac24d46404919a8e44ef64`
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
# Wed, 10 May 2023 02:00:09 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Wed, 10 May 2023 02:00:10 GMT
ENV MONGO_VERSION=6.0.5
# Wed, 10 May 2023 02:00:50 GMT
COPY dir:8cafabdc84824168ccb42f1fb38dd461d1f5833e45f22346735df9067c52e6a6 in C:\mongodb 
# Wed, 10 May 2023 02:01:01 GMT
RUN mongod --version
# Wed, 10 May 2023 02:01:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 May 2023 02:01:02 GMT
EXPOSE 27017
# Wed, 10 May 2023 02:01:03 GMT
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
	-	`sha256:7e7a5644fdc14b36e2d367b2a0cd0e92984d2f33a59df4c7ff7b370ca858b249`  
		Last Modified: Wed, 10 May 2023 02:24:59 GMT  
		Size: 267.1 KB (267075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061f955cedeab37fb083d1833e914ae4c33efab80d42a35834f63d16567e54d0`  
		Last Modified: Wed, 10 May 2023 02:24:59 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a72c9a00a772e984f2962be6e2b38c9efbd6df1098f8a8ea798c1bb0f339bb9`  
		Last Modified: Wed, 10 May 2023 02:26:11 GMT  
		Size: 514.3 MB (514298737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234f77c44a88802ef9a5a50481be3eacade70abd18cd3e793b98e11a6fe69f83`  
		Last Modified: Wed, 10 May 2023 02:24:57 GMT  
		Size: 52.4 KB (52401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fcd69602cdcdeb338fc69c9ade6c681a6dacec26cdf6ac222c9b10d3cada62`  
		Last Modified: Wed, 10 May 2023 02:24:57 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71df131789d6caeb2028ef48a3dbc1a64a047ec75b556939c60c6521c181df4c`  
		Last Modified: Wed, 10 May 2023 02:24:57 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e1d3fa74883073713c82089aaf34966132c22b94e495c137261510f2143f15`  
		Last Modified: Wed, 10 May 2023 02:24:57 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:nanoserver` - windows version 10.0.17763.4377; amd64

```console
$ docker pull mongo@sha256:01c1299b203d53c94c90f2c6e7facbcd5cc5b5809a73ac89a3b0101626334381
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.1 MB (619093419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74d9f6a7de0354210ec793e20cc8fb2b218d7ca0b8572750e3a98de32b16be6`
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
# Wed, 10 May 2023 02:01:24 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Wed, 10 May 2023 02:01:25 GMT
ENV MONGO_VERSION=6.0.5
# Wed, 10 May 2023 02:02:04 GMT
COPY dir:8cafabdc84824168ccb42f1fb38dd461d1f5833e45f22346735df9067c52e6a6 in C:\mongodb 
# Wed, 10 May 2023 02:02:16 GMT
RUN mongod --version
# Wed, 10 May 2023 02:02:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 May 2023 02:02:18 GMT
EXPOSE 27017
# Wed, 10 May 2023 02:02:19 GMT
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
	-	`sha256:5883016a4e02b85dace5bd9fe10a5466a6aa4896b34b6c5148945751cc896318`  
		Last Modified: Wed, 10 May 2023 02:26:27 GMT  
		Size: 267.1 KB (267062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd40acb0af03bc893eef3b7e2856d5c601fc3afdaecb91bc959692bac0861f2f`  
		Last Modified: Wed, 10 May 2023 02:26:26 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9910d6e75990214cdddb9e40cc786b4afe1903c738857a87ed0cfed7d7fbf77`  
		Last Modified: Wed, 10 May 2023 02:27:35 GMT  
		Size: 514.3 MB (514298808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bc989fd0058f590e5a80a9bbdce7a43be7cf5a8667840f318765fb45a46fad`  
		Last Modified: Wed, 10 May 2023 02:26:24 GMT  
		Size: 73.2 KB (73239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8038e32644ce4a2ff864c95c4016923eb22db7ce683b8358dac03aaeef5de6b6`  
		Last Modified: Wed, 10 May 2023 02:26:24 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccafa06b5d6bae8fb8a7ae84a1199f6e15bc31c2717ac92beedf6b2f1039883a`  
		Last Modified: Wed, 10 May 2023 02:26:24 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23425226adb7ba000622950215070dd3ab86e9f23b15a2f9384e794fa32cb85c`  
		Last Modified: Wed, 10 May 2023 02:26:24 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
