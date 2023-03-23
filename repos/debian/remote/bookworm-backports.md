## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:ca466a55ab03ff64f51e5aa64b9257ca964682673c92457c6dc2c64eb4758ad5
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:0e75dc48efef655a6f7a4efd18d062de38fce2f24d9dc4f1051a39524f622341
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49237498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8527e8bd3510ed76b434734092a57968f5bda60807471b5c54338f1e248f3a2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:21 GMT
ADD file:74b4e0fbcb9cb38344c32a0512a72d8179f885de4b7bb127215f8d96a6262664 in / 
# Wed, 01 Mar 2023 04:09:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:09:26 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9d915a4248d2913bb8451eba978ac348a983990eca9186543367f5f44900e0fb`  
		Last Modified: Wed, 01 Mar 2023 04:13:25 GMT  
		Size: 49.2 MB (49237273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbdf461f58d9b4bfeca1878bc23d12676f12febee37ef0493e75610a8299c5a8`  
		Last Modified: Wed, 01 Mar 2023 04:13:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:104c0466a075f1cd7ca16ed7801a72b79bea9dc63ab604ce46c3054e4399504c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48073064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57517505edda4579869169dbee7d4f0a4e766250e01909274026463da917529`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:48:24 GMT
ADD file:1685939a153ab7a7aa03035565c60e99663abd3a416ef0d00bddaf24e0ae6f08 in / 
# Wed, 01 Mar 2023 01:48:25 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:48:30 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f7516928cdf57280d137bb31220dd9f0b6ca54e290189b42a68ab64d0d2065b7`  
		Last Modified: Wed, 01 Mar 2023 01:51:43 GMT  
		Size: 48.1 MB (48072838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba9b375e1769f8d21f3b65be340b87906da55908c4f4f61398d46209bcd997b`  
		Last Modified: Wed, 01 Mar 2023 01:51:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:8575f0588ab580eea1d3f29474ab334b64fd607a2ad5767e61f7bbda7b1d2d91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45843527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93284d62e0881b589c00663dc4f98c77b9f4666f08a41b28196c0519b573cb67`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:26 GMT
ADD file:9f8ce83cf3e75c63cb351ec688378ffe29d7105ff8e8892b3cef95aeacbf6779 in / 
# Wed, 01 Mar 2023 01:57:27 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:57:31 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4c5d14f15cd67359c9f8d5dbc636ce6ffee972aa4acbeb663e40e865b0dd7dee`  
		Last Modified: Wed, 01 Mar 2023 02:01:54 GMT  
		Size: 45.8 MB (45843301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243101e199090a32c224d7f3a66065d74d6119b53f7a8be67ca6fb61023a0a28`  
		Last Modified: Wed, 01 Mar 2023 02:02:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4fd8f0003ee3744d36ecc4eaafc406b5db0907d482f1247ea5407e4fff8ed134
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49328503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0466c46f51ae77128f02600968654dfd793bae9ab1794a537c54ad1e21c1cb8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:44:48 GMT
ADD file:fc54d0a42f70d91c654d7ac03aa3d437fad192d9f4fd701e214da74c18630636 in / 
# Thu, 23 Mar 2023 00:44:49 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 00:44:50 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b813e5ae6de73806a605f44184f1b7d14569e88447b46841154803d1dd1eb646`  
		Last Modified: Thu, 23 Mar 2023 00:47:13 GMT  
		Size: 49.3 MB (49328280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b17967d612dc392ed52fed540e556b18298da158f7c9a2f576bc96d131f432`  
		Last Modified: Thu, 23 Mar 2023 00:47:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:460a44ab5412c9c20200c75fa547ede316ccd1ea03a421ab927e9990a595e25b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50324158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f679498ab7edc57c6bd1ba939837309b93837698ed55b082d7866242d5ca5926`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:38:46 GMT
ADD file:a8b128db07f7f5c47ccd2afe2595fdf9b31844beff2d07ae2ea0e204e2aef4c9 in / 
# Thu, 23 Mar 2023 00:38:47 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 00:38:49 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4dc30e65d953c72fa1dd5a25980f7eeea620434c102211fdb72a04706c06dd96`  
		Last Modified: Thu, 23 Mar 2023 00:42:07 GMT  
		Size: 50.3 MB (50323933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78cf2d244fc0ceacc5b5f0799be9f3be977adee14abc6cb94dabcac94157ec3f`  
		Last Modified: Thu, 23 Mar 2023 00:42:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:426644b7c42f4bfbf79c83df43c9259ba4cf8e87a7b748e69cd2cdfc425ff148
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49245700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc6fa77ce6a06ef64509c5e404fd8c94c27d7f0e72bba49fc8aff64cbd52ef0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:09:05 GMT
ADD file:77abd413b6799ae4f1f24f3bcc389dd12515fc4f732e81239d8c25475bc37fac in / 
# Wed, 01 Mar 2023 02:09:10 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:09:20 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:65f9863fa983221d5b14b7a7e06e92e49a04fbced0e7af12bdafbdfcbc7a2deb`  
		Last Modified: Wed, 01 Mar 2023 02:16:56 GMT  
		Size: 49.2 MB (49245473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64374528e42fffb9a9f08b972942128c40c8f8b48283c666fb226f8e5b6bfb75`  
		Last Modified: Wed, 01 Mar 2023 02:17:05 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:6952c55216b84107295acd48cf512b88d7ff3727ade295e10d373e24aa6d5f06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53250456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4fd735caf91c9b1f4d03b260ad3172101c05be5e0b2b7da50ce1ff9b01d42a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:46:00 GMT
ADD file:311d9174b941eeaaa2babe3a94b035ab7c3880d5908d630bdec420f42eff6a06 in / 
# Wed, 01 Mar 2023 04:46:05 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:46:21 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6b61b4a96c9a944bd44d67cc885cdb2ef5f9aa35a0a94dba6ea2b6372ad27e48`  
		Last Modified: Wed, 01 Mar 2023 04:52:26 GMT  
		Size: 53.3 MB (53250230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695a39025abf7b07d247dc12f9d0b285b7f824b1690a656b54cb321d27e1586f`  
		Last Modified: Wed, 01 Mar 2023 04:52:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:c63ff8b19dec1f5380e763eb9313d772704a92d6ba93e6835d18ef933f2f0975
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47671261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eeee0290269cc8658da057af0ab2729901862f45a46855fcd6266b01af0371c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:43:22 GMT
ADD file:2114d04d7187ee787a64bd515adc18fc532b91c0272b95492fd44714772b3eb4 in / 
# Thu, 23 Mar 2023 00:43:24 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 00:43:31 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:09c6f64f2013e0d0258d4e75a51c004bfcc5479af28502ec4cbf6e25f28ee505`  
		Last Modified: Thu, 23 Mar 2023 00:46:39 GMT  
		Size: 47.7 MB (47671033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ce71ab9828c634a772b629abfa1a12ba9ce2a7d1da8b25e62b8c81060419d8`  
		Last Modified: Thu, 23 Mar 2023 00:46:45 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
