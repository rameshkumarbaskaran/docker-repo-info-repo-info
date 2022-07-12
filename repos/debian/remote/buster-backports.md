## `debian:buster-backports`

```console
$ docker pull debian@sha256:fc345b8db584ab971f57e6fd3080d6828a969bc9405ff7606c1f91193ec0b79b
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

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:c89f493d8772714833867eb36d74652ba8d3617fd38481f57ace77b9f5fd344e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50441033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946087feaa0a78bef5f3f55cd4dd5b9d89daa90df0ddebe77794e72d94a46f8c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:36 GMT
ADD file:2f32dd3ef1e51a4d2d6dcf55fbf766434df5b3ada802b087d5761f2fa0cdebf5 in / 
# Thu, 23 Jun 2022 00:20:36 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:20:39 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ea267e4631a981caf2841a7e9a1faf29cef9d020c4378fc64845802d17586531`  
		Last Modified: Thu, 23 Jun 2022 00:25:38 GMT  
		Size: 50.4 MB (50440811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0435039edc7e863c9f6b6a37916258c78934c70be9239c22644d3764c63660cd`  
		Last Modified: Thu, 23 Jun 2022 00:25:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:a5a3eeaa27b79d550c461f1ca59916c1058264e7e4d7fd0c4bc2f7ff694e8223
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48160771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99218998b490311512cb6755a513b010b0485b906a5daf5586bb1c85be56efb1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:51:06 GMT
ADD file:46ca1be3e2e70869adc2c2213ad21ac3c743f1c7c0bbec927f855a82888f603d in / 
# Tue, 12 Jul 2022 00:51:07 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:51:22 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:83500cf45b6520b8ee0db35bb2065dcec25da5fca7b08fdb211039411146182b`  
		Last Modified: Tue, 12 Jul 2022 01:03:49 GMT  
		Size: 48.2 MB (48160548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb136ad53eb676ce8370b84063a98285efd5d04b98b5181658c43891fe29fe3`  
		Last Modified: Tue, 12 Jul 2022 01:04:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:7910ac7f1206289e01d81253fe0ac5c13f54e7fcef9882b3227f5dfc5c8f1df0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45915980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08b54e5846a9e776014e4e68b3a8da7eae36d3bd21d6ad489b96620501f513d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:14 GMT
ADD file:b8401862d74ac67a61f764c5dcc54fde231623bf55d2299665eab35dccd25114 in / 
# Thu, 23 Jun 2022 01:00:15 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:00:30 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0555d003e6ef528480fa5625ca8ff9a45d899a62b5c20ab7547a42c64d7c1d4c`  
		Last Modified: Thu, 23 Jun 2022 01:16:07 GMT  
		Size: 45.9 MB (45915761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f7d46d42068e02d5e3e56e3846f539cf16f459a74931b5684ee8c437ac48c9`  
		Last Modified: Thu, 23 Jun 2022 01:16:27 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:efd937b6e0fd0ea940d0b4305b451c43dfc555170198164dbaefe429d149bf6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49229150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a35233192d53b4afb010203817f90e5a4cac3d4f9ca40569ba189012e570fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:46 GMT
ADD file:ea39534c5e9a548d7938f6b0e2459383caaf3906f3cc5eafe8bf66053b19f2d5 in / 
# Tue, 12 Jul 2022 00:40:47 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:40:54 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:891a1587d3644a8b4b6dab3726ef380a725a0e19bfbf0eac02a275f711985862`  
		Last Modified: Tue, 12 Jul 2022 00:46:46 GMT  
		Size: 49.2 MB (49228928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc47a10a1d03eda4e475c443abe0c9cb99f685cd805df2c2d396b0fe5e54bf8b`  
		Last Modified: Tue, 12 Jul 2022 00:47:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:6d5366c9767c70fc600512bfbc18feff4aaa60f588367bdba8f4a6991a4fb2a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51204227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b801497f2df9ba800441cb4c132b67e4f4f562da35541c682a2d3295b397dd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:39:39 GMT
ADD file:0f1020fa1fb5b3518ec765b21180056cc802ac9258d1eed5e109edd83e0038d9 in / 
# Tue, 12 Jul 2022 00:39:40 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:39:46 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:87a13c20a9000f48185a3819712d2a14a8ddd6111bd1392856609aa18a233847`  
		Last Modified: Tue, 12 Jul 2022 00:45:40 GMT  
		Size: 51.2 MB (51204001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed15c2ef3516d9efd8e482aefef62edbaa3175ad43b8070118c991104af9db`  
		Last Modified: Tue, 12 Jul 2022 00:45:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; mips64le

```console
$ docker pull debian@sha256:7c78e608a7f31b67021f4e66c2f3c97512b78d8688e601fce6aa8b38cb1f9684
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49073394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251e251170bbdfc66076e489090ad34c270ff40fbfa3b55cdb1f98c9e8727416`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:10:55 GMT
ADD file:e97021cb9347cc6233316e4e1f31dc6728791c819d5c4f472c2e9009df33ed64 in / 
# Thu, 23 Jun 2022 01:10:58 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:11:10 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c69f93f35e40f60566a2c787b9d7a1e4ae3c026d480bd089de24eaaa432ffab6`  
		Last Modified: Thu, 23 Jun 2022 01:21:04 GMT  
		Size: 49.1 MB (49073169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28904093310a26e12b7e0a53e431cc04981af53700f3fbf12925550655a8fa3`  
		Last Modified: Thu, 23 Jun 2022 01:21:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:4d748d1b2b32bd71133be59b639d36c757cbfd63fbc07710144ab7817153bcde
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54177301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ff7cc1cd9e2b2c35dece441554b3f45799909af3bf370da7edd9c4903e2147`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:02:51 GMT
ADD file:651dca0ba404ba6a560fe25a63054deb11b1aec0fc51ebd145c915e1b97fd834 in / 
# Thu, 23 Jun 2022 02:02:58 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:03:13 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8fb2f047b2d097aaf3e5da7de371063fbf729a1c3fd6ab1cee82d13f03254370`  
		Last Modified: Thu, 23 Jun 2022 02:16:23 GMT  
		Size: 54.2 MB (54177078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636c1c46a73a28f15763a21a9cdce8193d44f3497606f55aea727f4016728f48`  
		Last Modified: Thu, 23 Jun 2022 02:16:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; s390x

```console
$ docker pull debian@sha256:174d80435f99f00c4052d70f7779522aee92513ff7182f685bbca28149691742
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49007192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ee0b115f30da865a422dbfbdc5e9e53126d0de4cc46f547148e9418f2f2813`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:44:12 GMT
ADD file:b8babeb1255f220a475b65f77c9d786d49eda80433cab5dc00c944dc05d31c77 in / 
# Tue, 12 Jul 2022 00:44:18 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:44:28 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:99ceea1856d0a41d4fd9ea8821ed7e159ce3cc53839fdbed273f1a57f5d9f5b1`  
		Last Modified: Tue, 12 Jul 2022 00:53:59 GMT  
		Size: 49.0 MB (49006967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b2ace99e1769abc259d904aa4e89ce34ff3b8f5140d99099ec30325ddc1472`  
		Last Modified: Tue, 12 Jul 2022 00:54:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
