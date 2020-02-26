## `debian:stable-backports`

```console
$ docker pull debian@sha256:313aa1b96e042fba73425a5358b3e2586f58206bf4bdb86a8b23f97d9fbecefd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:d1b7170190026eda5a5fd062bf19573488e653daf54e62e787612827719c8db5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50382242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430b9ea1d8efc21dec9889f34b82ad4c0d086626d955a5670fe1ee116c828320`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:40:38 GMT
ADD file:7d3b1ec0cb6ffcdbb880b300eb716cafbd8a9a44c558f3b9f1ab9b4a1655dae8 in / 
# Wed, 26 Feb 2020 00:40:39 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:40:43 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:252ea3946b692b0b70ab430ddee87f6ebf44edb4f1adac8c56dfbf81daa7c55b`  
		Last Modified: Wed, 26 Feb 2020 00:46:35 GMT  
		Size: 50.4 MB (50382018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231a9485f104f4411cd78b8c0ed1865264e9c677a719b08c056c592ad6848409`  
		Last Modified: Wed, 26 Feb 2020 00:46:40 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:198cf564a89280ff178c754db0d34bc7131de9bedb54587ddc2b9b5e4252f3bc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48093148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a7a2fd8753801538c6186b6da537a4fb5cbfcbff2fb2c6874df35cf4d09c60`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:04 GMT
ADD file:af3acc7fcf4055fd890f3f8f9885c23ff868d7c7a4e19da0ef6449ba5a7d245a in / 
# Sat, 01 Feb 2020 16:53:06 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 16:53:13 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2ee893b61f2f93bc84fd6d580e90b0610df96a724bb3cbb434f14536f57f1190`  
		Last Modified: Sat, 01 Feb 2020 16:59:54 GMT  
		Size: 48.1 MB (48092924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148cbcdba5fd674aaa2813784114c7f65815efee33b6666342c006e6ab6a1d4`  
		Last Modified: Sat, 01 Feb 2020 16:59:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e0ad9bbd0ca2d2e86409c4e277b84678ad56c44f45bb2bc2ec3c9c1649553b55
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45859922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3e69f469bfa9d984e21d302e5d8021553c3c53e325c72f06bf9148ff53a3ce`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:03:27 GMT
ADD file:a3edfad9f83c7a182b73290d40e6f5f6ee94a8a3e8b81971719a67208d1bce33 in / 
# Sat, 01 Feb 2020 17:03:29 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:03:35 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:57662fc8a1279cd8d42f3acdc7719cf7c7604a2e2397a4d75127230a2993ba42`  
		Last Modified: Sat, 01 Feb 2020 17:10:20 GMT  
		Size: 45.9 MB (45859696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7ecf0420add3af4c9ddc92d4317387820273ba36b6370be1b54de1a1762cfb`  
		Last Modified: Sat, 01 Feb 2020 17:10:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7d23975adbbbac1b165bb9573dd153c65dbd8e3979c8243b5ed974002d17432d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49171936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab979d8954cb51dbb53756797fc842959c9e02a0599af1c94afcb70961f34bf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:42:26 GMT
ADD file:db14bd80b506e5e1754a5e84f5db0a7e53b9fb85d8b6918b381de8f213538b2e in / 
# Sat, 01 Feb 2020 16:42:28 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 16:42:36 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fab170ceaa7d371d5a29b424744b1b61c4e7b546843bba74ded687d59ef8cfbf`  
		Last Modified: Sat, 01 Feb 2020 16:47:47 GMT  
		Size: 49.2 MB (49171714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f195d81e85bad9a889e854708c0689c8ec939736af187835c976f0417d89bdc`  
		Last Modified: Sat, 01 Feb 2020 16:47:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:f2079b6c78f4599acc28280a88365d2b1275b1bcd5402f722e627667d93d0ada
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51146334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8debeffd3945cc7ed9ab4b923613569378e58e050868338271fe093389553c74`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:34:47 GMT
ADD file:e583a8d1a9bc51a5460811e19c7e5f1a7c7d0f7675fc3f0a736cd099c8770367 in / 
# Wed, 26 Feb 2020 00:34:48 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:34:54 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:21db9efe6497a43a542416166e47e6fe6d0599e0cc7c15b611b9ff041b8bdd54`  
		Last Modified: Wed, 26 Feb 2020 00:41:08 GMT  
		Size: 51.1 MB (51146113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc596a1424fe6fe69ee743be5ab66bbac9cfb98e9d8360afbe77a86d73a78e30`  
		Last Modified: Wed, 26 Feb 2020 00:41:12 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:3da086c872892b043c6ea0a88d50c735fe704323f6bce2d4cf27869b5f68c1b9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54133018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2493b237270ac141d15aec89f28e6b3741884604a2d875debe6f88206f8dec5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:19:35 GMT
ADD file:48cf5f8fcdcc66f1e7fcbca9dff8e2f9c0c423abffe93c54d5c3364c7dceb666 in / 
# Sat, 01 Feb 2020 17:19:40 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:19:48 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7672ed36d18a19abdfb622589d848bf5e86f152ec96a8c45cfee133912d67987`  
		Last Modified: Sat, 01 Feb 2020 17:29:36 GMT  
		Size: 54.1 MB (54132792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd54aeb19cff53b4008b2d33ba9d9493c66f39218b19253c51a2e6da0bda8a1e`  
		Last Modified: Sat, 01 Feb 2020 17:29:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:5d7baaea8a20f29060d53b07ed9b6ae705663cced75f61ef398d2954c9e8fa3d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48958316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e165bb7a84ecd52d5b4693ca73c238762cd3a67ae54f150595d41f6510e18626`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:43:57 GMT
ADD file:be5cdbc6b5ce85fa7b01883858f4de3f57f49168921c7b4adfd553253075a6f5 in / 
# Wed, 26 Feb 2020 00:44:00 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:44:06 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:59726d02408e7d0cb82e910945264a18f5640d36ea5e213e36e39d33452ea586`  
		Last Modified: Wed, 26 Feb 2020 00:48:43 GMT  
		Size: 49.0 MB (48958093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb5c2be6211404dd3d7be9656b1ecf1142e4547d990274eeb2cae0695b6a742`  
		Last Modified: Wed, 26 Feb 2020 00:48:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
