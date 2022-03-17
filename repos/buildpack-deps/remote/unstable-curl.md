## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:41ae100660580ef6a2142f2b70db95392165d470b89b4ca273c743a1e2375cc3
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:63a7ebdf658dfbecd7c80ee33f278e0f7f519d43281268656af4e3491a9ab674
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72177271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5615ee80480683c8f83862d5d816428ebaa1a1f13ab1892a76007deb61e7e965`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:14:59 GMT
ADD file:62b7e1deca7e12cf507f0b06446a94bfbaff1760c4333fb3f8f92392b57d50b9 in / 
# Tue, 01 Mar 2022 02:15:00 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:29:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:29:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:740da9cc2bb63315fd21f4469ac9e44b2f6efbfd32f98a83c863fa9c1a145714`  
		Last Modified: Tue, 01 Mar 2022 02:21:38 GMT  
		Size: 56.0 MB (55974168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0280ba50ca2de993dcb64a6b9609cf934e39abda112acfcbab8f17a1f5874075`  
		Last Modified: Tue, 01 Mar 2022 06:38:49 GMT  
		Size: 5.3 MB (5275205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04148c21dcbdebe02df7619b1d768334fddc8ac9b581eea2f0dfea8e0a08664f`  
		Last Modified: Tue, 01 Mar 2022 06:38:50 GMT  
		Size: 10.9 MB (10927898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:397a5a8f428618622c2a2388f7e270ee7ce686205fa76a98edf5fd7f9c5d2ce2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69138468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280f136c31ef0c61121a82be00b1b9c2ec6f0af93350b25207a1104a365255e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:06:24 GMT
ADD file:ac39701f9a18e3289cda9df4afa1e6d52cc3d78e450fe0f6c8eeca44fcfbc1f8 in / 
# Tue, 01 Mar 2022 02:06:25 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 03:10:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 03:10:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:63235811a46a23f0266af9da0adeda5035210e9743bc381224f6094ba385018a`  
		Last Modified: Tue, 01 Mar 2022 02:23:10 GMT  
		Size: 53.4 MB (53368459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6001fc0f1458be1cd71edddcfc4c80e694e97390d00c3d9321a55c350435e3d`  
		Last Modified: Tue, 01 Mar 2022 03:30:47 GMT  
		Size: 5.2 MB (5175117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980544d5a86961e1d8ee36922ff866b49151ba29c6e9147204d209098f94070c`  
		Last Modified: Tue, 01 Mar 2022 03:30:49 GMT  
		Size: 10.6 MB (10594892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fcb99ce3e04494216fd202644de8f8dd1076a25b12318ab6fb5279aed228f74d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66272565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f709c5b39e66bf76fae317ee39d2b2e26fc951c7ab758c004c2015ed29e98f1b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:06:51 GMT
ADD file:6d4b498179cf5ce76b5c392522e45f7c4c4d0d4bfecee20cf2e30c39ab2c209f in / 
# Tue, 01 Mar 2022 02:06:52 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:33:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:34:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1c659af384e72219bee43c78d09cffa65613c854ea39a8d72326f2897f1c899d`  
		Last Modified: Tue, 01 Mar 2022 02:23:24 GMT  
		Size: 51.0 MB (50991190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00022efa6a0aec733e4d12aa18f38e4a2938f4f051f6e9e8c3e2046f1ff2f9c`  
		Last Modified: Tue, 01 Mar 2022 09:56:41 GMT  
		Size: 5.0 MB (5035167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81db15ace667b6657bcdacc04d0531c5cd45fd704d5e17e4addddfa52a907051`  
		Last Modified: Tue, 01 Mar 2022 09:56:42 GMT  
		Size: 10.2 MB (10246208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:44ec3b0afdcdd3dc9a797d8c4fcd66fd69676f11c908d9b00ecc8dec2ce3bd89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70832413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8455d09424006e7159ab71e11b8630bdb2e0e18a9282e9f7dd4f839b23a32f3f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:12:59 GMT
ADD file:709038b8298e06fdef9e537e714acadf4542cec6bd98db2854a8aaa95d67784e in / 
# Tue, 01 Mar 2022 02:13:00 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:36:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:37:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6895b0cfa9016bdd8a8e291fec2a7c649679eebea9c4d2fe2c1eec8c2f512d66`  
		Last Modified: Tue, 01 Mar 2022 02:20:55 GMT  
		Size: 54.9 MB (54879655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8621720688b7414775922fb5239ca1707bf52ccdd3850a148e568e195ec558bb`  
		Last Modified: Tue, 01 Mar 2022 10:46:47 GMT  
		Size: 5.3 MB (5263140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88604056d03abc1ef3b327fece87ea7f0429f351804053423edf4afdb2f1ffc`  
		Last Modified: Tue, 01 Mar 2022 10:46:48 GMT  
		Size: 10.7 MB (10689618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cf918a40def0ef2a54f8aa34f15c84c35383777e1fb1019b778d1c40ebb8130e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73736777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9416a3cf6ac3af32a1df140b38f25850e253e092a6f07a6f0d40bff60603f1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:09:17 GMT
ADD file:cc05e2e409ddf6094d6143fb5d4b47dfb3390bc7281658217d6456c28a94c208 in / 
# Tue, 01 Mar 2022 02:09:17 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:44:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:fe6e66c27ed7931bded2ff21e1416e6590e3576bb223676ce7abc704e1326545`  
		Last Modified: Tue, 01 Mar 2022 02:18:48 GMT  
		Size: 57.0 MB (57009099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111e6839c4aa2db70f0f1ec148e3436b2b0964e461965e85327ded44355cb32`  
		Last Modified: Tue, 01 Mar 2022 05:55:11 GMT  
		Size: 5.4 MB (5407372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ee5a5a98edeffbc2270186d55a9d2f1ea5dea3a894a3a0b2cf2ed8cf132b99`  
		Last Modified: Tue, 01 Mar 2022 05:55:12 GMT  
		Size: 11.3 MB (11320306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:08f67eb245fa938e0212fb4fd96182f1b224424b0a377a2af985805c1341015e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70687606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76fb9e87d23c1c62c34176eb3b6e6380eb50367cbbda6901ab6e934a406a31c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:05:25 GMT
ADD file:203c31666290b4e65e608aeb6cf875bc54d17e55d10989248bc2e2de001c76ab in / 
# Tue, 01 Mar 2022 02:05:26 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 03:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 03:13:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b2b0d222db40c7856984c24ac798f37a235dcde0335158adc8c39139ae52f7cf`  
		Last Modified: Tue, 01 Mar 2022 02:15:36 GMT  
		Size: 54.6 MB (54567600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d562f6b968b46a3de6e09307afbb7cfa6dde77f9fcf6233afe17a922240c64e1`  
		Last Modified: Tue, 01 Mar 2022 03:27:17 GMT  
		Size: 5.2 MB (5232082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be770772e21b5a1d959feb0ae9f1caf8620cfa788e9a77787add844ecb690498`  
		Last Modified: Tue, 01 Mar 2022 03:27:19 GMT  
		Size: 10.9 MB (10887924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:513d32b1d653847f4f012a0d9227aab2d8186fde78d49220e81dd5838881dc35
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77636462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d9f7706bd5f1dc2e9e2f17b934432b336e61682cd1b3370b1e378d0b3b4869`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:07:35 GMT
ADD file:b9f003037b742d278d03bf492fdacca507aed7e40b6e3727c8e5053d83d7d356 in / 
# Tue, 01 Mar 2022 02:07:43 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 07:30:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 07:30:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:071265fa048a30ea363f6d7ac648ffe04d00265431517a6f41931d6009cba801`  
		Last Modified: Tue, 01 Mar 2022 02:17:38 GMT  
		Size: 60.4 MB (60392664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f2a2974e7f09a087305fde1cbea3479f9c172ddfb12eedebe53cd4ec065cd4`  
		Last Modified: Tue, 01 Mar 2022 07:45:03 GMT  
		Size: 5.5 MB (5543587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce69ed89337ee2d370f6c9b149d277c8c1c479029a4113ddbfaa0b6783949565`  
		Last Modified: Tue, 01 Mar 2022 07:45:04 GMT  
		Size: 11.7 MB (11700211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c3980de3ed3b025c0d84d5e38516aaccca3a7acdeb4125424201686281a029b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67060604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650dfff09d8b84ea9c4bbf1943958bb863e0d56c07c84dfaeb67baf2ec1491a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 01:14:42 GMT
ADD file:a994e723b30499cbdba960284559bdde2e3abee2fdcb763fdd233da95dafe147 in / 
# Thu, 17 Mar 2022 01:14:44 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 02:01:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 02:02:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:271cb4a0cf55f464e243d145aec35f35f8228420ef9aefb2a52eaabc09bf5c50`  
		Last Modified: Thu, 17 Mar 2022 01:33:41 GMT  
		Size: 51.7 MB (51661116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cead6fedbff27583eae8cbd457b531667d28b94bafbb24b1402d794d4c55ec0`  
		Last Modified: Thu, 17 Mar 2022 02:34:04 GMT  
		Size: 5.1 MB (5077182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8e5e53be16547420594001f871619cc0c003f8d23528375b0f6c4550aaa2f2`  
		Last Modified: Thu, 17 Mar 2022 02:34:07 GMT  
		Size: 10.3 MB (10322306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dc5a6caafc74df788f4e23001700eca261d972645567a7ac41fdf9a370b56bc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70305665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff95eb54deced20fceecb5a0d55e3d7f0b2eb339203e7a4b0aec1231b74ed32f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:03:07 GMT
ADD file:2f65c3757aaa4675484ab3662d157fea03e752f3e5c0b584a7d05649e2599f2e in / 
# Tue, 01 Mar 2022 02:03:10 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 03:54:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 03:54:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b3073d0c9abbb315a4b9ae0014cf38bf506aea211bf49fa8a5cc18e3c3f8e282`  
		Last Modified: Tue, 01 Mar 2022 02:08:44 GMT  
		Size: 54.2 MB (54226570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cce01958dc2b82af4149cffed8f513336e35311876a55434ce123fbf4ab7f28`  
		Last Modified: Tue, 01 Mar 2022 04:01:38 GMT  
		Size: 5.3 MB (5256919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56a31c0ef8012cb8ef744bce50c47373eeee13a4d42a2fb45572f73067f0115`  
		Last Modified: Tue, 01 Mar 2022 04:01:38 GMT  
		Size: 10.8 MB (10822176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
