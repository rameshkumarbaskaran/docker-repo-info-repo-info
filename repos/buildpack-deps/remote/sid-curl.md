## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:5026ddb8d827d4d1d402a718e97895eb47881189a4d33919711a2ab71ad1e386
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:eba2f36b648ff2a8895f58fa445152c80dd28e16d7ba0c904970a1e62ed1deb0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71095442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456f607a08d80280ad597c44011acfad66a5e247d845eab4bbcfd1410b3ec333`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:42:22 GMT
ADD file:9463b73933c9a0f2df3bbfaa2805027794a0e3a0cca69453b066ebc4644b6f06 in / 
# Tue, 13 Oct 2020 01:42:22 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:22:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:23:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ead5025e4e59e53184c941889a91b90e4e7af750b6f2e005952c8484512851fe`  
		Last Modified: Tue, 13 Oct 2020 01:49:57 GMT  
		Size: 52.6 MB (52587404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50bcb11b150787afba1f3af7ebbb7af8259b2b8b14121b74a6d0b01551ad97c`  
		Last Modified: Tue, 13 Oct 2020 02:30:25 GMT  
		Size: 7.9 MB (7879844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455355c490cedd80caaa467646ef3389e55170d8520f80248b97232c03d34b5f`  
		Last Modified: Tue, 13 Oct 2020 02:30:25 GMT  
		Size: 10.6 MB (10628194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cb38ff79d5cb86d414e0e6dd74654d5e3c93d5d30480a23e631947924e577591
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68853143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c357d14a04f389a0bfc65d4aa66630e2cd7c060f75459112e1c3bca95350f323`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:25 GMT
ADD file:48fdddee7022ba5a0519e9f9dc9a63dd483e5294d0cfed9db93b066547405eec in / 
# Tue, 17 Nov 2020 20:23:27 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:54:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:54:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a5730ec2f66f57a119aa59f80f288eee4fa0a1adebe48e9a184400d277b84ee2`  
		Last Modified: Tue, 17 Nov 2020 20:33:13 GMT  
		Size: 53.5 MB (53546003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7216d292993333f9d256b5efb205324811bb27a35f161c01af5690ebc3c5dd10`  
		Last Modified: Tue, 17 Nov 2020 22:11:18 GMT  
		Size: 5.0 MB (4974955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97e0fda183c339defd615cf109c141a20426f4d5020d3d97bff391567c03d72`  
		Last Modified: Tue, 17 Nov 2020 22:11:18 GMT  
		Size: 10.3 MB (10332185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3f5b438dfde3a30914017aab51d2a25a616875279268c6a6db5a27f18b251eb0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65936251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe40ce14727139636269cc766467a2835193b5cf7afc28ed7d1c84b0860315e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:06 GMT
ADD file:7bc088cc808b76314a338212bb2b1cfa40e3747a587709f883b0b3d24272ed5d in / 
# Tue, 17 Nov 2020 20:24:08 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:52:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:52:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6540e01ce43e9b114890e344f5358356defa70d487f91c1a002e0a64db73d60d`  
		Last Modified: Tue, 17 Nov 2020 20:34:10 GMT  
		Size: 51.1 MB (51125953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba56633e4f20c85ff3a7a96ebf325e3b8eb38ce01b4a19d147fba95c41307d6`  
		Last Modified: Tue, 17 Nov 2020 22:10:06 GMT  
		Size: 4.8 MB (4838976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3f95259ef99cc96a3d8352c48117cd75a72bbd30aa5c3198adc601ee244ce8`  
		Last Modified: Tue, 17 Nov 2020 22:10:07 GMT  
		Size: 10.0 MB (9971322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:653649165e85305ba91ed15c627e09c9a931aa9ce739ed336f71c10063ff6b07
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70424241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5161dc23b84d6c5756111f2477170e7920d5e43c54dc93115ed3855ff3455d7f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:57 GMT
ADD file:dd38237d30f418925f9d05a463817130964bc613d39a38eeea7b87b9b5d62608 in / 
# Tue, 17 Nov 2020 20:25:15 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:24:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:24:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:28adf41b7f9d0f64232c0970a16416d0ef2eaa00df57f3caf5d257ccbd3b206c`  
		Last Modified: Tue, 17 Nov 2020 20:33:04 GMT  
		Size: 54.7 MB (54719929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516539a7ff1b41bcd60f56a25019366722df8db637f7a409ba85ab9918633b31`  
		Last Modified: Tue, 17 Nov 2020 22:38:10 GMT  
		Size: 5.1 MB (5055909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58beb0eca7357870a7d9572e6897310b7dbb65ea59a9f76afc5b75a63c11820`  
		Last Modified: Tue, 17 Nov 2020 22:38:10 GMT  
		Size: 10.6 MB (10648403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8c9f792df88c924d883281936dd7ae7e4a3b7328537eca3b8080bc4d044f1fd6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73308219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88329186fa891b9f9fa60ba923532e1c54ad8595d6bbf2a6986435c553ed2f82`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:59 GMT
ADD file:6d6afa8490ae5ac639c8369b0f5d9f8e49c675672ebd5348a955a3c9656453f5 in / 
# Tue, 17 Nov 2020 20:22:00 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:17:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:17:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:be81561500ea27b67d364b1567d73e6fbfac19e1739e5b1e5674dbea758abedd`  
		Last Modified: Tue, 17 Nov 2020 20:28:52 GMT  
		Size: 57.1 MB (57102236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc436cb880e1d23236f4f748fe380b16b0e16955049a2c0c1ab65456f67c2a49`  
		Last Modified: Tue, 17 Nov 2020 21:26:18 GMT  
		Size: 5.2 MB (5183137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca3e53afca84ddbe3333e0b6c779a68bb454199b167cfb74eda23f74fbea675`  
		Last Modified: Tue, 17 Nov 2020 21:26:19 GMT  
		Size: 11.0 MB (11022846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5688e8494fc51655b8feebfa9d116e9e705f2af7dc187edaca02c3a423aa4e14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69926438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63b00b2719dc1389e7bd767fee7ddc0bb9136b2f9e0953afd6406348f503463`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:54 GMT
ADD file:e6702c456d50f8685a251f68c8f1ef26036f57dc2b0b3ee32a713a0fff6192eb in / 
# Tue, 17 Nov 2020 20:19:55 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:44:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:44:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:15e7eab80614971302cc43d79249de4c2eaedd05f7ae229c90002e6998c37745`  
		Last Modified: Tue, 17 Nov 2020 20:27:23 GMT  
		Size: 54.2 MB (54247133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb52b20dfb96ec0abe6e94d1493602c96b8050c535a911f580f3723be5bd3b7`  
		Last Modified: Tue, 17 Nov 2020 22:55:28 GMT  
		Size: 5.0 MB (5026356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe047368d6844c3bab8d888c6322017279e7a1ab2f8537217ab3e70de38f39d4`  
		Last Modified: Tue, 17 Nov 2020 22:55:31 GMT  
		Size: 10.7 MB (10652949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4c78cba5a674d0117a0549c11318b3cb7baffd79ee69d9a8f747d5a6de2e8a73
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76217733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc7cfbf8882871f1e3f7c1728ee24886a7f593bfbed8a590fa23cd9bd41f0b5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:24 GMT
ADD file:7998a5d3f49a86501eb252e7dc54464d086e8239a5f918b15cd85dd11e7341bb in / 
# Tue, 13 Oct 2020 01:39:30 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 09:10:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 09:11:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ab405c79eb283d457b4f978511bbef215699b366c926b3450f2a7cbc6a56e33b`  
		Last Modified: Tue, 13 Oct 2020 01:51:11 GMT  
		Size: 56.5 MB (56495338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38962ab4f4d37e5644006dc2c9a5a9b270448a5ea5ea29a387f4c7955497875d`  
		Last Modified: Tue, 13 Oct 2020 09:38:29 GMT  
		Size: 8.3 MB (8329668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8ecae68ecea0d3add456e8b38f9eef46b95731e6dfca00f430a45a774f2a19`  
		Last Modified: Tue, 13 Oct 2020 09:38:30 GMT  
		Size: 11.4 MB (11392727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:12dd0226821fe2a3ff63116dd0a60c01d12b9bc10d70736470f6a39e2f1dbf3e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69777453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf07845427e81d6f0b253cbcf5514ca8551367e7412e5747a21cba8304efd257`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:18:51 GMT
ADD file:8962f20bb4a72e135379229e0846f699624835b74ec331608abaaebb561f33eb in / 
# Tue, 17 Nov 2020 20:19:00 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:36:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ea0b76bf69e10e271efafd881a3e6209b856a27b396fee1fe5c96626da5668da`  
		Last Modified: Tue, 17 Nov 2020 20:24:00 GMT  
		Size: 54.2 MB (54214424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d6fd966df630924882593f8be50b60b4dd8cbe08956bf3a1a09ab0c62129fa`  
		Last Modified: Tue, 17 Nov 2020 21:54:49 GMT  
		Size: 5.0 MB (5048615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5387e7afec1cae76ed6c62c9f9b187efd32793da95a21fba4cd0099aa37002c`  
		Last Modified: Tue, 17 Nov 2020 21:54:49 GMT  
		Size: 10.5 MB (10514414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
