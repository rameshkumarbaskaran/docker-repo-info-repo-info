## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:d30882b27e88c14f5c6ab99dd0b9e42b0714a72dae1042c3e60d550c0c82bdf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1726; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.1726; amd64

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
