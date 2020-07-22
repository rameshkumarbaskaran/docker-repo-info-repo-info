## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:15a1341d2d9c8fc1efd1432b40c3bf7f8abb6719951adbd7c0575ea7cddd797b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:df524c6d24f69deaa111ef5fb1594e40d34e015fed331d4df52d8780ba3020c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68198346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25206ac5e74a4b465c3a613fadb7c862b5303d045e91cb9ffe3dad6b8afe7c1f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:16 GMT
ADD file:89dfd7d3ed77fd5e05f20a0ab631142207ae462f5bbd877f8745d3930c751d87 in / 
# Wed, 22 Jul 2020 02:03:16 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:00:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:00:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:31dd5ebca5efc5e96a425402fa85e492b02c8fe757dfd3edfdea2a7c67322909`  
		Last Modified: Wed, 22 Jul 2020 02:09:37 GMT  
		Size: 50.4 MB (50390325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed641c4ae9821ca3c399071ea82ae667237acbcaad1e367c3e1e87fc967834c`  
		Last Modified: Wed, 22 Jul 2020 03:16:28 GMT  
		Size: 7.8 MB (7811702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd57146431eae70720cf24877e818256ae1a30b9c1c9e7d0ad093c945ca0af2`  
		Last Modified: Wed, 22 Jul 2020 03:16:28 GMT  
		Size: 10.0 MB (9996319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d61a90253c38f5646426a83d901a833adef1d2b850acb5962b96fe1891df9427
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65155247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67b22e3a41a555c19f2b7a6d607793def9b647f0729f6342a2045b8a45ff260`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:50:16 GMT
ADD file:0431730a3850ee2a710a03ba04d05224938cf2f5318e1f73ed74677c70d09b78 in / 
# Wed, 22 Jul 2020 00:50:20 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:31:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:32:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:71cf5632cfeb30dc5a7a7ccd4742a02af636cd970ef3a45bebc17d3f20b3662d`  
		Last Modified: Wed, 22 Jul 2020 00:58:30 GMT  
		Size: 48.1 MB (48107278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87dffc06540f2eca873274114a3d8d49684b38428e946f67b0b62aa848ae49c`  
		Last Modified: Wed, 22 Jul 2020 02:02:59 GMT  
		Size: 7.4 MB (7360981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad12a2dc68e08e793efc12362e49a16257506721c8074ee8361c242244763bc4`  
		Last Modified: Wed, 22 Jul 2020 02:03:00 GMT  
		Size: 9.7 MB (9686988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4f4aab80df9009ff0a106345efd92926c59c0571b89a4ed806318eb5b872703e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62310333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c03614e2279aecfc842806ab7ff441c5cd288ae76ac0eae69d3e1df66af07ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:00:40 GMT
ADD file:35073a186411c4b773a9d4d540ec0693ced845cb847b43d8465f9579174cd2b0 in / 
# Tue, 09 Jun 2020 01:00:45 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cff0731da2e4f4a0ae8329840eb7fed7ea6aac11aecbfa15c6e684caec03920d`  
		Last Modified: Tue, 09 Jun 2020 01:09:57 GMT  
		Size: 45.9 MB (45868949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbeb0ded58d68be17265763fda36a4e1a520234a291d66f370d98a3e0d6e591`  
		Last Modified: Tue, 09 Jun 2020 02:11:21 GMT  
		Size: 7.1 MB (7097860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6159fbed770bb99a219eae06828da55caaa649879843c0b9df18ddda9b698b3`  
		Last Modified: Tue, 09 Jun 2020 02:11:20 GMT  
		Size: 9.3 MB (9343524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:afa9acf2e7ff9ceaaa9497fb899b7e9bcd7a5f236b4d297d4514c23dfe1c1924
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66833783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff98a414c56ef4a518274c2440049de2837ee4b729ca85f6dc693379e9ab0f6d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:40:37 GMT
ADD file:14b8dca0bc0e6dae2f0bdb018a3a4e6d8d041abd03d118ae27cf7a72668f4970 in / 
# Wed, 22 Jul 2020 00:40:41 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:16:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:17:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e2b2cb832ad58353bcc4edbdd16023beb64ec7856b469d202975f8de836c6906`  
		Last Modified: Wed, 22 Jul 2020 00:47:20 GMT  
		Size: 49.2 MB (49168473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d6493ea016bd1aa68fa88d01d53cd305f67bae5fa500592c76c466808bf221`  
		Last Modified: Wed, 22 Jul 2020 01:35:25 GMT  
		Size: 7.7 MB (7681419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33779eed82f6ae65801a87fd1278e902bbab0f609f0c6a0232d8ef0b37112127`  
		Last Modified: Wed, 22 Jul 2020 01:35:25 GMT  
		Size: 10.0 MB (9983891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c60edc216a99f1c184e4a1531064ec83ee610600e5e74bee81f9379d3ad0cbf5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69476764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8a0a8e8703313c2b0f2f7c22b09c1e53a50d66778da6a6ddab8f019c808dc0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:08:55 GMT
ADD file:2f4b8d9ab41b6e158f5926883b6bffdab1757086d903f3f0244f75bafc2e4876 in / 
# Wed, 22 Jul 2020 02:08:56 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:20:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:20:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:88151d2519867746e4945a0a06b45430b9ddc2ae4be7e7f927cc00e3f640290d`  
		Last Modified: Wed, 22 Jul 2020 02:15:24 GMT  
		Size: 51.2 MB (51157197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63faf17c1329ba4be1004b79b9d5981fdb34d19dafc018cddec9e666c9c34b01`  
		Last Modified: Wed, 22 Jul 2020 03:40:04 GMT  
		Size: 8.0 MB (7981104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01afb186eafcffc2d1ca254ef5ee318f8bcb96ad9f552c6d73ecb3d5330e09fb`  
		Last Modified: Wed, 22 Jul 2020 03:40:04 GMT  
		Size: 10.3 MB (10338463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e29e7acfa542ca00a94e08eeda393f38e19af790b0a93f8d17a454611c2a6a87
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66267071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adced5c2269780cbf4f7905ad8e3d9daaa2265f54ada1631375228efc1c6e93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:09:44 GMT
ADD file:b51eae556569a7654c89a15b745fafdb0477ed08e8a06f7fcd6363145123d67f in / 
# Tue, 09 Jun 2020 01:09:45 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:51:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:51:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8084fc3b4d2453eb8005c0b33e3c542e3615868e22652e74e19fec36df3c488e`  
		Last Modified: Tue, 09 Jun 2020 01:17:30 GMT  
		Size: 49.0 MB (49019818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df088964944d43608e89126d7ae55a47489499bad77148bac16c1593e8ff69a`  
		Last Modified: Tue, 09 Jun 2020 02:10:24 GMT  
		Size: 7.2 MB (7231469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a34d1c06dc4557c94a0e8dc1d4f49ee8f512c443dea9748d2bb00fc4e1f6502`  
		Last Modified: Tue, 09 Jun 2020 02:10:24 GMT  
		Size: 10.0 MB (10015784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b4b40edd0d76357826138e48faf1e115042d820b1aa7640b33599b4df8da9031
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73125386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0140641ee79abcdb4d6f4bdcad7d23e5c8ee144795b4c3843e031c60b9089ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:22:01 GMT
ADD file:18a41180457a190a9dede1228479d2e332a348f22ac027c36e14d6d92e556f22 in / 
# Tue, 09 Jun 2020 01:22:06 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:57:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:58:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0cad52b1770a1b4a84068be3efe78098837be582f5905e627b2cdba07e641fd1`  
		Last Modified: Tue, 09 Jun 2020 01:30:12 GMT  
		Size: 54.1 MB (54143376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0318f8e4196d9f742fcca63ed04f9c2cb14ac6541f33cd67dae342ef35845da`  
		Last Modified: Tue, 09 Jun 2020 03:43:38 GMT  
		Size: 8.3 MB (8254819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec302fe954105553bdc7cac9100b6bfd114d3b56ef94d850b0364da83650fc6`  
		Last Modified: Tue, 09 Jun 2020 03:43:37 GMT  
		Size: 10.7 MB (10727191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d7b281dabfa84642d35cdc06238c041d2c7635d4c7f0da022ecf3b3a40d6a4bc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66233673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7970f06f0dc60ce670ff86815089051474b65aa62ea405eb20722a0c47e4b6a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:42:24 GMT
ADD file:e5fcdcbbd996899922beac57e202b7e0895321e07263147e96c6e3b7b811d8a2 in / 
# Wed, 22 Jul 2020 00:42:26 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:06:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:06:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7ecdd8436fd4d951f4ca002a2aa8b01d427a7c4b535083e3ef0792444053154d`  
		Last Modified: Wed, 22 Jul 2020 00:45:30 GMT  
		Size: 49.0 MB (48966422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e8e5cabcd07c3b92963e637fc22608613c8a9013bf41d621452d8827c71214`  
		Last Modified: Wed, 22 Jul 2020 01:12:20 GMT  
		Size: 7.4 MB (7385174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a68e3c7fb279126bd2a86ecae67a5c1bd01806670cb45ad4367f30176fcdb7`  
		Last Modified: Wed, 22 Jul 2020 01:12:20 GMT  
		Size: 9.9 MB (9882077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
