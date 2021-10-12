## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:654d363d647706e4b6458ec598e100b76db11a1718516d7d4c84a8c2a48c04a2
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
$ docker pull debian@sha256:150669b7d1b16b2ea6493ccab8a7cc9c38b9cd20fcfc61aa17d44cf7759713da
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.4 MB (55446265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1c3b8bb822441693d0ed182c36653582fc283cd297cb50af20a89a3ac67c7a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:05 GMT
ADD file:27dfce899c847022174d5caa95af127a948c63fcd5a23b6cbecc8167f4b2de21 in / 
# Tue, 12 Oct 2021 01:20:06 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:20:11 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:618a27eae568875e1902bc8979ae01edf1e0116fea44ca04d1d7c67d590cd708`  
		Last Modified: Tue, 12 Oct 2021 01:24:59 GMT  
		Size: 55.4 MB (55446041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104421c32b430b080cb319ebabcbaab6718a76638df220148a893aaaad3081d7`  
		Last Modified: Tue, 12 Oct 2021 01:25:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:9f6b720212d900beb03731e95d8be8dc3b7d247b060264a08683953118424f8e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52965168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af17d65cf2289dd37cb151341f138b4b1242b164e3b51895efe58fb4bfd0fddd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:48:55 GMT
ADD file:ab43782dfcd6f5ad4a656cf43f0385f45ef4a3c26e23153f4898190cf9b704c5 in / 
# Tue, 12 Oct 2021 00:48:56 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:49:09 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:13544a9b0148e44e1e5fa2a9d5e9cd0ecec08898da21d7ebf79b6a6b34d6b67a`  
		Last Modified: Tue, 12 Oct 2021 01:03:53 GMT  
		Size: 53.0 MB (52964940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e813a4832474dca02caadcb80883e590f995e930f1e4ca14ba99912abf6eb8`  
		Last Modified: Tue, 12 Oct 2021 01:04:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c939e45a893dc72f8dfa304ee2259ad9e5c0fc13276f2cc34d1d57412d8ebe5b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50566464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43f75ca1d2bb035b5d05458331ab44d0317e5066725f5bf57ca523cc8d8a272`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:26:56 GMT
ADD file:3b73f2accf5cf51a65b062fd02e1840ba8413191e44707e035ba6819a8eba1be in / 
# Tue, 12 Oct 2021 01:26:57 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:27:10 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:96084cd63f96d5395a465b5034a4392747af562af1269011d400540dc5b85a5d`  
		Last Modified: Tue, 12 Oct 2021 01:42:27 GMT  
		Size: 50.6 MB (50566236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4bb284d73302ba99570d9ec052fa58a187e4cd12c60bf0a47652931722f064`  
		Last Modified: Tue, 12 Oct 2021 01:42:39 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b0d643ffaa524d7b29fd3279d47c0deba661fe57499d97a2420abc6e055c0352
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54465395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720d134fac657c54c534ae83be567c3b4c640fe738ef99ef3cb270313a67f79d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:40:41 GMT
ADD file:4f13e43ce08281cef17adbdc736c615c592b9a55db9dcea6106e9355805d8eb3 in / 
# Tue, 12 Oct 2021 01:40:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:40:47 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2cbe7f3c2d37f6e753ada76cd01b0ecb8c8dc3a63791174a7bc8f7b2c95aa4eb`  
		Last Modified: Tue, 12 Oct 2021 01:46:59 GMT  
		Size: 54.5 MB (54465168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452ccd75a659ea27051705ee942662b01be42dd3e7df0a92d9dfcc08f1e14b8f`  
		Last Modified: Tue, 12 Oct 2021 01:47:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:4aa38ab2f152cf70dc581ae6cc6e8977614c8cbe59e4c078ed495e2614a70adc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56481022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b112c3a46ed04798db57ddcbe8d16a20e9b19578efe3a2525f27ad1b245d6f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:39:00 GMT
ADD file:5c67fb048ea543a4bda0c18d5b1f13f9ed438f0c2da79f7710603bb8072f06e5 in / 
# Tue, 12 Oct 2021 01:39:01 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:39:07 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5b6ea382495037522d99f596d06e6a07243f5c9a81406a71b1867d7b81c2d245`  
		Last Modified: Tue, 12 Oct 2021 01:46:18 GMT  
		Size: 56.5 MB (56480795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110b92c7383bdb6a8b5ebc6ddd880198e43bab191591320c17634b4ed06faa72`  
		Last Modified: Tue, 12 Oct 2021 01:46:29 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:4b701ae0899b5d93661e05b3db308e6d2c0af9329f6f4ad6b876d7f6ca143b7e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54069282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b8df1494b6d86f40ac2ac8a29db6c1201232510920fb70d39f851564c48cd5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:09:56 GMT
ADD file:8f2e72c6d8bc47bf31947b2f916b90c94c62fd9a3fd11deef021971c079ff665 in / 
# Tue, 12 Oct 2021 01:09:57 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:10:03 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fad81077a6466f0231de8750a5f41773b60638f37eeb5ec052d93dd340d095de`  
		Last Modified: Tue, 12 Oct 2021 01:17:59 GMT  
		Size: 54.1 MB (54069055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed867af3f7ee18bdef2fc2b049767bbb6bba4d8d53f61d12f9a244180c75f7ad`  
		Last Modified: Tue, 12 Oct 2021 01:18:08 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:cf22c84ccd8efdf50dd221507871231768c0cd98ff25dde3773f04eb348d0c73
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59660206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718d2bbff060756f389eb0d469c78b30020375ed53c86d58f76e172f7e9338d1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:24:06 GMT
ADD file:2208d7bf60cb752ee46dc1a2c107f0ffefb15b83324ef516b1b93f03c5d0c249 in / 
# Tue, 12 Oct 2021 01:24:11 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:24:32 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3cb87628128232319961676d93044c80b66d2fba881080d5a34c710d8a09207d`  
		Last Modified: Tue, 12 Oct 2021 01:34:29 GMT  
		Size: 59.7 MB (59659978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8906c83d1be1e812c758a74046b16deb6646ed34f62abdf4756b9cb0017f04`  
		Last Modified: Tue, 12 Oct 2021 01:34:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:e830b6567bc5813d206b5f906754ae35ce8f8bcc757c16d56f81542a45b93f10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53700366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781cfc78360a9ae84f859c1c5c41584ad312d1a679601923bdd45740c3327c89`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:41:38 GMT
ADD file:c1434e9b848c2f01f3fbd798a3e6ea6f1806b144dbc3f1b0d5bb8e1f51339b7d in / 
# Tue, 12 Oct 2021 00:41:44 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:41:50 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:68fb91bf36b385ffeb27bd029bade1171ff1a60e865f85a09ee539cbdb35b1e7`  
		Last Modified: Tue, 12 Oct 2021 00:47:15 GMT  
		Size: 53.7 MB (53700141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecd56624e3942a458f6c84f3b49627bb4b95fe8d8421e4e0d83e3b1db44b5d4`  
		Last Modified: Tue, 12 Oct 2021 00:47:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
