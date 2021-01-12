## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:ab1b6ebf681667d7e249bf3d8a24ddbd150d6a094408068974586d2056c0467b
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

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0fbe6079a41a1a669ca1b9c081932ae2f9bd5e77f9069f682a24de8867d326ae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128116881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fce4d1158c2ea89a5cd6aec41fcfd440895acb0dce75f4a9e193f4460dbe96f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:07:48 GMT
ADD file:51a85ad79ebd7e288cd0ea14cd2ae41990aab2d77352f801f09c3a4682cb83a9 in / 
# Fri, 11 Dec 2020 02:07:48 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 16:59:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 16:59:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 17:00:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ff8cddfd21234a3c42ee0af471b251a807aa29af4ca00392976a17d3257ed269`  
		Last Modified: Fri, 11 Dec 2020 02:14:23 GMT  
		Size: 53.4 MB (53352668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58120f59d80232cb93b7fff568312888d13cf4167158305ffe8adc4483af30e5`  
		Last Modified: Thu, 17 Dec 2020 17:27:16 GMT  
		Size: 7.9 MB (7909957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37776afef7b17d4680060a625bb43a68146d6e6d5ab006be07856897c2aed6dd`  
		Last Modified: Thu, 17 Dec 2020 17:27:16 GMT  
		Size: 10.6 MB (10648135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43542ad23e1682377f889e0fd8dd5dd662b4d9f1b8e85bf63145a64dcaed34a1`  
		Last Modified: Thu, 17 Dec 2020 17:27:37 GMT  
		Size: 56.2 MB (56206121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:430caf2bc72bb332687644e1d929f31698720e7f9ea76d78dfad0eebda43d113
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121520389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a41e1f9e5a9a765b6d68e67e15de0fae162398a833b6acb58c7bd00655f56c63`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:53:57 GMT
ADD file:7c196731dd997fe0c289ed02eba35ecfe200559ab33bcd6e863f39d8dd0ea362 in / 
# Tue, 12 Jan 2021 00:53:59 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:32:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:33:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 01:33:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8703e0802b99292f132d58e67ad879ab0ffa44370ae81a8ca7a93ee05c332d4d`  
		Last Modified: Tue, 12 Jan 2021 01:03:20 GMT  
		Size: 54.4 MB (54362040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2920a5dce5819aaefba9b42acf5eecc9bf6a9cece8f1115be0561cd7604d55`  
		Last Modified: Tue, 12 Jan 2021 01:45:30 GMT  
		Size: 5.1 MB (5061367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ad854c9d78348debd410e2b83d72c46ebbefeabc275c2a9fa7877161420d56`  
		Last Modified: Tue, 12 Jan 2021 01:45:32 GMT  
		Size: 10.3 MB (10336421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea051d0fa4b3585dc14e2b6b16e7bd6bab45c2363fd73fdb6f52016e7976558`  
		Last Modified: Tue, 12 Jan 2021 01:45:58 GMT  
		Size: 51.8 MB (51760561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:269e462e07e2550a6d485e28c3c569fa5da043174aec85e41f870e5fa7425b2b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116573873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb24e45497c42ad3b506c7a19b92a44782654e74d073cdb09dca362b42fb1c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:03:45 GMT
ADD file:a459be4601ccf608a415f6ce53ea885edd1a9a10ba1205f3e8493e277e6a7faf in / 
# Tue, 12 Jan 2021 00:03:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:17:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:18:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 01:18:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2fdfe7e087b5c823888d02320fcca90d4debb7a7d0ead6a978abb2de6acbbc00`  
		Last Modified: Tue, 12 Jan 2021 00:13:47 GMT  
		Size: 51.9 MB (51902171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0592e7529a748d8d0e52ef640addc32dcea717609f5c656e4399e87bdd4d9db`  
		Last Modified: Tue, 12 Jan 2021 01:31:29 GMT  
		Size: 4.9 MB (4921500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeb968aa1e6a404fcd0a89cbc65878f592c4c4067725853712ca4d00c1669ce`  
		Last Modified: Tue, 12 Jan 2021 01:31:31 GMT  
		Size: 10.0 MB (9976214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdb7dfd157d86a4ab3edd03ec9cf4d063137a8f583451d79dea1963f4ac7213`  
		Last Modified: Tue, 12 Jan 2021 01:31:56 GMT  
		Size: 49.8 MB (49773988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:47f792147745c3a04e3075b90b8e336e8ed66aeb3ab30058cd22e9c917f3ea69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125496053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3f1ec20341d60a664a366e1dcfb03a7c2de631dcea6de70e2124f7fc531ced`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:42:27 GMT
ADD file:ba9ce45e2c6743713798982615c806de6db6d8fd9a0d8734c8a69d80f3959eb6 in / 
# Tue, 12 Jan 2021 00:42:35 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:27:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:27:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 01:28:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:01dba80e9024f3ac734ae74a14f2997ea67918b4de57aef778ed839a508baab1`  
		Last Modified: Tue, 12 Jan 2021 00:53:15 GMT  
		Size: 55.5 MB (55537816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8417d785c975de855b94a5c17e92b69107a02149bbd61ac1b6d1355d80b32549`  
		Last Modified: Tue, 12 Jan 2021 01:40:11 GMT  
		Size: 5.1 MB (5140360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34511ce04354db34bda0eb613bcb4990a4e262fe16307861b007423a0033c44`  
		Last Modified: Tue, 12 Jan 2021 01:40:13 GMT  
		Size: 10.7 MB (10655802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23256b8138d02e2f8552e7878b3d34195476c50b86ef0dcf9d758fb0bade2fc`  
		Last Modified: Tue, 12 Jan 2021 01:40:39 GMT  
		Size: 54.2 MB (54162075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4196455136664ad3ee180d8cb2166b2407d5514ffc67067eca8234c95c15b9ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131156653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f595e8161b5c912d2c9e4fb1b8e65cef2f077514057c4e656c2297d4fb2762ef`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:43 GMT
ADD file:ac372b15438c9387718286ebd1a5b9512e674cdc90319668b3612fcb0cd99441 in / 
# Fri, 11 Dec 2020 02:04:43 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:10:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:10:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 08:11:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbad886384348be399f916b804d2efe113827e77f3c2b05f9b19a4dd67bff32e`  
		Last Modified: Fri, 11 Dec 2020 02:11:56 GMT  
		Size: 54.4 MB (54407631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107edbf54231bab6e619380b341236d89d7c373021e0ca4ced89d4b094f74537`  
		Last Modified: Thu, 17 Dec 2020 08:27:04 GMT  
		Size: 8.1 MB (8083852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770453472dffc640059e49933b5042237ef0d2a63e4ecbc572da6109134c440b`  
		Last Modified: Thu, 17 Dec 2020 08:27:04 GMT  
		Size: 11.0 MB (11031266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6aff5ce2d179cce5128375be4a9798643c0eece646c52f9f561fc0a83103843`  
		Last Modified: Thu, 17 Dec 2020 08:27:29 GMT  
		Size: 57.6 MB (57633904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:58f7c36a6f3774dd3233336975741f3f58b69b7ef5dac5a10af488711ef95027
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123578418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5080581b208811c075eea5ce0f7991f7fb4b576f6463ef9a1ba8394961848244`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 01:16:48 GMT
ADD file:7bfb9d47fcd2b6a553e5be3b702d34f192cd8798dd3982fc6e6e77479f0affdc in / 
# Tue, 12 Jan 2021 01:16:49 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:54:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:54:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 01:55:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24a4375dbae3deddd016bd6d4372d219ba5fe4102ce643c06dd57677bc882654`  
		Last Modified: Tue, 12 Jan 2021 01:24:08 GMT  
		Size: 55.0 MB (55046139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1447ce8a926cf7692ae55e3f2edb9925e5b11be684c7fd68fe2a385a5b812880`  
		Last Modified: Tue, 12 Jan 2021 02:05:46 GMT  
		Size: 5.1 MB (5114938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfd08658a76a7d3cedb6b4760f760c0ce830104bb77dbffd92228d4d0448730`  
		Last Modified: Tue, 12 Jan 2021 02:05:49 GMT  
		Size: 10.7 MB (10658281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646e7a05de00a7a60c4b7f630af924f98065319eb7883ece0b8839a36675802f`  
		Last Modified: Tue, 12 Jan 2021 02:06:42 GMT  
		Size: 52.8 MB (52759060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:da7d02d54f25245b44530156a1c8dde78590aa4570d25cf76250229401eb11be
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136205465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3bf782687e1b88166a4992fdbdc58a14a653553a4459da68ab97f1a17e4e02`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:40 GMT
ADD file:f289d6dea557bc0563fd9221c4857a56c56bb52d981a3ec90ade2f1b76980794 in / 
# Tue, 12 Jan 2021 00:25:56 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 02:21:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 02:22:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 02:25:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:594e638823d3ce0bbedac4d1aebea00f91d28a98d7b98ca680fd90e4c0fc8850`  
		Last Modified: Tue, 12 Jan 2021 00:34:46 GMT  
		Size: 61.0 MB (61048727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a59148553af7496dfbc29a5704e94338ac15ab898a646dcbab32076a5f00f3`  
		Last Modified: Tue, 12 Jan 2021 02:40:41 GMT  
		Size: 5.4 MB (5400394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45a065f7b5587bec16714bce093a4075fb92b291238fee1bae7d383a16a4052`  
		Last Modified: Tue, 12 Jan 2021 02:40:42 GMT  
		Size: 11.4 MB (11422811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d08d3752bb8f3109a9dc34906d86a1d6f92b178e9b8153717c78ad56a98e568`  
		Last Modified: Tue, 12 Jan 2021 02:41:08 GMT  
		Size: 58.3 MB (58333533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c01da195431155fd365c4e3aac73a544f041de44a74be472f29ebdaf486d5908
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124227025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61edff26e6dbd2f2178de05710dbbfa9994520c866ac49ead75b32f1eb5e274`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:42:33 GMT
ADD file:168fa93b7a5e386f9127b8b0d3ef48b98f82ba06ff1d48ac529b03d704687af9 in / 
# Tue, 12 Jan 2021 00:42:37 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 02:12:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 02:12:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 02:12:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c7a519e99fa2bc8473c6755b8e9be0f1d685a3d42426bbd0d3e942b5d1f9a4e8`  
		Last Modified: Tue, 12 Jan 2021 00:54:49 GMT  
		Size: 55.0 MB (55038475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c303cc6ccc4ed36f7947903ef4cd9e4d9325b5495c5019ac8262fbe63bd0acf6`  
		Last Modified: Tue, 12 Jan 2021 02:25:30 GMT  
		Size: 5.1 MB (5135101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2547d9300a261d759832bce2972dd571e9149f705eea6a0b45574d2e535745e7`  
		Last Modified: Tue, 12 Jan 2021 02:25:31 GMT  
		Size: 10.5 MB (10527070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e93c3392d1f717040729d8a87724fcdb1756e410ea116e261c5169f4d501e1b`  
		Last Modified: Tue, 12 Jan 2021 02:26:52 GMT  
		Size: 53.5 MB (53526379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
