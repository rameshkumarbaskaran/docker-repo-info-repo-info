## `debian:experimental`

```console
$ docker pull debian@sha256:ff4780cd545a4d8ab9136ee973f4761e1a275dd3f96e5ef96442dd01e5662338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:8bbeef6e32768cbc1213989edd62860a511278b8426fa6b9cba354bb569ca9e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53219164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c131b48619fccd62fa3488b2d0723ef5c154f0c7f8cc1f31db062ce48f75a10`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:49 GMT
ADD file:45d826596769429bdd8e44a7e4190e8251862fb92b291469c25a7f3adda1e39c in / 
# Thu, 23 Jun 2022 00:22:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:23:01 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:79d3127460f36c355c974cecc0ffaa2ec77e9b0ce6167c147a569dc304caf3ef`  
		Last Modified: Thu, 23 Jun 2022 00:30:59 GMT  
		Size: 53.2 MB (53218943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3252eb9414033e608e9dd7d4ee6106197abb35696108c27c1e4ac29a903c7022`  
		Last Modified: Thu, 23 Jun 2022 00:31:22 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:ae3904279e4a7137d63cc4673280b9a8345a1a0325d00278e0da12845b571deb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50998620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2860fe94635e21ba4b2216c8bdc164849c9369f34637b472eacdd2abae35817`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:57:34 GMT
ADD file:4bf21aa467ceb4d839160af4de449dad29d044a520791e6c71c54dde704d8bc3 in / 
# Thu, 23 Jun 2022 00:57:36 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:58:09 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b3478ed536c9e1abe83e1e0f866445e3e0fe7c2007c7aa36ad9cb504bf924a0f`  
		Last Modified: Thu, 23 Jun 2022 01:15:39 GMT  
		Size: 51.0 MB (50998397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6830b78a40c2a50a2a77f63f25a19a48b4a0ca0217fe3ab00744d28aa8ddbd1c`  
		Last Modified: Thu, 23 Jun 2022 01:16:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:8ca80eff05c673129d56331c9e8a86318c9efeac13d97b450c17967173259a38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48734896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc8a7c0b766d912e2e593420659a775813ada9f149609581876854e528071ba`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:07:08 GMT
ADD file:b53c1e9cf9af8f5ea1a55131d9e3ba9bcd734826aa2ee6b592d3f52eb83d35ad in / 
# Thu, 23 Jun 2022 01:07:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:07:43 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:98cc035ea75b77a3f8e8c19ebda6ee6eeb73c981a69a70564698d364354603fb`  
		Last Modified: Thu, 23 Jun 2022 01:24:40 GMT  
		Size: 48.7 MB (48734673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e77a79a82e62c457d0f2eba4333228511662bec66812d8db8cf0fd60ae50405`  
		Last Modified: Thu, 23 Jun 2022 01:25:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:81fd676af9929faaa800503d087b1a9eaae82ff048820ac853b761784af68e2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52331983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9135fc74e637077431fced62e66ababec5d338aea2167502a0a75fbccb8278`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:42:50 GMT
ADD file:1a940d88f62561651e40db55ea36a74594ec8b86da92a88afc099114961760be in / 
# Tue, 12 Jul 2022 00:42:51 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:43:07 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:53c4770665de01f88f5dc350b92ef44a1033377fe101fa00ca5bf012a1aad442`  
		Last Modified: Tue, 12 Jul 2022 00:50:12 GMT  
		Size: 52.3 MB (52331762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d292dd7ad4a0a24bf800c9a8a48c347ba4724f7cf05c95a2f579cfed96746a`  
		Last Modified: Tue, 12 Jul 2022 00:50:38 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:ee517901fa6a6fd581bdf1eff3fcea9ddef0d8602a6cc51aec353b88c8e1a583
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54207825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7b43623170770dcd956beeaa5555eef78b3b8d26afd39a07932db25c5b8573`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:41:45 GMT
ADD file:878426d87119dba8a22324e8c538357940c203ba90bc15912d0485b2267af353 in / 
# Tue, 12 Jul 2022 00:41:46 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:42:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:16053bd732f64321af8db68e64a8f71bd4687a00c0722bf8cd08a64a6576464a`  
		Last Modified: Tue, 12 Jul 2022 00:49:18 GMT  
		Size: 54.2 MB (54207605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7166d9c296c16421eaa66e6d6a8dca6975a387c20cda22e63ceb329ac35bf3`  
		Last Modified: Tue, 12 Jul 2022 00:49:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:1c3150839e599b594f5bc883aa5943bf830cde5896bafe8afafe97e98926a694
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52302739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61065a9b26086862c02636f4e14b2d10dda67dc5f4d40b7b6283c28da56ff22a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:16:08 GMT
ADD file:5c6778fb86e7d357d580b290f5c2412a60a10e9471bdd35f7f1bcea89f778b5d in / 
# Thu, 23 Jun 2022 01:16:13 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:16:47 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e35d557c5f59c786e1cee99b27bbcfb82971b64fb68396d2dff965edda36ca78`  
		Last Modified: Thu, 23 Jun 2022 01:27:26 GMT  
		Size: 52.3 MB (52302516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9362f47d703d4c89c6093d310c18365b549176060a114e38ea63aae258377a`  
		Last Modified: Thu, 23 Jun 2022 01:28:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:9d451e4790625db6cec4a301fd50b71ff9348d460848bc203efcb62e9bf24385
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57413945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a952df83f91a4666a372eb42c8f2755bcbd84cf8afb054335c9591390f310036`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:07:25 GMT
ADD file:fdd6cbb2933f9789ed5aa49c79fdf3bf0cedd65ebbcabf222f0b23273fac9f99 in / 
# Thu, 23 Jun 2022 02:07:37 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:08:25 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:128adcf475823e4b10e1fa7d93e28914b85e7ac8fab1bd76dc0461df8139dcf4`  
		Last Modified: Thu, 23 Jun 2022 02:27:26 GMT  
		Size: 57.4 MB (57413721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c319a42087ca6fc41be55cc63e091f028dfb1108a6ba1ed0920b0ff800ad21b2`  
		Last Modified: Thu, 23 Jun 2022 02:28:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:6aa62f841e34fece8fb80ff14b20ceeeda6909f478545c6702b0c365c8af5ffb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49430058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b828398d2959653986804d33abf2f436f2533a9c09ad1bd064b8958b13e54d4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:15:44 GMT
ADD file:a681feaccc3b9ba4d66c01479fa4508aa35ce651550197a7c3df923cec737ae8 in / 
# Thu, 23 Jun 2022 01:15:47 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:19:22 GMT
RUN echo 'deb http://deb.debian.org/debian-ports experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:cb743002126f41957a0e66460d7f8a43b87be31bebe91733276c7a32c52f23f7`  
		Last Modified: Thu, 23 Jun 2022 01:34:07 GMT  
		Size: 49.4 MB (49429829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5345e0236dfa7acd1cafbf5340e4892e9c246059899ed26834c36bc14de7f5c4`  
		Last Modified: Thu, 23 Jun 2022 01:37:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:d1cc6bd803a00acadccec4f8ca720ee3f5be342c512a269f0db1a77c62cd0967
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51757607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1950c450da9d06262726b33ed9a00d21dfdddb046eeeb19a7fac82807a8d00b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:48:58 GMT
ADD file:ad15fe4787e44ec9dfda2d969c0adbbe98fa7cf5febddfd596b0e114a84ad120 in / 
# Tue, 12 Jul 2022 00:49:05 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:49:35 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:954d58d5c4ede279df1f24864d0cdbbb65d80c4803bf85a6c6ff55312899fbe7`  
		Last Modified: Tue, 12 Jul 2022 00:56:41 GMT  
		Size: 51.8 MB (51757385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808ceeca4a72efea3ac7ed35751f97654344af3f4058c9fafed2175952391f64`  
		Last Modified: Tue, 12 Jul 2022 00:57:00 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
