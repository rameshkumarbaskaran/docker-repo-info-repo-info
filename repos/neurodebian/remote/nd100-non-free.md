## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:e6523b07526e368e1ed1ad5cd5ace1816af73b2c558f95dcdb6d3ecaa7a6a659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:36baea0d92be742ffacd3e287f3aff751161983cafac9656a231765c900b5b34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61258767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c289b0f5dc037a7f60cd95e66a73e31a506be771f2aaf96d656292db28d88c5f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:02 GMT
ADD file:259be79d94a2549a667ad08a093fe18f15a6c93d66a0723292f49294e31fc7a1 in / 
# Tue, 25 Oct 2022 01:44:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:13:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:13:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 25 Oct 2022 04:13:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 25 Oct 2022 04:13:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:13:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:fd31ec14dccdcda8f2472547f1a94ef0a23b8dabb764cd7b1d48aeee0afea7c8`  
		Last Modified: Tue, 25 Oct 2022 01:48:15 GMT  
		Size: 50.4 MB (50447742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9122ec6aa2a6194ca00862c6d9350bc5b3a8b530dfdf48dd3973cac441ddb49f`  
		Last Modified: Tue, 25 Oct 2022 04:15:59 GMT  
		Size: 10.5 MB (10504344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4c20cf0b981052b23457bc1f8457f68bd7515cad276917ba46fb57144c755d`  
		Last Modified: Tue, 25 Oct 2022 04:15:58 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb9a440939dfe96a44b07dfa89426581578c53b5e5d02c8b8b02b74d3fc9305`  
		Last Modified: Tue, 25 Oct 2022 04:15:58 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879b3b855360c632fcecd2c95dd76c57425ff8bb0dc3e9d94794896068a07ebf`  
		Last Modified: Tue, 25 Oct 2022 04:15:59 GMT  
		Size: 304.3 KB (304315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ae27cf1fad4a72965222c9604eb452c169583c3844584aafc24d68824bf812`  
		Last Modified: Tue, 25 Oct 2022 04:16:08 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ffb9d19fe8c03c95431cdccedf93b7cdf41a3dcd3cdc68025c93e4531af03b70
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60050114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ef527ff2a63b510dcf913ad24e4088ca04416888755766c1b9a5f769771a33`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:07 GMT
ADD file:21afa32c0395cc5046d09741d6821d21cfd9b77bce46ebcfc8fd9aca57c73648 in / 
# Tue, 25 Oct 2022 05:46:08 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 00:33:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 00:33:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 26 Oct 2022 00:33:28 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 26 Oct 2022 00:33:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 00:33:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:3ba81f4c3c21f92780061ee116827d64ac4edbcd02b056845c2aaa3097b730ed`  
		Last Modified: Tue, 25 Oct 2022 05:49:24 GMT  
		Size: 49.2 MB (49233280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff53c60eac6d1dc3c271e3361822a2783054fe9b43ce44af55bae172bc8c9334`  
		Last Modified: Wed, 26 Oct 2022 00:36:29 GMT  
		Size: 10.5 MB (10510227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69f9a270c61cf8475095db25ff69291bf57d46d9bf06aa449ba03ae1d8ab0ff`  
		Last Modified: Wed, 26 Oct 2022 00:36:28 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61fe36b36c040fbeb49c421a37b912e05a2b157dc791445ab1a86f0209e6d281`  
		Last Modified: Wed, 26 Oct 2022 00:36:27 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5b04745e6d32a3cbeda610fa27f4eed0c107aa63e0719cd2aa548f5c547226`  
		Last Modified: Wed, 26 Oct 2022 00:36:28 GMT  
		Size: 304.3 KB (304252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0323693c7aef794cfff76d90c4b1ee63643a5cf3acb57149dc1e10f47cff6bc`  
		Last Modified: Wed, 26 Oct 2022 00:36:38 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:02087f06598fc2afa2769e0db26c9ef36ce321bdfad9982c937f17f01f2464be
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61990996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7cefda656644799350ea5ccca373c1111efd90d03ac4acefd66a7c392fef21f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:38 GMT
ADD file:e8c5010609ee5ceb22093e461dbe3f9748a4d6ca2fd436e635276b0f99e777e8 in / 
# Tue, 15 Nov 2022 01:41:39 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 09:04:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 09:04:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 15 Nov 2022 09:04:05 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 15 Nov 2022 09:04:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 09:04:16 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:a9674eda0741cb717f181697e2f2695ea87fdaf557d253407a096f80ad4f9fb3`  
		Last Modified: Tue, 15 Nov 2022 01:47:27 GMT  
		Size: 51.2 MB (51207653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32b7bcd7087544177338284a50004d2e02cfac59dd38718c22498da128bbf35`  
		Last Modified: Tue, 15 Nov 2022 09:06:25 GMT  
		Size: 10.7 MB (10672283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3dbcaf37259f807fbefa9fc997c00f13a7ff211a7422ea0aa4bb5e0a988062`  
		Last Modified: Tue, 15 Nov 2022 09:06:23 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27da7b13055889d8af547a5b80c4aecfddc77e8dfc31bc6f77b3b87ac174a246`  
		Last Modified: Tue, 15 Nov 2022 09:06:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85d8557710c21914b39bdde005c03e499ccd54f844f892dbff926dfd8f54d7f`  
		Last Modified: Tue, 15 Nov 2022 09:06:24 GMT  
		Size: 108.7 KB (108716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898aa8fcc1d1273071a252588933e8b5bf9710ec8c945726beee1d79a3adb2cb`  
		Last Modified: Tue, 15 Nov 2022 09:06:34 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
