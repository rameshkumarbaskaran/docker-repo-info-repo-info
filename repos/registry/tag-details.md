<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.7`](#registry27)
-	[`registry:2.7.1`](#registry271)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:800b754ced52e629ad2d14092f82ce3824029708f50c95080ba799ea6356c6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:2` - linux; amd64

```console
$ docker pull registry@sha256:1d1c3a2624c16a916e8a7d891e155edf35614e78034f784a37bf73ff3a7bfd6e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9939493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefcac9e385600903a7d9aecbbd9ac7c88af61f4ef68993ff11039656eaa7a1b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:09:27 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Fri, 26 Mar 2021 08:09:27 GMT
COPY file:21256ff7df5369f7ad2e19c6d020a644303aded200bdbec4d46648f38d55df78 in /bin/registry 
# Fri, 26 Mar 2021 08:09:27 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 26 Mar 2021 08:09:28 GMT
VOLUME [/var/lib/registry]
# Fri, 26 Mar 2021 08:09:28 GMT
EXPOSE 5000
# Fri, 26 Mar 2021 08:09:28 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 26 Mar 2021 08:09:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:09:28 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1d0edb7ed924c231547f37487ec3fb1ba8837fa94b68bfdf5a57b07f350141`  
		Last Modified: Fri, 26 Mar 2021 08:09:39 GMT  
		Size: 299.6 KB (299622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a3564df80253da16a1a28f17cba5230c86f7e23aaeac0e82128d51771a12ff`  
		Last Modified: Fri, 26 Mar 2021 08:09:41 GMT  
		Size: 6.8 MB (6823927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655e20670f83cb2413fb5e27208a994b0331018434908846dd6c9f8e663bdcb3`  
		Last Modified: Fri, 26 Mar 2021 08:09:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b9efe22f2dd04f2a57f4f8d9e50486719771ca26afce1b4ff0c1e9554f464c`  
		Last Modified: Fri, 26 Mar 2021 08:09:39 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm variant v6

```console
$ docker pull registry@sha256:82b4ae365aa03c555c6ec69e2fe60964b829a9252775a487fbceabc2d49bcca4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db2d18a4dc279a653234ceb0c949c45dbb152c956023d679d94b2fddf188b75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:20 GMT
ADD file:15a1f9d3700deb648f0b3701afebc97ff28eb30d1b55e18dc9c696a9dd5c8e36 in / 
# Wed, 31 Mar 2021 17:19:21 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 03:03:13 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 01 Apr 2021 03:03:15 GMT
COPY file:29c6c1625420a558a03cc7ed253192f8138cba6212b64e30217fb6488af668e2 in /bin/registry 
# Thu, 01 Apr 2021 03:03:16 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 01 Apr 2021 03:03:17 GMT
VOLUME [/var/lib/registry]
# Thu, 01 Apr 2021 03:03:18 GMT
EXPOSE 5000
# Thu, 01 Apr 2021 03:03:19 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 01 Apr 2021 03:03:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 03:03:21 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:ac95243af174972febc49043f62f7b952a0c610e59b55ac4133f442e399e8729`  
		Last Modified: Wed, 31 Mar 2021 17:20:17 GMT  
		Size: 2.6 MB (2621248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81abd9ad682b4554d8eef9a3e45d373886c1e3aa52c33febc1fb42c1a41099e3`  
		Last Modified: Thu, 01 Apr 2021 03:03:38 GMT  
		Size: 299.9 KB (299934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c16d1e58d4635a248334fe48ce9dc26dbddd3b86b905b2c0375ddd11aa24ef`  
		Last Modified: Thu, 01 Apr 2021 03:03:40 GMT  
		Size: 6.4 MB (6391088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d3d6fc8a860cb1c030a937de0e4330791152d68acfa11aff172fc74d6b1500`  
		Last Modified: Thu, 01 Apr 2021 03:03:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1a5d247010eed566ec69e2a0949843b89441c5b0128383c1e699ee07cf1434`  
		Last Modified: Thu, 01 Apr 2021 03:03:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:e1c3c139d506e6e2e7ceb97d00a898f2fbcea03d6ea0881253675461e56a24f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9266764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5c4f51945c01a05fddbce4fb0cf23021c7b9d8d64c39efefeafbb14498add5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:33 GMT
ADD file:6fca680ab44d711c282deb126e7ad2f7ab51d84a6364192a4913e178f7d393a0 in / 
# Thu, 25 Mar 2021 22:41:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 11:54:47 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Fri, 26 Mar 2021 11:54:49 GMT
COPY file:51a441e6eceff49ef32609e7070b64e8d5690648e4f915cc825274e6fe37aed2 in /bin/registry 
# Fri, 26 Mar 2021 11:54:52 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 26 Mar 2021 11:54:56 GMT
VOLUME [/var/lib/registry]
# Fri, 26 Mar 2021 11:54:57 GMT
EXPOSE 5000
# Fri, 26 Mar 2021 11:54:58 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 26 Mar 2021 11:54:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 11:55:00 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:47185b9379cb432a7a6711ec279fdcb33fe0426be145e1bf61879568c9b54054`  
		Last Modified: Thu, 25 Mar 2021 22:45:46 GMT  
		Size: 2.7 MB (2725878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec72d2e2b64072c3e30be3439e45c34fbf8494174a0f0fb813c6d1810b1b606`  
		Last Modified: Fri, 26 Mar 2021 11:55:15 GMT  
		Size: 300.1 KB (300072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1b5970263d73c106de36d69135b7c3698c73ffcf20bd032169541b633ab2bd`  
		Last Modified: Fri, 26 Mar 2021 11:55:15 GMT  
		Size: 6.2 MB (6240199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38679773c4d8c723aa0753c2ef3de1cff4de856ef9fb0d4c2c6c8d79b2e86eec`  
		Last Modified: Fri, 26 Mar 2021 11:55:13 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e4aa7bb1688c41eba4a7f3a39ba78dd74cb57f92f7a93b17c33dca38c6f31f`  
		Last Modified: Fri, 26 Mar 2021 11:55:16 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.7`

```console
$ docker pull registry@sha256:800b754ced52e629ad2d14092f82ce3824029708f50c95080ba799ea6356c6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:2.7` - linux; amd64

```console
$ docker pull registry@sha256:1d1c3a2624c16a916e8a7d891e155edf35614e78034f784a37bf73ff3a7bfd6e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9939493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefcac9e385600903a7d9aecbbd9ac7c88af61f4ef68993ff11039656eaa7a1b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:09:27 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Fri, 26 Mar 2021 08:09:27 GMT
COPY file:21256ff7df5369f7ad2e19c6d020a644303aded200bdbec4d46648f38d55df78 in /bin/registry 
# Fri, 26 Mar 2021 08:09:27 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 26 Mar 2021 08:09:28 GMT
VOLUME [/var/lib/registry]
# Fri, 26 Mar 2021 08:09:28 GMT
EXPOSE 5000
# Fri, 26 Mar 2021 08:09:28 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 26 Mar 2021 08:09:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:09:28 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1d0edb7ed924c231547f37487ec3fb1ba8837fa94b68bfdf5a57b07f350141`  
		Last Modified: Fri, 26 Mar 2021 08:09:39 GMT  
		Size: 299.6 KB (299622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a3564df80253da16a1a28f17cba5230c86f7e23aaeac0e82128d51771a12ff`  
		Last Modified: Fri, 26 Mar 2021 08:09:41 GMT  
		Size: 6.8 MB (6823927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655e20670f83cb2413fb5e27208a994b0331018434908846dd6c9f8e663bdcb3`  
		Last Modified: Fri, 26 Mar 2021 08:09:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b9efe22f2dd04f2a57f4f8d9e50486719771ca26afce1b4ff0c1e9554f464c`  
		Last Modified: Fri, 26 Mar 2021 08:09:39 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.7` - linux; arm variant v6

```console
$ docker pull registry@sha256:82b4ae365aa03c555c6ec69e2fe60964b829a9252775a487fbceabc2d49bcca4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db2d18a4dc279a653234ceb0c949c45dbb152c956023d679d94b2fddf188b75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:20 GMT
ADD file:15a1f9d3700deb648f0b3701afebc97ff28eb30d1b55e18dc9c696a9dd5c8e36 in / 
# Wed, 31 Mar 2021 17:19:21 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 03:03:13 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 01 Apr 2021 03:03:15 GMT
COPY file:29c6c1625420a558a03cc7ed253192f8138cba6212b64e30217fb6488af668e2 in /bin/registry 
# Thu, 01 Apr 2021 03:03:16 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 01 Apr 2021 03:03:17 GMT
VOLUME [/var/lib/registry]
# Thu, 01 Apr 2021 03:03:18 GMT
EXPOSE 5000
# Thu, 01 Apr 2021 03:03:19 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 01 Apr 2021 03:03:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 03:03:21 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:ac95243af174972febc49043f62f7b952a0c610e59b55ac4133f442e399e8729`  
		Last Modified: Wed, 31 Mar 2021 17:20:17 GMT  
		Size: 2.6 MB (2621248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81abd9ad682b4554d8eef9a3e45d373886c1e3aa52c33febc1fb42c1a41099e3`  
		Last Modified: Thu, 01 Apr 2021 03:03:38 GMT  
		Size: 299.9 KB (299934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c16d1e58d4635a248334fe48ce9dc26dbddd3b86b905b2c0375ddd11aa24ef`  
		Last Modified: Thu, 01 Apr 2021 03:03:40 GMT  
		Size: 6.4 MB (6391088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d3d6fc8a860cb1c030a937de0e4330791152d68acfa11aff172fc74d6b1500`  
		Last Modified: Thu, 01 Apr 2021 03:03:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1a5d247010eed566ec69e2a0949843b89441c5b0128383c1e699ee07cf1434`  
		Last Modified: Thu, 01 Apr 2021 03:03:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.7` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:e1c3c139d506e6e2e7ceb97d00a898f2fbcea03d6ea0881253675461e56a24f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9266764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5c4f51945c01a05fddbce4fb0cf23021c7b9d8d64c39efefeafbb14498add5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:33 GMT
ADD file:6fca680ab44d711c282deb126e7ad2f7ab51d84a6364192a4913e178f7d393a0 in / 
# Thu, 25 Mar 2021 22:41:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 11:54:47 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Fri, 26 Mar 2021 11:54:49 GMT
COPY file:51a441e6eceff49ef32609e7070b64e8d5690648e4f915cc825274e6fe37aed2 in /bin/registry 
# Fri, 26 Mar 2021 11:54:52 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 26 Mar 2021 11:54:56 GMT
VOLUME [/var/lib/registry]
# Fri, 26 Mar 2021 11:54:57 GMT
EXPOSE 5000
# Fri, 26 Mar 2021 11:54:58 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 26 Mar 2021 11:54:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 11:55:00 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:47185b9379cb432a7a6711ec279fdcb33fe0426be145e1bf61879568c9b54054`  
		Last Modified: Thu, 25 Mar 2021 22:45:46 GMT  
		Size: 2.7 MB (2725878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec72d2e2b64072c3e30be3439e45c34fbf8494174a0f0fb813c6d1810b1b606`  
		Last Modified: Fri, 26 Mar 2021 11:55:15 GMT  
		Size: 300.1 KB (300072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1b5970263d73c106de36d69135b7c3698c73ffcf20bd032169541b633ab2bd`  
		Last Modified: Fri, 26 Mar 2021 11:55:15 GMT  
		Size: 6.2 MB (6240199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38679773c4d8c723aa0753c2ef3de1cff4de856ef9fb0d4c2c6c8d79b2e86eec`  
		Last Modified: Fri, 26 Mar 2021 11:55:13 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e4aa7bb1688c41eba4a7f3a39ba78dd74cb57f92f7a93b17c33dca38c6f31f`  
		Last Modified: Fri, 26 Mar 2021 11:55:16 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.7.1`

```console
$ docker pull registry@sha256:800b754ced52e629ad2d14092f82ce3824029708f50c95080ba799ea6356c6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:2.7.1` - linux; amd64

```console
$ docker pull registry@sha256:1d1c3a2624c16a916e8a7d891e155edf35614e78034f784a37bf73ff3a7bfd6e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9939493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefcac9e385600903a7d9aecbbd9ac7c88af61f4ef68993ff11039656eaa7a1b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:09:27 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Fri, 26 Mar 2021 08:09:27 GMT
COPY file:21256ff7df5369f7ad2e19c6d020a644303aded200bdbec4d46648f38d55df78 in /bin/registry 
# Fri, 26 Mar 2021 08:09:27 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 26 Mar 2021 08:09:28 GMT
VOLUME [/var/lib/registry]
# Fri, 26 Mar 2021 08:09:28 GMT
EXPOSE 5000
# Fri, 26 Mar 2021 08:09:28 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 26 Mar 2021 08:09:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:09:28 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1d0edb7ed924c231547f37487ec3fb1ba8837fa94b68bfdf5a57b07f350141`  
		Last Modified: Fri, 26 Mar 2021 08:09:39 GMT  
		Size: 299.6 KB (299622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a3564df80253da16a1a28f17cba5230c86f7e23aaeac0e82128d51771a12ff`  
		Last Modified: Fri, 26 Mar 2021 08:09:41 GMT  
		Size: 6.8 MB (6823927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655e20670f83cb2413fb5e27208a994b0331018434908846dd6c9f8e663bdcb3`  
		Last Modified: Fri, 26 Mar 2021 08:09:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b9efe22f2dd04f2a57f4f8d9e50486719771ca26afce1b4ff0c1e9554f464c`  
		Last Modified: Fri, 26 Mar 2021 08:09:39 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.7.1` - linux; arm variant v6

```console
$ docker pull registry@sha256:82b4ae365aa03c555c6ec69e2fe60964b829a9252775a487fbceabc2d49bcca4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db2d18a4dc279a653234ceb0c949c45dbb152c956023d679d94b2fddf188b75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:20 GMT
ADD file:15a1f9d3700deb648f0b3701afebc97ff28eb30d1b55e18dc9c696a9dd5c8e36 in / 
# Wed, 31 Mar 2021 17:19:21 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 03:03:13 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 01 Apr 2021 03:03:15 GMT
COPY file:29c6c1625420a558a03cc7ed253192f8138cba6212b64e30217fb6488af668e2 in /bin/registry 
# Thu, 01 Apr 2021 03:03:16 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 01 Apr 2021 03:03:17 GMT
VOLUME [/var/lib/registry]
# Thu, 01 Apr 2021 03:03:18 GMT
EXPOSE 5000
# Thu, 01 Apr 2021 03:03:19 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 01 Apr 2021 03:03:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 03:03:21 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:ac95243af174972febc49043f62f7b952a0c610e59b55ac4133f442e399e8729`  
		Last Modified: Wed, 31 Mar 2021 17:20:17 GMT  
		Size: 2.6 MB (2621248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81abd9ad682b4554d8eef9a3e45d373886c1e3aa52c33febc1fb42c1a41099e3`  
		Last Modified: Thu, 01 Apr 2021 03:03:38 GMT  
		Size: 299.9 KB (299934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c16d1e58d4635a248334fe48ce9dc26dbddd3b86b905b2c0375ddd11aa24ef`  
		Last Modified: Thu, 01 Apr 2021 03:03:40 GMT  
		Size: 6.4 MB (6391088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d3d6fc8a860cb1c030a937de0e4330791152d68acfa11aff172fc74d6b1500`  
		Last Modified: Thu, 01 Apr 2021 03:03:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1a5d247010eed566ec69e2a0949843b89441c5b0128383c1e699ee07cf1434`  
		Last Modified: Thu, 01 Apr 2021 03:03:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.7.1` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:e1c3c139d506e6e2e7ceb97d00a898f2fbcea03d6ea0881253675461e56a24f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9266764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5c4f51945c01a05fddbce4fb0cf23021c7b9d8d64c39efefeafbb14498add5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:33 GMT
ADD file:6fca680ab44d711c282deb126e7ad2f7ab51d84a6364192a4913e178f7d393a0 in / 
# Thu, 25 Mar 2021 22:41:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 11:54:47 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Fri, 26 Mar 2021 11:54:49 GMT
COPY file:51a441e6eceff49ef32609e7070b64e8d5690648e4f915cc825274e6fe37aed2 in /bin/registry 
# Fri, 26 Mar 2021 11:54:52 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 26 Mar 2021 11:54:56 GMT
VOLUME [/var/lib/registry]
# Fri, 26 Mar 2021 11:54:57 GMT
EXPOSE 5000
# Fri, 26 Mar 2021 11:54:58 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 26 Mar 2021 11:54:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 11:55:00 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:47185b9379cb432a7a6711ec279fdcb33fe0426be145e1bf61879568c9b54054`  
		Last Modified: Thu, 25 Mar 2021 22:45:46 GMT  
		Size: 2.7 MB (2725878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec72d2e2b64072c3e30be3439e45c34fbf8494174a0f0fb813c6d1810b1b606`  
		Last Modified: Fri, 26 Mar 2021 11:55:15 GMT  
		Size: 300.1 KB (300072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1b5970263d73c106de36d69135b7c3698c73ffcf20bd032169541b633ab2bd`  
		Last Modified: Fri, 26 Mar 2021 11:55:15 GMT  
		Size: 6.2 MB (6240199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38679773c4d8c723aa0753c2ef3de1cff4de856ef9fb0d4c2c6c8d79b2e86eec`  
		Last Modified: Fri, 26 Mar 2021 11:55:13 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e4aa7bb1688c41eba4a7f3a39ba78dd74cb57f92f7a93b17c33dca38c6f31f`  
		Last Modified: Fri, 26 Mar 2021 11:55:16 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:latest`

```console
$ docker pull registry@sha256:800b754ced52e629ad2d14092f82ce3824029708f50c95080ba799ea6356c6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:latest` - linux; amd64

```console
$ docker pull registry@sha256:1d1c3a2624c16a916e8a7d891e155edf35614e78034f784a37bf73ff3a7bfd6e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9939493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefcac9e385600903a7d9aecbbd9ac7c88af61f4ef68993ff11039656eaa7a1b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:09:27 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Fri, 26 Mar 2021 08:09:27 GMT
COPY file:21256ff7df5369f7ad2e19c6d020a644303aded200bdbec4d46648f38d55df78 in /bin/registry 
# Fri, 26 Mar 2021 08:09:27 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 26 Mar 2021 08:09:28 GMT
VOLUME [/var/lib/registry]
# Fri, 26 Mar 2021 08:09:28 GMT
EXPOSE 5000
# Fri, 26 Mar 2021 08:09:28 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 26 Mar 2021 08:09:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:09:28 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1d0edb7ed924c231547f37487ec3fb1ba8837fa94b68bfdf5a57b07f350141`  
		Last Modified: Fri, 26 Mar 2021 08:09:39 GMT  
		Size: 299.6 KB (299622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a3564df80253da16a1a28f17cba5230c86f7e23aaeac0e82128d51771a12ff`  
		Last Modified: Fri, 26 Mar 2021 08:09:41 GMT  
		Size: 6.8 MB (6823927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655e20670f83cb2413fb5e27208a994b0331018434908846dd6c9f8e663bdcb3`  
		Last Modified: Fri, 26 Mar 2021 08:09:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b9efe22f2dd04f2a57f4f8d9e50486719771ca26afce1b4ff0c1e9554f464c`  
		Last Modified: Fri, 26 Mar 2021 08:09:39 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:82b4ae365aa03c555c6ec69e2fe60964b829a9252775a487fbceabc2d49bcca4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db2d18a4dc279a653234ceb0c949c45dbb152c956023d679d94b2fddf188b75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:20 GMT
ADD file:15a1f9d3700deb648f0b3701afebc97ff28eb30d1b55e18dc9c696a9dd5c8e36 in / 
# Wed, 31 Mar 2021 17:19:21 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 03:03:13 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 01 Apr 2021 03:03:15 GMT
COPY file:29c6c1625420a558a03cc7ed253192f8138cba6212b64e30217fb6488af668e2 in /bin/registry 
# Thu, 01 Apr 2021 03:03:16 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 01 Apr 2021 03:03:17 GMT
VOLUME [/var/lib/registry]
# Thu, 01 Apr 2021 03:03:18 GMT
EXPOSE 5000
# Thu, 01 Apr 2021 03:03:19 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 01 Apr 2021 03:03:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 03:03:21 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:ac95243af174972febc49043f62f7b952a0c610e59b55ac4133f442e399e8729`  
		Last Modified: Wed, 31 Mar 2021 17:20:17 GMT  
		Size: 2.6 MB (2621248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81abd9ad682b4554d8eef9a3e45d373886c1e3aa52c33febc1fb42c1a41099e3`  
		Last Modified: Thu, 01 Apr 2021 03:03:38 GMT  
		Size: 299.9 KB (299934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c16d1e58d4635a248334fe48ce9dc26dbddd3b86b905b2c0375ddd11aa24ef`  
		Last Modified: Thu, 01 Apr 2021 03:03:40 GMT  
		Size: 6.4 MB (6391088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d3d6fc8a860cb1c030a937de0e4330791152d68acfa11aff172fc74d6b1500`  
		Last Modified: Thu, 01 Apr 2021 03:03:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1a5d247010eed566ec69e2a0949843b89441c5b0128383c1e699ee07cf1434`  
		Last Modified: Thu, 01 Apr 2021 03:03:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:e1c3c139d506e6e2e7ceb97d00a898f2fbcea03d6ea0881253675461e56a24f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9266764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5c4f51945c01a05fddbce4fb0cf23021c7b9d8d64c39efefeafbb14498add5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:33 GMT
ADD file:6fca680ab44d711c282deb126e7ad2f7ab51d84a6364192a4913e178f7d393a0 in / 
# Thu, 25 Mar 2021 22:41:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 11:54:47 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Fri, 26 Mar 2021 11:54:49 GMT
COPY file:51a441e6eceff49ef32609e7070b64e8d5690648e4f915cc825274e6fe37aed2 in /bin/registry 
# Fri, 26 Mar 2021 11:54:52 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 26 Mar 2021 11:54:56 GMT
VOLUME [/var/lib/registry]
# Fri, 26 Mar 2021 11:54:57 GMT
EXPOSE 5000
# Fri, 26 Mar 2021 11:54:58 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 26 Mar 2021 11:54:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 11:55:00 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:47185b9379cb432a7a6711ec279fdcb33fe0426be145e1bf61879568c9b54054`  
		Last Modified: Thu, 25 Mar 2021 22:45:46 GMT  
		Size: 2.7 MB (2725878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec72d2e2b64072c3e30be3439e45c34fbf8494174a0f0fb813c6d1810b1b606`  
		Last Modified: Fri, 26 Mar 2021 11:55:15 GMT  
		Size: 300.1 KB (300072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1b5970263d73c106de36d69135b7c3698c73ffcf20bd032169541b633ab2bd`  
		Last Modified: Fri, 26 Mar 2021 11:55:15 GMT  
		Size: 6.2 MB (6240199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38679773c4d8c723aa0753c2ef3de1cff4de856ef9fb0d4c2c6c8d79b2e86eec`  
		Last Modified: Fri, 26 Mar 2021 11:55:13 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e4aa7bb1688c41eba4a7f3a39ba78dd74cb57f92f7a93b17c33dca38c6f31f`  
		Last Modified: Fri, 26 Mar 2021 11:55:16 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
