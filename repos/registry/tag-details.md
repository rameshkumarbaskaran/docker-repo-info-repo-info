<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.7`](#registry27)
-	[`registry:2.7.1`](#registry271)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:da946ca03fca0aade04a73aa94b54ff0dc614216bdd1d47585f97b4c1bdaa0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:2` - linux; amd64

```console
$ docker pull registry@sha256:32150bb4704c0f9cf10599cb7fd7165841f73f1dfe4a96243e5e20e54f66e319
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9939366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4008a25e0565faf88dd3f060a8d7659f8c41c539a3ee9c693b05f08a13ebf9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 02:37:52 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 25 Feb 2021 02:37:52 GMT
COPY file:21256ff7df5369f7ad2e19c6d020a644303aded200bdbec4d46648f38d55df78 in /bin/registry 
# Thu, 25 Feb 2021 02:37:52 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 25 Feb 2021 02:37:53 GMT
VOLUME [/var/lib/registry]
# Thu, 25 Feb 2021 02:37:53 GMT
EXPOSE 5000
# Thu, 25 Feb 2021 02:37:53 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 25 Feb 2021 02:37:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 02:37:53 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7f2300f040df20ef1ac4ba68cf30b50a983312dab37d9f11ffb6bcdd125a96`  
		Last Modified: Thu, 25 Feb 2021 02:38:05 GMT  
		Size: 299.5 KB (299549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a7b7da390525be56ae8e7a5e96d376cabfee29f640566b58d6d39eeef40a7a`  
		Last Modified: Thu, 25 Feb 2021 02:38:08 GMT  
		Size: 6.8 MB (6823920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d656466e1fe8ae16ee516f95835bf63e6f117d7f14234cc96dea872c5ded5b51`  
		Last Modified: Thu, 25 Feb 2021 02:38:05 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cb731e4f93611fa1d8d87d8c8d7b0a13ee8c4f06ce07c353f58b6e591f36ed`  
		Last Modified: Thu, 25 Feb 2021 02:38:05 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm variant v6

```console
$ docker pull registry@sha256:4d6081e122a83f7e7af7a6c88c5c36d17af946c4367e332df88e2390cb148585
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea660224f682d39e1f577822c095f2fc01dfecd2e3689517c6b6150df544331a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:45 GMT
ADD file:72743cfd9913f13553e700f9d9cfdc17b9dc793ebeeb337fd5fe02dc962d4b63 in / 
# Wed, 24 Feb 2021 20:50:46 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 02:41:57 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 25 Feb 2021 02:41:58 GMT
COPY file:29c6c1625420a558a03cc7ed253192f8138cba6212b64e30217fb6488af668e2 in /bin/registry 
# Thu, 25 Feb 2021 02:41:59 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 25 Feb 2021 02:42:00 GMT
VOLUME [/var/lib/registry]
# Thu, 25 Feb 2021 02:42:00 GMT
EXPOSE 5000
# Thu, 25 Feb 2021 02:42:01 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 25 Feb 2021 02:42:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 02:42:03 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:10e3bc1a9288f315752811ab2f438cb080f27de72c30375566135a542c8e03a1`  
		Last Modified: Wed, 24 Feb 2021 20:51:26 GMT  
		Size: 2.6 MB (2621066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbda16690554a5be5df10780ab2655a8bdecf083b7c33ed1f7220d5497ee50f3`  
		Last Modified: Thu, 25 Feb 2021 02:42:19 GMT  
		Size: 299.9 KB (299922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c05e78117b2bce677952a4f42ea969058af216f9515e94ffc3943842147c0`  
		Last Modified: Thu, 25 Feb 2021 02:42:22 GMT  
		Size: 6.4 MB (6391085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a4e74ad0d5835ce9a80219d0f6c37dc63b1f50adaab2bbdc002cee6fb07312`  
		Last Modified: Thu, 25 Feb 2021 02:42:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1374117b827968a4aad9aff957acdf68658f4c3cb1b7c9cc0dcc8ea1f2a0cc`  
		Last Modified: Thu, 25 Feb 2021 02:42:19 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:912bba44e4c925687f11ff381bb220b6ad36591b45cf28a4db0be4bd182d95a3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9266695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a5db4d0baf50bcf98f2fc8f7aa3349b92f66367e21f39b28be256717af77a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 04:14:25 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 25 Feb 2021 04:14:26 GMT
COPY file:51a441e6eceff49ef32609e7070b64e8d5690648e4f915cc825274e6fe37aed2 in /bin/registry 
# Thu, 25 Feb 2021 04:14:27 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 25 Feb 2021 04:14:28 GMT
VOLUME [/var/lib/registry]
# Thu, 25 Feb 2021 04:14:30 GMT
EXPOSE 5000
# Thu, 25 Feb 2021 04:14:30 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 25 Feb 2021 04:14:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 04:14:33 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c76ffa81fc0ef1fc9110b987e901cc961916a142f2c95b7e392c1fbafe2c83`  
		Last Modified: Thu, 25 Feb 2021 04:14:46 GMT  
		Size: 300.1 KB (300067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0641e9a4962ce9f565852d7ff21a12a88f1608c521f789e9a34ec812b9227ac`  
		Last Modified: Thu, 25 Feb 2021 04:14:46 GMT  
		Size: 6.2 MB (6240200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792f7a0448903337485b204bc10d4eb4553fbc6d250fbd104a2c1b81b8edbb0f`  
		Last Modified: Thu, 25 Feb 2021 04:14:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdd90a0c21fc055951a3be8a799f795cb54f730e2b0961018cfe419f78895e5`  
		Last Modified: Thu, 25 Feb 2021 04:14:44 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.7`

```console
$ docker pull registry@sha256:da946ca03fca0aade04a73aa94b54ff0dc614216bdd1d47585f97b4c1bdaa0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:2.7` - linux; amd64

```console
$ docker pull registry@sha256:32150bb4704c0f9cf10599cb7fd7165841f73f1dfe4a96243e5e20e54f66e319
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9939366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4008a25e0565faf88dd3f060a8d7659f8c41c539a3ee9c693b05f08a13ebf9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 02:37:52 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 25 Feb 2021 02:37:52 GMT
COPY file:21256ff7df5369f7ad2e19c6d020a644303aded200bdbec4d46648f38d55df78 in /bin/registry 
# Thu, 25 Feb 2021 02:37:52 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 25 Feb 2021 02:37:53 GMT
VOLUME [/var/lib/registry]
# Thu, 25 Feb 2021 02:37:53 GMT
EXPOSE 5000
# Thu, 25 Feb 2021 02:37:53 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 25 Feb 2021 02:37:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 02:37:53 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7f2300f040df20ef1ac4ba68cf30b50a983312dab37d9f11ffb6bcdd125a96`  
		Last Modified: Thu, 25 Feb 2021 02:38:05 GMT  
		Size: 299.5 KB (299549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a7b7da390525be56ae8e7a5e96d376cabfee29f640566b58d6d39eeef40a7a`  
		Last Modified: Thu, 25 Feb 2021 02:38:08 GMT  
		Size: 6.8 MB (6823920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d656466e1fe8ae16ee516f95835bf63e6f117d7f14234cc96dea872c5ded5b51`  
		Last Modified: Thu, 25 Feb 2021 02:38:05 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cb731e4f93611fa1d8d87d8c8d7b0a13ee8c4f06ce07c353f58b6e591f36ed`  
		Last Modified: Thu, 25 Feb 2021 02:38:05 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.7` - linux; arm variant v6

```console
$ docker pull registry@sha256:4d6081e122a83f7e7af7a6c88c5c36d17af946c4367e332df88e2390cb148585
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea660224f682d39e1f577822c095f2fc01dfecd2e3689517c6b6150df544331a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:45 GMT
ADD file:72743cfd9913f13553e700f9d9cfdc17b9dc793ebeeb337fd5fe02dc962d4b63 in / 
# Wed, 24 Feb 2021 20:50:46 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 02:41:57 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 25 Feb 2021 02:41:58 GMT
COPY file:29c6c1625420a558a03cc7ed253192f8138cba6212b64e30217fb6488af668e2 in /bin/registry 
# Thu, 25 Feb 2021 02:41:59 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 25 Feb 2021 02:42:00 GMT
VOLUME [/var/lib/registry]
# Thu, 25 Feb 2021 02:42:00 GMT
EXPOSE 5000
# Thu, 25 Feb 2021 02:42:01 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 25 Feb 2021 02:42:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 02:42:03 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:10e3bc1a9288f315752811ab2f438cb080f27de72c30375566135a542c8e03a1`  
		Last Modified: Wed, 24 Feb 2021 20:51:26 GMT  
		Size: 2.6 MB (2621066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbda16690554a5be5df10780ab2655a8bdecf083b7c33ed1f7220d5497ee50f3`  
		Last Modified: Thu, 25 Feb 2021 02:42:19 GMT  
		Size: 299.9 KB (299922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c05e78117b2bce677952a4f42ea969058af216f9515e94ffc3943842147c0`  
		Last Modified: Thu, 25 Feb 2021 02:42:22 GMT  
		Size: 6.4 MB (6391085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a4e74ad0d5835ce9a80219d0f6c37dc63b1f50adaab2bbdc002cee6fb07312`  
		Last Modified: Thu, 25 Feb 2021 02:42:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1374117b827968a4aad9aff957acdf68658f4c3cb1b7c9cc0dcc8ea1f2a0cc`  
		Last Modified: Thu, 25 Feb 2021 02:42:19 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.7` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:912bba44e4c925687f11ff381bb220b6ad36591b45cf28a4db0be4bd182d95a3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9266695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a5db4d0baf50bcf98f2fc8f7aa3349b92f66367e21f39b28be256717af77a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 04:14:25 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 25 Feb 2021 04:14:26 GMT
COPY file:51a441e6eceff49ef32609e7070b64e8d5690648e4f915cc825274e6fe37aed2 in /bin/registry 
# Thu, 25 Feb 2021 04:14:27 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 25 Feb 2021 04:14:28 GMT
VOLUME [/var/lib/registry]
# Thu, 25 Feb 2021 04:14:30 GMT
EXPOSE 5000
# Thu, 25 Feb 2021 04:14:30 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 25 Feb 2021 04:14:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 04:14:33 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c76ffa81fc0ef1fc9110b987e901cc961916a142f2c95b7e392c1fbafe2c83`  
		Last Modified: Thu, 25 Feb 2021 04:14:46 GMT  
		Size: 300.1 KB (300067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0641e9a4962ce9f565852d7ff21a12a88f1608c521f789e9a34ec812b9227ac`  
		Last Modified: Thu, 25 Feb 2021 04:14:46 GMT  
		Size: 6.2 MB (6240200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792f7a0448903337485b204bc10d4eb4553fbc6d250fbd104a2c1b81b8edbb0f`  
		Last Modified: Thu, 25 Feb 2021 04:14:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdd90a0c21fc055951a3be8a799f795cb54f730e2b0961018cfe419f78895e5`  
		Last Modified: Thu, 25 Feb 2021 04:14:44 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.7.1`

```console
$ docker pull registry@sha256:da946ca03fca0aade04a73aa94b54ff0dc614216bdd1d47585f97b4c1bdaa0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:2.7.1` - linux; amd64

```console
$ docker pull registry@sha256:32150bb4704c0f9cf10599cb7fd7165841f73f1dfe4a96243e5e20e54f66e319
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9939366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4008a25e0565faf88dd3f060a8d7659f8c41c539a3ee9c693b05f08a13ebf9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 02:37:52 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 25 Feb 2021 02:37:52 GMT
COPY file:21256ff7df5369f7ad2e19c6d020a644303aded200bdbec4d46648f38d55df78 in /bin/registry 
# Thu, 25 Feb 2021 02:37:52 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 25 Feb 2021 02:37:53 GMT
VOLUME [/var/lib/registry]
# Thu, 25 Feb 2021 02:37:53 GMT
EXPOSE 5000
# Thu, 25 Feb 2021 02:37:53 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 25 Feb 2021 02:37:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 02:37:53 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7f2300f040df20ef1ac4ba68cf30b50a983312dab37d9f11ffb6bcdd125a96`  
		Last Modified: Thu, 25 Feb 2021 02:38:05 GMT  
		Size: 299.5 KB (299549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a7b7da390525be56ae8e7a5e96d376cabfee29f640566b58d6d39eeef40a7a`  
		Last Modified: Thu, 25 Feb 2021 02:38:08 GMT  
		Size: 6.8 MB (6823920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d656466e1fe8ae16ee516f95835bf63e6f117d7f14234cc96dea872c5ded5b51`  
		Last Modified: Thu, 25 Feb 2021 02:38:05 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cb731e4f93611fa1d8d87d8c8d7b0a13ee8c4f06ce07c353f58b6e591f36ed`  
		Last Modified: Thu, 25 Feb 2021 02:38:05 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.7.1` - linux; arm variant v6

```console
$ docker pull registry@sha256:4d6081e122a83f7e7af7a6c88c5c36d17af946c4367e332df88e2390cb148585
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea660224f682d39e1f577822c095f2fc01dfecd2e3689517c6b6150df544331a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:45 GMT
ADD file:72743cfd9913f13553e700f9d9cfdc17b9dc793ebeeb337fd5fe02dc962d4b63 in / 
# Wed, 24 Feb 2021 20:50:46 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 02:41:57 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 25 Feb 2021 02:41:58 GMT
COPY file:29c6c1625420a558a03cc7ed253192f8138cba6212b64e30217fb6488af668e2 in /bin/registry 
# Thu, 25 Feb 2021 02:41:59 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 25 Feb 2021 02:42:00 GMT
VOLUME [/var/lib/registry]
# Thu, 25 Feb 2021 02:42:00 GMT
EXPOSE 5000
# Thu, 25 Feb 2021 02:42:01 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 25 Feb 2021 02:42:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 02:42:03 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:10e3bc1a9288f315752811ab2f438cb080f27de72c30375566135a542c8e03a1`  
		Last Modified: Wed, 24 Feb 2021 20:51:26 GMT  
		Size: 2.6 MB (2621066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbda16690554a5be5df10780ab2655a8bdecf083b7c33ed1f7220d5497ee50f3`  
		Last Modified: Thu, 25 Feb 2021 02:42:19 GMT  
		Size: 299.9 KB (299922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c05e78117b2bce677952a4f42ea969058af216f9515e94ffc3943842147c0`  
		Last Modified: Thu, 25 Feb 2021 02:42:22 GMT  
		Size: 6.4 MB (6391085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a4e74ad0d5835ce9a80219d0f6c37dc63b1f50adaab2bbdc002cee6fb07312`  
		Last Modified: Thu, 25 Feb 2021 02:42:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1374117b827968a4aad9aff957acdf68658f4c3cb1b7c9cc0dcc8ea1f2a0cc`  
		Last Modified: Thu, 25 Feb 2021 02:42:19 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.7.1` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:912bba44e4c925687f11ff381bb220b6ad36591b45cf28a4db0be4bd182d95a3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9266695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a5db4d0baf50bcf98f2fc8f7aa3349b92f66367e21f39b28be256717af77a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 04:14:25 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 25 Feb 2021 04:14:26 GMT
COPY file:51a441e6eceff49ef32609e7070b64e8d5690648e4f915cc825274e6fe37aed2 in /bin/registry 
# Thu, 25 Feb 2021 04:14:27 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 25 Feb 2021 04:14:28 GMT
VOLUME [/var/lib/registry]
# Thu, 25 Feb 2021 04:14:30 GMT
EXPOSE 5000
# Thu, 25 Feb 2021 04:14:30 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 25 Feb 2021 04:14:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 04:14:33 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c76ffa81fc0ef1fc9110b987e901cc961916a142f2c95b7e392c1fbafe2c83`  
		Last Modified: Thu, 25 Feb 2021 04:14:46 GMT  
		Size: 300.1 KB (300067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0641e9a4962ce9f565852d7ff21a12a88f1608c521f789e9a34ec812b9227ac`  
		Last Modified: Thu, 25 Feb 2021 04:14:46 GMT  
		Size: 6.2 MB (6240200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792f7a0448903337485b204bc10d4eb4553fbc6d250fbd104a2c1b81b8edbb0f`  
		Last Modified: Thu, 25 Feb 2021 04:14:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdd90a0c21fc055951a3be8a799f795cb54f730e2b0961018cfe419f78895e5`  
		Last Modified: Thu, 25 Feb 2021 04:14:44 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:latest`

```console
$ docker pull registry@sha256:da946ca03fca0aade04a73aa94b54ff0dc614216bdd1d47585f97b4c1bdaa0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:latest` - linux; amd64

```console
$ docker pull registry@sha256:32150bb4704c0f9cf10599cb7fd7165841f73f1dfe4a96243e5e20e54f66e319
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9939366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4008a25e0565faf88dd3f060a8d7659f8c41c539a3ee9c693b05f08a13ebf9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 02:37:52 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 25 Feb 2021 02:37:52 GMT
COPY file:21256ff7df5369f7ad2e19c6d020a644303aded200bdbec4d46648f38d55df78 in /bin/registry 
# Thu, 25 Feb 2021 02:37:52 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 25 Feb 2021 02:37:53 GMT
VOLUME [/var/lib/registry]
# Thu, 25 Feb 2021 02:37:53 GMT
EXPOSE 5000
# Thu, 25 Feb 2021 02:37:53 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 25 Feb 2021 02:37:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 02:37:53 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7f2300f040df20ef1ac4ba68cf30b50a983312dab37d9f11ffb6bcdd125a96`  
		Last Modified: Thu, 25 Feb 2021 02:38:05 GMT  
		Size: 299.5 KB (299549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a7b7da390525be56ae8e7a5e96d376cabfee29f640566b58d6d39eeef40a7a`  
		Last Modified: Thu, 25 Feb 2021 02:38:08 GMT  
		Size: 6.8 MB (6823920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d656466e1fe8ae16ee516f95835bf63e6f117d7f14234cc96dea872c5ded5b51`  
		Last Modified: Thu, 25 Feb 2021 02:38:05 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cb731e4f93611fa1d8d87d8c8d7b0a13ee8c4f06ce07c353f58b6e591f36ed`  
		Last Modified: Thu, 25 Feb 2021 02:38:05 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:4d6081e122a83f7e7af7a6c88c5c36d17af946c4367e332df88e2390cb148585
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea660224f682d39e1f577822c095f2fc01dfecd2e3689517c6b6150df544331a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:45 GMT
ADD file:72743cfd9913f13553e700f9d9cfdc17b9dc793ebeeb337fd5fe02dc962d4b63 in / 
# Wed, 24 Feb 2021 20:50:46 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 02:41:57 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 25 Feb 2021 02:41:58 GMT
COPY file:29c6c1625420a558a03cc7ed253192f8138cba6212b64e30217fb6488af668e2 in /bin/registry 
# Thu, 25 Feb 2021 02:41:59 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 25 Feb 2021 02:42:00 GMT
VOLUME [/var/lib/registry]
# Thu, 25 Feb 2021 02:42:00 GMT
EXPOSE 5000
# Thu, 25 Feb 2021 02:42:01 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 25 Feb 2021 02:42:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 02:42:03 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:10e3bc1a9288f315752811ab2f438cb080f27de72c30375566135a542c8e03a1`  
		Last Modified: Wed, 24 Feb 2021 20:51:26 GMT  
		Size: 2.6 MB (2621066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbda16690554a5be5df10780ab2655a8bdecf083b7c33ed1f7220d5497ee50f3`  
		Last Modified: Thu, 25 Feb 2021 02:42:19 GMT  
		Size: 299.9 KB (299922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c05e78117b2bce677952a4f42ea969058af216f9515e94ffc3943842147c0`  
		Last Modified: Thu, 25 Feb 2021 02:42:22 GMT  
		Size: 6.4 MB (6391085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a4e74ad0d5835ce9a80219d0f6c37dc63b1f50adaab2bbdc002cee6fb07312`  
		Last Modified: Thu, 25 Feb 2021 02:42:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1374117b827968a4aad9aff957acdf68658f4c3cb1b7c9cc0dcc8ea1f2a0cc`  
		Last Modified: Thu, 25 Feb 2021 02:42:19 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:912bba44e4c925687f11ff381bb220b6ad36591b45cf28a4db0be4bd182d95a3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9266695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a5db4d0baf50bcf98f2fc8f7aa3349b92f66367e21f39b28be256717af77a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 04:14:25 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 25 Feb 2021 04:14:26 GMT
COPY file:51a441e6eceff49ef32609e7070b64e8d5690648e4f915cc825274e6fe37aed2 in /bin/registry 
# Thu, 25 Feb 2021 04:14:27 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 25 Feb 2021 04:14:28 GMT
VOLUME [/var/lib/registry]
# Thu, 25 Feb 2021 04:14:30 GMT
EXPOSE 5000
# Thu, 25 Feb 2021 04:14:30 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 25 Feb 2021 04:14:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 04:14:33 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c76ffa81fc0ef1fc9110b987e901cc961916a142f2c95b7e392c1fbafe2c83`  
		Last Modified: Thu, 25 Feb 2021 04:14:46 GMT  
		Size: 300.1 KB (300067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0641e9a4962ce9f565852d7ff21a12a88f1608c521f789e9a34ec812b9227ac`  
		Last Modified: Thu, 25 Feb 2021 04:14:46 GMT  
		Size: 6.2 MB (6240200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792f7a0448903337485b204bc10d4eb4553fbc6d250fbd104a2c1b81b8edbb0f`  
		Last Modified: Thu, 25 Feb 2021 04:14:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdd90a0c21fc055951a3be8a799f795cb54f730e2b0961018cfe419f78895e5`  
		Last Modified: Thu, 25 Feb 2021 04:14:44 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
