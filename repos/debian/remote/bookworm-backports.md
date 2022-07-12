## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:9b02e131b67d29ba4a941689ff46dfb08252a306a0bb147afa5ee5e2f803dc3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:02730bed17106a177ea16ce7bba1224e3fd1be3bce085ff790133380683250e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52994206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e550058ac1a5f1b412dd543173df88a84365855436e38bc34e122d69ab82a686`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:19:54 GMT
ADD file:7e968e6ae38ede120a52f1d2e734b4fee4fd4ffd6e5f747edc8190d2a8bc6a52 in / 
# Thu, 23 Jun 2022 00:19:56 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:20:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8849e73adf621df4a443e9ac4eec9b698476e4f14f8ed894806f302d5b33156b`  
		Last Modified: Thu, 23 Jun 2022 00:24:12 GMT  
		Size: 53.0 MB (52993983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baec0e933ef4d12c74562b25bc861ca80dc538738f2a719dceaf4f2b6dfca53b`  
		Last Modified: Thu, 23 Jun 2022 00:24:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:c9151ed87fa4b8fad1c87afb74df704caeb8d683e49a78f7b96c5c212fdd38ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50821830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888c9cc1c6e2995d813ea4f8240e80f6ee8918df2e3e57cc9c2c6e3145e2c83d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:48:59 GMT
ADD file:211648cfc211d73b6facf8b4f6762e1b45f5894d43880d7bf0a7822be746ad58 in / 
# Tue, 12 Jul 2022 00:49:00 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:49:13 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e06063f979dbe8242191c248c95f1840e27b65404e59a60f54bfc1575fabed87`  
		Last Modified: Tue, 12 Jul 2022 01:00:53 GMT  
		Size: 50.8 MB (50821602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d77ddead4911380a572699aef15782c8bd39559968a16691e197f1f54e87de`  
		Last Modified: Tue, 12 Jul 2022 01:01:05 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ba7a016efa438945e34a02a865f1428d4753c86d466d3f4cda86f49eef86394b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48506742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d55f321d3ac76325f63487d897e21a0f2d88ccc5825e2456b76994f2afd4b3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:58:08 GMT
ADD file:485670bbc3d21c74d06e079229d1c74d05970c4bdf8c5d25692ab1464f0acfce in / 
# Thu, 23 Jun 2022 00:58:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:58:22 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:da5c76d2fa54760a1e859c83968ea6d7dfee1c43064fb6f34c27f8d639859b07`  
		Last Modified: Thu, 23 Jun 2022 01:13:19 GMT  
		Size: 48.5 MB (48506514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a870a33a2f42343a2de22de16d5edc8f176e731f29a2c0d55d03d845765fd715`  
		Last Modified: Thu, 23 Jun 2022 01:13:31 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d20bf190e069de17ba94652878264d20b5488368c3f4745a5d5dfa8bdd32dd4e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52128844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d886c1c6b227328ee4ed1f99f5044f115bd786f2733cf13e257a62d911f4469f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:39:53 GMT
ADD file:56a82a6c91d29741aef57453822e5502a13bd7841a1b3c8936a6f7b5c0b80bb6 in / 
# Tue, 12 Jul 2022 00:39:55 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:40:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:73d3feb17dc47282a9451cf8832ac9c5a707630877cc6c832d9f5cf4d3e2d202`  
		Last Modified: Tue, 12 Jul 2022 00:45:00 GMT  
		Size: 52.1 MB (52128620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195e89fe239a1fa72d9bf129ab23b24d5b86cd6eed652eb464b0d6a97e3d6e39`  
		Last Modified: Tue, 12 Jul 2022 00:45:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:5ea729742cc143d19640b3e84f71fa2e73d921785ea9beca400a124a8f12f908
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54004301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc4ce2ddc52c0e497d6cc8de33d7229fcd9c5f579ad5314c3418183024fece7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:38:44 GMT
ADD file:80ec0e35d6a4c162afe79f40617b47f846a2eb2065f245a230447609d1e7c001 in / 
# Tue, 12 Jul 2022 00:38:45 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:38:50 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ec7f9e3ed305349e742c012dcd142cce637ef3525759fea18f30c5987bf0e2fe`  
		Last Modified: Tue, 12 Jul 2022 00:44:03 GMT  
		Size: 54.0 MB (54004076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996b8e0595bd59781e3588a551c6fa269fc2b2d449fb3aea4d29665c8ef3a5b6`  
		Last Modified: Tue, 12 Jul 2022 00:44:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:43fe5fafd62afdf389dc9aaba776e09d063305ed3c8c4b418bc47e6bb54064c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52089521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323e642ed09c1ef6fb6ce1a7c16f894620efab8dfe4b07c01eeab41fcf9e6cc5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:08:42 GMT
ADD file:8bc6b496d7debb22306bce782f6b34ee75efae7151dc19314b45a9751b8fbdb4 in / 
# Thu, 23 Jun 2022 01:08:47 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:08:57 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:25ef8061366d5e6abd7ca324b8c1f08ba96be6bd0e55fd310e046a1e4becfdb6`  
		Last Modified: Thu, 23 Jun 2022 01:18:17 GMT  
		Size: 52.1 MB (52089294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447b26c2090a007856d0d4d58823ce2fec684bb71764199a27a3aa408a9b429b`  
		Last Modified: Thu, 23 Jun 2022 01:18:27 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:af0ade038dbd641498567ab029bb1a214f8d4f9ecced34f46206e4a6f7397821
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57198276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16091544097f823011ad380ac8ae5411cb31b86e1378c6a4755f0f592870c65c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:00:58 GMT
ADD file:d857864fffea40faaeec8c9492ef1805e6c891ebf06f1427f02398a3824debce in / 
# Thu, 23 Jun 2022 02:01:01 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:01:15 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8afb6214160c68cb540431e94c7bfe898f1a094dc45a834aa07634d34b1505a3`  
		Last Modified: Thu, 23 Jun 2022 02:12:13 GMT  
		Size: 57.2 MB (57198049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4cd1956cf1726db2e7d5800f179e011716973c50538c21d657cd0eee3691b6`  
		Last Modified: Thu, 23 Jun 2022 02:12:25 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:0a569e0d164fbb76a71a9b16fac68875e49be7eb325fff67f1938eddc91ac0f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51554396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850af3ff8e0c337594469d5d6440aae231e27be674b397e26b55c641e71e330c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:42:21 GMT
ADD file:affba659885c7b0f365e0fe6df963322452d3a11e8c5d1f1d1908cadb57c33eb in / 
# Tue, 12 Jul 2022 00:42:27 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:42:35 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4819cb6cd77746b912d22ae402922254d55d38be97967a6c3851624256c8a8cb`  
		Last Modified: Tue, 12 Jul 2022 00:52:08 GMT  
		Size: 51.6 MB (51554170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db8ae024c4a8ee964f675aebe7f0e2790a6c0c63ffa3f9f8a48bb8f5aff8285`  
		Last Modified: Tue, 12 Jul 2022 00:52:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
