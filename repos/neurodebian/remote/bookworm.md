## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:0b6f90e056cfe222aaf85c14031c24ea5c7635039e10791386f7d8644e3f74b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:9d603bdb418f3bb44cc7556cf26fb247c79cbc9c7cab8cd2760f131fa9ead460
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61303309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aea8dec3ae15d48cc5f8d86eb459a96be59bd5375fa156f4d339305392a1eea`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:28 GMT
ADD file:98cacc5890a8c0b29d7a2b296774428cb2268b01b4ff97a84deadcd3b513f319 in / 
# Mon, 12 Jun 2023 23:20:29 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 07:13:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 07:13:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 13 Jun 2023 07:13:04 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 13 Jun 2023 07:13:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bba7bb10d5baebcaad1d68ab3cbfd37390c646b2a688529b1d118a47991116f4`  
		Last Modified: Mon, 12 Jun 2023 23:25:26 GMT  
		Size: 49.6 MB (49552112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc87ad854beee02a319572d16a9ac68c59d59976aedfa35e8e09bd993e4385e`  
		Last Modified: Tue, 13 Jun 2023 07:14:33 GMT  
		Size: 11.5 MB (11462925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffc38cd88fd0c537a31dcb160d54d7869d712aa92cff8c7914906121e936228`  
		Last Modified: Tue, 13 Jun 2023 07:14:32 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360d045b18c53a14406ee03775782666e65a64cb6fee2ecb240230caa1fcae45`  
		Last Modified: Tue, 13 Jun 2023 07:14:32 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9317f0f8a72c1638bbb4f12fdcc7db5bd56b302a27ebbe6c6c66a40a9b661`  
		Last Modified: Tue, 13 Jun 2023 07:14:32 GMT  
		Size: 286.3 KB (286263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:05cf73c282c5e7716e68b6613788501127c43ab480df29cf3b0827eed01ec26e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61288274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6572d2f98eea9113cc00e57b32259552e2915ab6b46ac64625adac10008a24e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:39:59 GMT
ADD file:0dfaa4beac7b0a95f2b33bc35e08b104057469f46fa35df2af7193451ab3714d in / 
# Mon, 12 Jun 2023 23:40:00 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:33:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:33:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 13 Jun 2023 04:33:17 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 13 Jun 2023 04:33:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a31111d070044ed920abddebc16bfa67a69fb0e0e782b703073c93ec10dedf67`  
		Last Modified: Mon, 12 Jun 2023 23:43:47 GMT  
		Size: 49.6 MB (49573162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d213aeb43c4397dd620ab43f9914b1013b3ec4046589b61d13a11e1f2c880c`  
		Last Modified: Tue, 13 Jun 2023 04:34:35 GMT  
		Size: 11.4 MB (11426538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cacfe086403ffef5add85bc0afdbce9bb86d32f7d969a86a51ffdc6bd5b6c09`  
		Last Modified: Tue, 13 Jun 2023 04:34:34 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e93a9d8410d509233fa7277f2e47ce578fddc8309b451bd044442bfc741d2bd`  
		Last Modified: Tue, 13 Jun 2023 04:34:34 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5e2c70d3523e9e2be3b712e4d0e10fb3c31578f72d41c281c4ac2d64b2dc8c`  
		Last Modified: Tue, 13 Jun 2023 04:34:34 GMT  
		Size: 286.6 KB (286565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:0b684d08e78e5713cbb0103c4aec38a580807d3f961fc080ec6a140df98d95c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62733943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:385d94a52abe893a26c36f77c0c71ab0688a40417f5e10c6b2881527c40e66f6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:39:02 GMT
ADD file:a0aeb9b361b31d75c8d96223fac8f3df2807735ed20715b24af45a414ad3965a in / 
# Mon, 12 Jun 2023 23:39:02 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 20:18:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 20:18:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 13 Jun 2023 20:18:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 13 Jun 2023 20:18:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9cf3331eb07181e9e59fdcd7e0dff8a268c9d12151911a49cf687e8007305b4`  
		Last Modified: Mon, 12 Jun 2023 23:45:56 GMT  
		Size: 50.6 MB (50562393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1550e022c5b9c57bb35f68e4560a45dd92ce336d78fad56d5bf671af67fb255c`  
		Last Modified: Tue, 13 Jun 2023 20:20:01 GMT  
		Size: 11.9 MB (11883202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd3247eb40ad2b9b30397b4020999d281f44617d4f96474674c2c90cb842763`  
		Last Modified: Tue, 13 Jun 2023 20:20:00 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6305dcfc4637c5acf3af02856be089da9a5ebe9e6caf3f8713ac20651c5744c0`  
		Last Modified: Tue, 13 Jun 2023 20:20:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa0529a058564bab52db5ef4d99d7a58e982ed4534387320956c73e08114cff`  
		Last Modified: Tue, 13 Jun 2023 20:20:00 GMT  
		Size: 286.3 KB (286339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
