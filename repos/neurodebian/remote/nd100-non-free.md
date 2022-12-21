## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:5ee44761f2288e4c3158ff842444c72e6312aae8003e89f292cfacd9258b1cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3337eef4483ede15f11aac8db45594e6bbfdda7e30f44156260fa3c22dd34f3f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61259899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4132dcabd38ae7a4233df9c85ac174d5b349b6985b49db48f7b9f839fa039ae7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:21:05 GMT
ADD file:00d8a84de32d523b936621886a10683664f38d8ec0846a60511fcf3a99d0e0c4 in / 
# Tue, 06 Dec 2022 01:21:06 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 08:59:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 08:59:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 08:59:06 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 08:59:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 08:59:15 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:620af4e91dbf80032eee9f1ff66a8b04119d7a329b2a13e007d69c8a0b337bf0`  
		Last Modified: Tue, 06 Dec 2022 01:25:30 GMT  
		Size: 50.4 MB (50448865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2245a25d386be32e15cb209d70572a5ce2e8f19808eb25fd65202321241442`  
		Last Modified: Tue, 06 Dec 2022 09:01:10 GMT  
		Size: 10.5 MB (10504333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f251a5621e2d77d4d00d757905c8dc0943eeaad16b3036df25c593d0fe89863`  
		Last Modified: Tue, 06 Dec 2022 09:01:09 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a3bd8057c9274a831c3b9344fdf5eaff29fa14979c18c85dadcf32c8cf03d1`  
		Last Modified: Tue, 06 Dec 2022 09:01:09 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a909c1337a444495b088c6f4fa1826a88b05d41405ccc6831699f525152b45`  
		Last Modified: Tue, 06 Dec 2022 09:01:09 GMT  
		Size: 304.3 KB (304332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b131d481005da32acc9ca52e72eb96f8d28fff02c8c4078bcfd071cf6a9078`  
		Last Modified: Tue, 06 Dec 2022 09:01:17 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b8a5ca1e768e4024b1623e757bfc1076af1d396b5a2ee26ca4a5657603158a35
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60050624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c31fba635ccf084a543e28263d1a683a2e7de0d2cda22c7e7fc3bb0342d084c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:24 GMT
ADD file:2deba7c04e28d01997b865f366cdc8d38a80aa39720c4e4d1fc581ac17e8ce4a in / 
# Tue, 06 Dec 2022 01:40:25 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:06:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:06:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 04:06:24 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 04:06:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:06:31 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:47d0ec2abdb05569eada58143acd16d47ee4b07a33535544cf5bf267bde20cc3`  
		Last Modified: Tue, 06 Dec 2022 01:44:13 GMT  
		Size: 49.2 MB (49233737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e928f3f303597bfd9fba2e92cdcf920d9fcafe42efca63103692d4366569b`  
		Last Modified: Tue, 06 Dec 2022 04:08:12 GMT  
		Size: 10.5 MB (10510258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8461cf556d4a4eaeaf44cbe29b1878cf0ad26ef6e36e98337ecc9eb7377b8367`  
		Last Modified: Tue, 06 Dec 2022 04:08:11 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feef9992ce9a2afe0529457ef73f13aca535f78aab518de102c86fe7217e2d1d`  
		Last Modified: Tue, 06 Dec 2022 04:08:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7ec231f354dd9452eb9dd010b908af0dee64ae8f3539f3420ce581f6bc97f8`  
		Last Modified: Tue, 06 Dec 2022 04:08:11 GMT  
		Size: 304.3 KB (304260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a274d6b33fdfdb3ff03c24d6b48fa9c1ad2b67698ae87efc6628f0a9f2a6c03`  
		Last Modified: Tue, 06 Dec 2022 04:08:20 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:4d0edd2ffbb95b464e028b9d3f3cf6202f7cbdabddb63d4cd9e4872d471d10ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61991249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27095cc01ae4cf0888ce60eb0b06f0a94b29d9fb64b70c41785b7766d8885da0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:32 GMT
ADD file:761d50db794e5887a7dd528cff032401788413ed374043f8995fb4370f61a175 in / 
# Wed, 21 Dec 2022 01:39:32 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:34:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:34:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 21 Dec 2022 02:34:40 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 21 Dec 2022 02:34:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:34:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:e8258458fa95364a2e7bf12aba19bd9fab7ebbb3144d9ff63b54fe3bdb605cc5`  
		Last Modified: Wed, 21 Dec 2022 01:45:08 GMT  
		Size: 51.2 MB (51207743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de5d1427dca0f93a35bcca8a34e38ea32e913c989d6aa1778817f6396b66e20`  
		Last Modified: Wed, 21 Dec 2022 02:36:57 GMT  
		Size: 10.7 MB (10672412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c448db8cbc1bbed9b412d8cc98b6f84bd17eda6b7ea974671ed057fab2eee6d`  
		Last Modified: Wed, 21 Dec 2022 02:36:55 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b4734dd8d3e19630ce11cba08a607c262a512622a8e19c2f3d86897972e32d`  
		Last Modified: Wed, 21 Dec 2022 02:36:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa99cf2032f4733c5f3da15e7c8f0067a52afce295dcbab3317bad361456e4e`  
		Last Modified: Wed, 21 Dec 2022 02:36:55 GMT  
		Size: 108.7 KB (108749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b773cc7b29c88e8da913705a98e97793e9fa4dbbbe90a9c0ac5b9a9d72779628`  
		Last Modified: Wed, 21 Dec 2022 02:37:06 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
