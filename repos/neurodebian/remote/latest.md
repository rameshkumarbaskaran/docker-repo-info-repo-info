## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:bed3b91dedac313128cc244bad638737abe3aa3ea38f092e68cc418d0cabcb8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:ccd1b59aad87a7c82820e157082bac2be35db3aaeb5a21b86b72ccf0d17bc03a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66671505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de330a89bf9b3656ed0d4909c39ff822d84609fe0be661455e5ef82eef9375b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:05 GMT
ADD file:b03d13d345c29f69557f410c8504e748226756d1f48e5abdb63cd40179b2640c in / 
# Thu, 09 Feb 2023 03:20:05 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:33:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:33:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 09 Feb 2023 10:33:05 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 09 Feb 2023 10:33:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e4aec178e0864db93a6f97a20bde3445871a4562c1801185eca1238d3a0e80d`  
		Last Modified: Thu, 09 Feb 2023 03:24:47 GMT  
		Size: 55.0 MB (55046771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6748fef26b12a93a8ea2e78ebc615a49a0a17ea28b338a2543564de8dbe7a6`  
		Last Modified: Thu, 09 Feb 2023 10:34:52 GMT  
		Size: 11.3 MB (11310827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38f8febb6240b1c0efe213c5ec66b0a670a65bacc58a728ee49d9595476b44d`  
		Last Modified: Thu, 09 Feb 2023 10:34:50 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feab659e925660d862b7b1085bba84ab6e23e3cf0a732dd7c751b691c5450539`  
		Last Modified: Thu, 09 Feb 2023 10:34:50 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b37097c0f732899899760f1a0ecf4d28df4e71f373ec4afb9bf706badbba17`  
		Last Modified: Thu, 09 Feb 2023 10:34:50 GMT  
		Size: 311.9 KB (311894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ed309fb410afe965990c2418d26dc13a54bf467f579157a7c6f5bae7dee26420
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65330288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9463c6b90f601d839de54e2c7e27fcab29a5386148c6913850ed213c1aa42acf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:29 GMT
ADD file:5cf2de182dac36d99ec41918889c9755f9c49c56fa0a8d0ca14040c1d8c04541 in / 
# Thu, 09 Feb 2023 03:58:30 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:51:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:51:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 09 Feb 2023 13:51:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 09 Feb 2023 13:51:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80dae1b9d879348c210c40024c6e90ef92677ac3515456375fcbb70bdf07b104`  
		Last Modified: Thu, 09 Feb 2023 04:02:11 GMT  
		Size: 53.7 MB (53703368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2629d6c817e5dc51a2450a8efd843508b2e4aa5fded18c3d771670e8c825dbe`  
		Last Modified: Thu, 09 Feb 2023 13:53:08 GMT  
		Size: 11.3 MB (11313106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76535df9fe4fcd5bc0465b83953ad4110959f58c3ec203fa2728839df95f45c1`  
		Last Modified: Thu, 09 Feb 2023 13:53:07 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f873b53aa4215e3b149b5b2c7e2fdca66bf7f86bb695dd531304413404badd`  
		Last Modified: Thu, 09 Feb 2023 13:53:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a70f2fa11626b1293081227cb120c69cee39b2e355569beeb6855fbe045880`  
		Last Modified: Thu, 09 Feb 2023 13:53:07 GMT  
		Size: 311.8 KB (311800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:ce1fbd72b2cdd70b4db22df3ec6da4ef9fbd3e19547c5d0af564a7d774eff1bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67637598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc5eeb71cd5570608df1aec87502a7e2016fbe882237e0f216f1b8d1bcc14a3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 05:12:37 GMT
ADD file:feaff299d3310c04952143a422f0d0bdd292cd174513c54b1f50765cdbcfd401 in / 
# Thu, 09 Feb 2023 05:12:38 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 12:43:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:43:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 09 Feb 2023 12:43:28 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 09 Feb 2023 12:43:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9708eacca143ba8fa6c7e9a5b05456412b7b16629c20015a43f3ca391e066162`  
		Last Modified: Thu, 09 Feb 2023 05:18:13 GMT  
		Size: 56.0 MB (56030197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc6553645eeab9f9390c2c8b8a61e7694834123049b6f060dbdbb11ef6b6819`  
		Last Modified: Thu, 09 Feb 2023 12:45:34 GMT  
		Size: 11.5 MB (11500078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e1e93c20ee20a385a9d97ed62c22e11afd73974b6821310c2baca0eb530970`  
		Last Modified: Thu, 09 Feb 2023 12:45:33 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a06c277f46a387d7ed96bf2575c4552a533f0d45c754c0680a1d8363ffebde3`  
		Last Modified: Thu, 09 Feb 2023 12:45:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7d84f478365f04d8d680da68bd0b3ea6cc10a025630c140d289b3a0a6c8705`  
		Last Modified: Thu, 09 Feb 2023 12:45:33 GMT  
		Size: 105.3 KB (105331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
