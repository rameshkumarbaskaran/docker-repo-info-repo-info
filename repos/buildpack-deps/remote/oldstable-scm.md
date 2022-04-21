## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:a092800cde076d400bc08e0771ced3ddb88efc154854dbebefc35da5c245a7ef
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

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:290ef4de398f9f61271ce22e4c961d1e3e1bd7ad977057f297838f6dac24ec2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120134388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8208ab8769975ac26b1b3a6ca1e25898d810c64748f30cb0af744bd43a50a8ba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 06:59:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 06:59:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 06:59:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdd409f4b2bf3771fac1cbc2df46d1cbb4b800b154cfc33e8e0cd23e67ab3e0`  
		Last Modified: Wed, 20 Apr 2022 07:06:56 GMT  
		Size: 7.9 MB (7856378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3069e6cecf9d5e43ace0a925b53849b2fd189ef41883d45d8f2e12213c2c06`  
		Last Modified: Wed, 20 Apr 2022 07:06:56 GMT  
		Size: 10.0 MB (9997231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee16f45eff97cbe98b74c63ca2375b2c6b2592cd765a86df098f731baab13ad`  
		Last Modified: Wed, 20 Apr 2022 07:07:14 GMT  
		Size: 51.8 MB (51843794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5ab243540a77918d52456c7522d8e197d471cb7ecece4e852d76537a111c3196
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114818997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c328fb7e6c1e86cdca435863df07303234f1aaebf88d0b2c73a74076d4a627fe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:17:11 GMT
ADD file:ad329516525d9a2e9eecb4bd6263809faafa65bbd9e6deebcda8196b0ea24234 in / 
# Wed, 20 Apr 2022 07:17:12 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:42:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:43:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 12:44:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d426a13b8d217ec7cc2eceea9d798d79a1c36c60cb9363d2ef2d86abcf895e88`  
		Last Modified: Wed, 20 Apr 2022 07:33:13 GMT  
		Size: 48.2 MB (48153607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e6f91f8d8f6effa3b0301678a3bffa5959462bbf96deb2b669b6388e93d47d`  
		Last Modified: Wed, 20 Apr 2022 13:04:28 GMT  
		Size: 7.4 MB (7400330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f92b3ddeebddc859cc64404c00806ebf416f52030af1bc22996ce6b6099f8e`  
		Last Modified: Wed, 20 Apr 2022 13:04:28 GMT  
		Size: 9.7 MB (9687491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33f3b87e965d4f4f6a012d5312fa273c2beffba18ccb2041fb9fe8fa446ee13`  
		Last Modified: Wed, 20 Apr 2022 13:05:16 GMT  
		Size: 49.6 MB (49577569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0c9c8ba01a56753f4d20b8881768f5254a2648d5d289886b43bb7c0d54bfd036
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109754314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851c96457a5c1e7ab6cc581f0665a7ac67f329458510568a090146edbc840a93`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 13:27:49 GMT
ADD file:fbbe7a4ec12b0fdfa82879ff73d49ba760c5b6cc47b4c8ecabe64f7e8f4e6340 in / 
# Wed, 20 Apr 2022 13:27:50 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 20:10:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 20:10:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 20:11:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca53ad6266ed4ba4323f1553d8b226d0a180384cd290a8361ab19347f6d761fa`  
		Last Modified: Wed, 20 Apr 2022 13:44:25 GMT  
		Size: 45.9 MB (45908143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88557019ac316ca250696b933e42aaa72ec3e8fbf729c5533426c4086c2fdbfa`  
		Last Modified: Wed, 20 Apr 2022 20:34:02 GMT  
		Size: 7.1 MB (7145008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a4c4d54010e8b79170bb4258d395325738492033d7f8f54b6e0e833848c969`  
		Last Modified: Wed, 20 Apr 2022 20:34:02 GMT  
		Size: 9.3 MB (9343718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982abaa2631ddfdda5b8470dc4b0b57ed3b1d10e77d38dca63de7a440db0a2dd`  
		Last Modified: Wed, 20 Apr 2022 20:34:46 GMT  
		Size: 47.4 MB (47357445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f756c7c483c0befee03cb3f2b3f86e4daf9650e4fadff671ac76f76342f69c1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118889344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c07dfcb1758a2e24aff32df23e68c292f2b05fb482d554f79033cfaa604cd71`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 06:45:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 06:45:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 06:45:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80651adb7e52d8ecd27d43b9e69ada9ca277071ea09607121d0076de36480b`  
		Last Modified: Wed, 20 Apr 2022 06:55:25 GMT  
		Size: 7.7 MB (7719745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b38ee622cbfb492ebc3bc598771624fba7ef1830b4e0f9737f2bbf4b6ec0ea`  
		Last Modified: Wed, 20 Apr 2022 06:55:26 GMT  
		Size: 9.8 MB (9767312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc937997baec7d2d040aba23614db074862008cbdd69b46d2baea31711d58a50`  
		Last Modified: Wed, 20 Apr 2022 06:55:45 GMT  
		Size: 52.2 MB (52174549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b3c4efb7f6d2adbceaf72d0521ea7bb83308785fb79fbbcd10640b31cd535f1e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122783384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7f3713deb33480ab5110021dedd309f8c500e32441ecc5b7631713af534796`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:37:47 GMT
ADD file:f66ba5e7b2801d19041661506f244a3bb89fc613e2e27891bdba3183bd6ee097 in / 
# Wed, 20 Apr 2022 07:37:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:18:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 10:18:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6e8f333ddc9f58dd9e74b1f250e3812ba3942ef13abee1d6b4e3d3131a7e29ff`  
		Last Modified: Wed, 20 Apr 2022 07:45:17 GMT  
		Size: 51.2 MB (51195868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4353b7b00b407b29561abe4d0fffed162775a58e3c48ee2edf64cbb21cfcb11`  
		Last Modified: Wed, 20 Apr 2022 10:28:45 GMT  
		Size: 8.0 MB (8022285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f90dfd06367deaf8c4c4f802c2dfb9a36dbfb3d208f4972a8c79b0892b07832`  
		Last Modified: Wed, 20 Apr 2022 10:28:45 GMT  
		Size: 10.1 MB (10122004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71948e43ad88935c94f9d58f3ef1c3f9aeca8f23d363ae038a1e4ad7d5ff8e52`  
		Last Modified: Wed, 20 Apr 2022 10:29:05 GMT  
		Size: 53.4 MB (53443227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f9880be0a15731e9afcffb63a029123909bd7ae588b5e6bf1ff1d48ffc1c2bce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117006234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9e1d718a4918aebe657f314e47f09bf9cd96e637fa068ab6df828fef26c57d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 14:29:07 GMT
ADD file:4d72d556af68726f3f6b8a1201825561024a6b9863d3458352941912fff3a1b7 in / 
# Wed, 20 Apr 2022 14:29:12 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 23:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 23:23:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 23:25:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cd1d11c7d9330cfc741196dea55cb8a7bfad252f4b3640a183c09af331282960`  
		Last Modified: Wed, 20 Apr 2022 14:40:00 GMT  
		Size: 49.1 MB (49070945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12df19ea003bf8c54f7dfd8f448b89e931fbfcb76ff9f57e0409ece92df3d553`  
		Last Modified: Wed, 20 Apr 2022 23:45:33 GMT  
		Size: 7.3 MB (7272722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524102a0e6a8e5aed6a2dbc76f92017662f4084331118b4dc7ff8b02504d50f1`  
		Last Modified: Wed, 20 Apr 2022 23:45:33 GMT  
		Size: 9.8 MB (9800274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee137529a582ee305a2f49c86fb749c88e670f3360f28331dd60ab25a13efde`  
		Last Modified: Wed, 20 Apr 2022 23:46:19 GMT  
		Size: 50.9 MB (50862293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e1189ab89868279d1ef27e0d088cf4b5edc798f911450c205079f1a81ee74cad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130648832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beda4c9a7ab47013c12b77006b6409cbc6844c632887b3d9109207c5bff1ed9c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 09:47:08 GMT
ADD file:0e047f9a02092945498103cc7b6483b67ad3a6d4945ac61230d539e4b6e14663 in / 
# Wed, 20 Apr 2022 09:47:15 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 16:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 16:58:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 16:59:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9d81baca7c32c0c0c5ac628e027c3c89760343d8a3469fbf7c764d60badfa23`  
		Last Modified: Wed, 20 Apr 2022 09:57:27 GMT  
		Size: 54.2 MB (54169874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471abb8491cb0e6fbc939a8b1288d0a3570dcb768b546f629492d9ed64c075bb`  
		Last Modified: Wed, 20 Apr 2022 17:30:00 GMT  
		Size: 8.3 MB (8293305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e79d615052af48cc503a49ad364e5af9254b18f8a25a544df7a576c0a678d7`  
		Last Modified: Wed, 20 Apr 2022 17:29:58 GMT  
		Size: 10.7 MB (10727739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7418e7bf65f0685bbf61fad49facffde7e586aa3b06d6e974572df0bc9bd1e50`  
		Last Modified: Wed, 20 Apr 2022 17:31:23 GMT  
		Size: 57.5 MB (57457914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:16b5c5735aff31fc9df0a4f8b2b924d7ae788738d13de7722e6aeabc20c0d84b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117690192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e3be098cffb3a143957c656f2d2813c3ee2f7b6f8059caf8b4f0221863df97`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 08:40:05 GMT
ADD file:fedc64967d4810188e8bd8289de1b1848a9501e7c68ae5bd4af83377fb9e3108 in / 
# Wed, 20 Apr 2022 08:40:12 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 11:17:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 11:17:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 11:18:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5c2799a5996f1eb24bb7f4c0219facf7e95c780314bb9e9b62594f1fe56cd511`  
		Last Modified: Wed, 20 Apr 2022 08:49:56 GMT  
		Size: 49.0 MB (48999225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346950f736889109f89f84157f4d1cc4e75599b0df1eaf097803680eb2fdb900`  
		Last Modified: Wed, 20 Apr 2022 11:29:06 GMT  
		Size: 7.4 MB (7423732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0a4abb2c4bda3be6e461f0d80740f3e2644a6dd833bcc0b97c83bd6a4e68ff`  
		Last Modified: Wed, 20 Apr 2022 11:29:06 GMT  
		Size: 9.9 MB (9883312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e0b9ea3498ff104383beba3cd632c64041234400c7a7d71acbcc7aa941e3a9`  
		Last Modified: Wed, 20 Apr 2022 11:29:21 GMT  
		Size: 51.4 MB (51383923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
