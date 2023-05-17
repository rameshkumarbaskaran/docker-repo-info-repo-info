## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:739a12ea2febb8f1a7837fff4b76740956ecc9bfa95fc0fe55930df722de8131
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

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1897d92f0c0450dea079a00f090ac723ba0393c31d8495f63fb3324d4c071179
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69541632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a7789e59b7819ec8fc1a3212b107cccf937b88e1b382a152a4b67cb4ce1110`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:46:33 GMT
ADD file:168af20819ee8d7bc6ca3fd35873fe0b65f567f6fc4763ae2fed655e04826ef6 in / 
# Tue, 02 May 2023 23:46:33 GMT
CMD ["bash"]
# Wed, 03 May 2023 19:56:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:879480f6969a02afb639ba9b35bc2df992fec064538a2e8af5e14cf6b6fbeac3`  
		Last Modified: Tue, 02 May 2023 23:49:26 GMT  
		Size: 49.3 MB (49299247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd0eff3468a08b4cdf12f032ff78080b7173e0fe025644e187e4ce067d8cec4`  
		Last Modified: Wed, 03 May 2023 20:12:04 GMT  
		Size: 20.2 MB (20242385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:686f4e2958d9717c85d7ecd47afb28b85e936e9b6125e4f92c53c3de8c6d338f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71182954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058dd6de3ace689f95f91bfbfedc107545bf0ca1041e45a3a4974df1f9e19b00`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 22:48:29 GMT
ADD file:1ecd266ebf23430d2ea2417b92ebee6029d940fbe99297183c4f811e24fdffb7 in / 
# Tue, 02 May 2023 22:48:32 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:48:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbca433c216350213a8b219e118cb55f422acfc53f49c76c44e044b42a5c0aa6`  
		Last Modified: Tue, 02 May 2023 22:50:27 GMT  
		Size: 47.2 MB (47167199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a510f555be9d50bf04a0e432e1da4122711987bdbb2544b99200d53b8ca8e2f`  
		Last Modified: Tue, 16 May 2023 23:54:02 GMT  
		Size: 24.0 MB (24015755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:09b0b458ca80ea55cd0140bfed1d90fb36b9225eb307fd93347d0e2bedebc70e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68206140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1de8c54842549f1984a85e4b0a0f679e93596e0ef37c40ca0c78317349342a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:28 GMT
ADD file:222aad59c348a6e07dd607ba4626497e12e5054fb651c9c30d5a4c5a8b3e4c82 in / 
# Tue, 02 May 2023 23:47:28 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:59:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:326cff266909348fa4e168fc7e76fbd52cc4855403565526a5ecd2e6bdb9d26c`  
		Last Modified: Tue, 02 May 2023 23:50:34 GMT  
		Size: 45.0 MB (44988072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55abb83f097438eeb001ad7afc4116735e243a512d7cfda49cdb7b6bd1f009b9`  
		Last Modified: Wed, 17 May 2023 00:23:16 GMT  
		Size: 23.2 MB (23218068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:050126935e17e454d13efefd96153cb253adf8c0c13d82637a37f2576ef0554e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74243827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f61cfb9cb43c8fd17b751dc11d98ebae1da9d7740fa480b5fdadad9d166068`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:25 GMT
ADD file:1af23b8894efa507a47bf873cf69ecaa5ea13b618cae85b8c46125af6399b4fb in / 
# Wed, 03 May 2023 00:22:26 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:15c964cdaf05fdeddcf9bddd79eba05f71f2859fee9c193ba5d19a237f7fb92e`  
		Last Modified: Wed, 03 May 2023 00:25:01 GMT  
		Size: 49.3 MB (49345335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1426a52e9479646762d18e7a8f0b801f6ba0cd16196e4619fd66dee64a27715`  
		Last Modified: Tue, 16 May 2023 23:56:18 GMT  
		Size: 24.9 MB (24898492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0163969e2591309126bf9ef24ba305b74c4168f5c3fe434387e388457f6c7815
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76514887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1efe97178e0a1c969194624a38e47f8e7d462ca8496e9561217be27cf6cc11`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:00:17 GMT
ADD file:cd02b45138959c7ec7d466eff66efaa68d03b2e72f294b468f08c576643ac084 in / 
# Wed, 03 May 2023 00:00:18 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:40:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:028db28caf3d2a0b3bc8b8281c9f370a6ca8a97954f596e2b27e20ebf7f3b578`  
		Last Modified: Wed, 03 May 2023 00:04:07 GMT  
		Size: 50.3 MB (50321827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3febc6af3fad6009c9ea3e2a5a4f667dfb01b41d973376f8783dc1a8cb0386c3`  
		Last Modified: Tue, 16 May 2023 23:45:46 GMT  
		Size: 26.2 MB (26193060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9629f9e6e9d7c6760fd673da33fec3726b10b550047bab2cb998e7e3c2a23f62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73508539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743529d4a72eaed51f20c5871d3576b82c2f65f31587e3fe7ece5ae2572d8a9a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:29 GMT
ADD file:ff6384c951ff8b6254c1c1f02c689314e2f30a43e4b60dcbf54c82df826f734d in / 
# Tue, 02 May 2023 23:47:33 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:44:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dc6b7fd1001cc2b329d98b8ea6ca86f4be0bff6654b36678fc5fa01f2f599145`  
		Last Modified: Tue, 02 May 2023 23:56:18 GMT  
		Size: 49.3 MB (49301357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d31482ac1d01bb4da186f1d7d1efabcbad13ce3186c1582781afa6d72d5b3b`  
		Last Modified: Wed, 17 May 2023 00:02:50 GMT  
		Size: 24.2 MB (24207182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:58f1263c1585fa9466471d324244587357cdfd375ab7b80afa1da080cbbf7f22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74893152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6be993ff92c59ff217efd0ece8fb26fa183b83e62c4567ef0e8a24179e3901b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:30:45 GMT
ADD file:25d67bdf8a8d7f1826107ec67b95338418561c0fd3833ca3065cf965e82b87f7 in / 
# Wed, 03 May 2023 00:30:47 GMT
CMD ["bash"]
# Wed, 03 May 2023 23:09:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e614e0d26e774be63c67b7f9f168ad3982d113da743f11dd74fec77e268d7e0`  
		Last Modified: Wed, 03 May 2023 00:35:40 GMT  
		Size: 53.3 MB (53307301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2b7373c4795c4edf6191c6e8844069ddb2239c4fc2e171691720178d865cbf`  
		Last Modified: Wed, 03 May 2023 23:35:19 GMT  
		Size: 21.6 MB (21585851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:64ae443213e76043cf30e363d4296236f3d3ab64406ddecc5e99997237cd1c26
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73030194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c241fa9464cd38e78fb0343051f1c5dda7398fb8c06965ac0209ba5e89d26898`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 03:41:05 GMT
ADD file:2b13279140b98de657b363865f9ee14f0c5c26df191533d1c5438dd1df5948ca in / 
# Wed, 03 May 2023 03:41:11 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:41:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f966d911ea531e8d55499ff0d85338412ff6e8012a1639d691e4bc5ecf08d42`  
		Last Modified: Wed, 03 May 2023 03:44:23 GMT  
		Size: 47.7 MB (47675931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a0c25941897af74b548e8b3030a4f6d12d7e0540497c20305c519e8b6a89e1`  
		Last Modified: Tue, 16 May 2023 23:54:59 GMT  
		Size: 25.4 MB (25354263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
