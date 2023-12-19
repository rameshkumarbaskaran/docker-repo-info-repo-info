## `debian:buster-backports`

```console
$ docker pull debian@sha256:20cdc1d1f65d534de019d11e1c79ca1dc925be1e66c8b7ac0e6807f8dd405d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:da59c0713047f173d625de65f972229fa5e42127a1bead7fd96c242522545edc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50500631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9257fede6e22e0bb98d0fe8e4a62f2e7cae81397e618e61e2f06742313f33a8e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:00 GMT
ADD file:e5e3f2fedf4fa6382f3bbf6203060ba68df1aadc7ebfa3350df20bf31b102f0e in / 
# Tue, 19 Dec 2023 01:21:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:21:05 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:30b73a2ffaab3c39355a8bcc5eae8ba1465bd7d9467f197b91f7635816b16bc9`  
		Last Modified: Tue, 19 Dec 2023 01:25:58 GMT  
		Size: 50.5 MB (50500409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4177c7067fd6836dab02806de0ed6c48bf684fb1975253819425bda29cdbc971`  
		Last Modified: Tue, 19 Dec 2023 01:26:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b6c70e145a58d84eca06af8882f2248a355684a780c8ec0a66e58b3c03e42bf6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45966534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b2cf67cd7b10d6d8424731ab620b951dcb61b9b690137345755114d91d775c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:12 GMT
ADD file:e69e944c7b28ca650586e3fa2bcb51c4c99491167bee97c4ab32982eeab66750 in / 
# Tue, 21 Nov 2023 03:58:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 03:58:16 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:859d411365ce23ca0a7fbddedc1babff0039e814c09756ad01c59527ebe62dc8`  
		Last Modified: Tue, 21 Nov 2023 04:02:56 GMT  
		Size: 46.0 MB (45966309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db21155347660f4290e33e6572b395c7f099c20f9cff08a9e238a7284db2eb`  
		Last Modified: Tue, 21 Nov 2023 04:03:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1c77de54f6f1c12bd38c58f179abdac38bb5c376b29e460bac7ba945ebd7d23d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49289251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73eb7505ae5caf0414acf2242d687fb3095144312448774c744c1be2abba80d5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:31 GMT
ADD file:df5e5dd39efc6ae3cc9132f6ca6bb569731f7a37cf4b41f87bcb7aa1ba9771e8 in / 
# Tue, 19 Dec 2023 01:41:32 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:41:35 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:93507f9712ced9fbfd0d0f689cf7b55fb245cef88530c07ac5dc5cad20fa889d`  
		Last Modified: Tue, 19 Dec 2023 01:45:40 GMT  
		Size: 49.3 MB (49289026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82067abbc6b5b11fe6057efec57a46492fd1fa6c32a2e257260981d611d84a9`  
		Last Modified: Tue, 19 Dec 2023 01:45:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:b7cca81af931a9a67b69983ccbad605b1f20c201035c7f829044ae883d96140b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51255667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e45d16423a3379571bfb3710d0d2a7599b6b581757d1153adb61d54dce1183`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:40 GMT
ADD file:4c009b0d408e3df297246382d87b0be68c34886e13ed79ba47feb8ff51acb863 in / 
# Tue, 19 Dec 2023 01:39:41 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:39:45 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8d351f5ab6958b8ca5f2b8e463c49cba65be4285ead8bdbc1378b5ce2c8cd736`  
		Last Modified: Tue, 19 Dec 2023 01:44:53 GMT  
		Size: 51.3 MB (51255444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff5556c29a9face04d75d0b30221084868d4e4b09845a4f46267f944c2412ec`  
		Last Modified: Tue, 19 Dec 2023 01:45:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
