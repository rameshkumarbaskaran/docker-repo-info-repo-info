## `buildpack-deps:eoan-scm`

```console
$ docker pull buildpack-deps@sha256:b88f44386d96b2e6b54d739f61da93a49aa4d13898c159eb50f2814bd04b993a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:eoan-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e635cf152c29f2bafc5fc879d280689f872df3d8328a320b6dbcf8c2e7396897
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85700377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664caac50be261cce41d3d815b415a4d38eeced4839306a9891bc8e447a71cc4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:22:52 GMT
ADD file:9cf0c9e2d83fd1f85ac0ca5e96b2fba6474f4bda7c20911811337fe11817a45a in / 
# Thu, 19 Dec 2019 04:22:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:22:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:22:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:22:56 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:29:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:29:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Dec 2019 07:29:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc5a81c29aabc68f3accf136ad5d1738904898296a367f807e0afb82c2f76d6e`  
		Last Modified: Thu, 28 Nov 2019 16:34:20 GMT  
		Size: 28.3 MB (28272270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c62728355f60c09e71f3706586cce3f15677526dccb3c47d25abd61ad46e1b`  
		Last Modified: Thu, 19 Dec 2019 04:25:19 GMT  
		Size: 30.6 KB (30581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9cffdd962a232b1d4ac5c63042f1c3bd032ad7be970ad7d2bf2ab18a336781`  
		Last Modified: Thu, 19 Dec 2019 04:25:19 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a46f000fce20f9ea03fcec6689eb2208e780af6528ce7d851a1e287d0e96c22`  
		Last Modified: Thu, 19 Dec 2019 04:25:19 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72e8b0d951ead0e6ef0ad9e865ecae5405c33385a24ea8975e888e6716db982`  
		Last Modified: Thu, 19 Dec 2019 07:41:04 GMT  
		Size: 6.5 MB (6511154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd178d4d1544f0f01ee5733f0ea8642e495243c617b5d15821521ba53886e66d`  
		Last Modified: Thu, 19 Dec 2019 07:41:04 GMT  
		Size: 3.5 MB (3516328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f17b21b0cf9cd26ee276a44910cbb1385690c0f600ea4848ed6a793044a10c8`  
		Last Modified: Thu, 19 Dec 2019 07:41:21 GMT  
		Size: 47.4 MB (47369034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:50796e879bee7f74d9f2cf48eed5df705d81db0bc7ba15fc4eccf2e159c79fc9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75356507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c129fcc29e13109caf3a9b0e2c31aee9aa6813be6c6c8ff67341bee211911b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:11:05 GMT
ADD file:1d649875b914193de549cfee5af0147c9ba102f2a9ff6b1b9da1fce7bcdb8c96 in / 
# Thu, 19 Dec 2019 06:11:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:11:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:11:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:11:30 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:46:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:47:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Dec 2019 07:47:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0d9ed73febf75e7373e7cf94c3b56a7dbca57ece77a2936b9e104aa05bb57de9`  
		Last Modified: Thu, 28 Nov 2019 16:57:26 GMT  
		Size: 23.7 MB (23729416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0ee2639229470d35e076f07de393afbc7996c074307da61d34b523eab703d6`  
		Last Modified: Thu, 19 Dec 2019 06:15:11 GMT  
		Size: 30.6 KB (30593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6374b86e241049a98de23ce22789a03361d0db3d2e3bfc2e05607c9bc14f18`  
		Last Modified: Thu, 19 Dec 2019 06:15:11 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e010d470fd3c21c69efd25118eba9301df9b4e5e6586ddbdb807b4cee82e5aa9`  
		Last Modified: Thu, 19 Dec 2019 06:15:11 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58a8f48bdf590d777082ac17237478735888814daa9f177c526bbcfc1a5ebb4`  
		Last Modified: Thu, 19 Dec 2019 08:01:41 GMT  
		Size: 5.5 MB (5529860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a64b48ab7795f0dc8b8fda368504df08a44b5b3b25b87a0492df61ff9a12aa`  
		Last Modified: Thu, 19 Dec 2019 08:01:41 GMT  
		Size: 3.0 MB (2981428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51cb926fd0f15900cd58a9534380a1d776dc27a5c1bd4c87d7eade9341a6400`  
		Last Modified: Thu, 19 Dec 2019 08:02:04 GMT  
		Size: 43.1 MB (43084170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f5535a6075caa11955a4a26bbdb3a0f7b44c8a8a4b44b75bacd36d7cb252b922
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84162511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601efc6a021f6e8898640b556538505e14a5ac798831a67fd9223f1d47bfc1bc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:52:11 GMT
ADD file:ab7860d075764dd37397c3e6b5cbc424a20f7908293aec76a22f2ee8b74e938d in / 
# Thu, 19 Dec 2019 03:52:16 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:52:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:52:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:52:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:16:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:17:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Dec 2019 08:17:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:87616e97cc89200ca46486ff9c1aa984dacdac7d86cfae973850319782203732`  
		Last Modified: Thu, 28 Nov 2019 16:54:17 GMT  
		Size: 26.9 MB (26874945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07583dc448658d9c9966c3ed29abc9474a5cd3aba4fbf16daa34af3ca349568b`  
		Last Modified: Thu, 19 Dec 2019 03:56:10 GMT  
		Size: 30.4 KB (30421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bfc19bd90414621995cb195c00410e195445c8a89a21abdc4e4bb36706de8a`  
		Last Modified: Thu, 19 Dec 2019 03:56:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64eda46f22fb8ea87f48be3e7c0a31d18ad7c5743bda3162e5b9c3382d0db97`  
		Last Modified: Thu, 19 Dec 2019 03:56:10 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffefd37a86721e1b893f6fe101ecaba34d1dfb713cb2dda10a3e1e26058dc7ef`  
		Last Modified: Thu, 19 Dec 2019 08:31:18 GMT  
		Size: 6.4 MB (6368516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f588a7e4f146b9dd3ea6168dbca57ff4a5beffee6bdfe6e5d8855f8e3f7b8e`  
		Last Modified: Thu, 19 Dec 2019 08:31:18 GMT  
		Size: 3.5 MB (3510060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650cee108cd4ffc4651807ade67e56d4f06b5cc05b1927ad41d94a687ad5db2`  
		Last Modified: Thu, 19 Dec 2019 08:31:41 GMT  
		Size: 47.4 MB (47377532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:dcabc5c38ad9fde270ef7f7e567d125935168a8f99421445a9e39b64688ed0d7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88681817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeff28d3f3464e07486f14dfef5f41a9f70a27f3339784cd3940898caf3bcbbb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:41:45 GMT
ADD file:60638e36e5460700715dad013d492dbf9400675e5d1ae73d65cb8c47eb89b593 in / 
# Thu, 19 Dec 2019 04:41:46 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:41:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:41:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:41:48 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:24:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:24:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Dec 2019 07:25:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d0f0f71ff3bdfdbca0fe246a9ea7efaf3c00bb8ef70159bf4a47bd02ec766d80`  
		Last Modified: Thu, 28 Nov 2019 16:44:44 GMT  
		Size: 29.0 MB (29039478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278eac09ba60b3af672db063d5c3ae1d7d306b953001bcba0135b6f8a87f4f95`  
		Last Modified: Thu, 19 Dec 2019 04:43:15 GMT  
		Size: 30.7 KB (30680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e189c56dfdc3274f1c45b1ba0e7cdeaf88ec0849d941c5872f833f0777353c3e`  
		Last Modified: Thu, 19 Dec 2019 04:43:15 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66c490ba28a2d54d12f11cf63e2fd48431b8691592a458f7511625e2793a9ff`  
		Last Modified: Thu, 19 Dec 2019 04:43:16 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449e0ae18dee54b5b033f6502692e9e825736c9af25bb451947ad5bacf320dfc`  
		Last Modified: Thu, 19 Dec 2019 07:35:07 GMT  
		Size: 6.8 MB (6839547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98214fafe0a932fc37037d4fb83045258fb21d66f274863d0e06c315434a7e9`  
		Last Modified: Thu, 19 Dec 2019 07:35:07 GMT  
		Size: 3.8 MB (3809425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c3c89cf48c9c1fb2ebdc865878e53671ec2f2cc29e81a4c01ba886465b1700`  
		Last Modified: Thu, 19 Dec 2019 07:35:34 GMT  
		Size: 49.0 MB (48961676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8a704f3d6a76a8b8a7b421ccbe116b985f0437876a969e9c3ea588deef0d29d9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100747552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247604dcdd995efb45a9baba5c9e95a62ed6a0ab1f2dcece09b8e0131749b68a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Nov 2019 00:29:49 GMT
ADD file:9290dea355f0fd25335e745c0fe627f8b84c72a2db761a35afb817face3ee003 in / 
# Wed, 27 Nov 2019 00:29:55 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 27 Nov 2019 00:30:01 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:30:06 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:30:08 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 00:52:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:52:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 27 Nov 2019 00:53:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fc4809eaa3c749ba0c119eb0c3f29a7de548ed7a05a27f3598ae160446a29551`  
		Last Modified: Sun, 03 Nov 2019 10:07:13 GMT  
		Size: 33.0 MB (33004041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935dc1bdaba57b30e4b6843b5758929200af42948ecd4ae4ef66b2c317721d48`  
		Last Modified: Wed, 27 Nov 2019 00:34:19 GMT  
		Size: 30.4 KB (30446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e0233504c260871f64281e2ca8b6bdf25d225fa7dfb160804b28a149b80a76`  
		Last Modified: Wed, 27 Nov 2019 00:34:19 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6ccd5d5ba9643d7a6700d586dd042702c5aa7cc28754dcc9323651fdb3d980`  
		Last Modified: Wed, 27 Nov 2019 00:34:19 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d092704307fb4c59090cab1c165b0e310f37c90ae07a84838b126f30ac43e287`  
		Last Modified: Wed, 27 Nov 2019 01:10:49 GMT  
		Size: 7.4 MB (7416917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb7e89827a46dc7b5f0bc148eb2b673c76ce3bb82ab755b48982c3d2e621c49`  
		Last Modified: Wed, 27 Nov 2019 01:10:48 GMT  
		Size: 4.5 MB (4461627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00188c6168736b6a8f1b9091c90857cb5ca7605e766f36ffff7651d60f0c0ec5`  
		Last Modified: Wed, 27 Nov 2019 01:11:22 GMT  
		Size: 55.8 MB (55833479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5f0ee312b9b8b3557dc6e61056beb73f78fe262feef61e90ac0ba8ddd279014f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83242641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0df8dadc8a729bf81fe7f2d8050720e212a26b83f576bd1fe13e44553b051c5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 01:19:15 GMT
ADD file:4c97153d4a7afc971d9aee338ce4f06a9fa3a64889b8f83bbf15781e664bab1c in / 
# Thu, 19 Dec 2019 01:19:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 01:19:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 01:19:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 01:19:17 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 01:51:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 01:51:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Dec 2019 01:51:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6c33d195ae4c0866bde1a47e436c84fdb77b9679e6af4ba02f9e8fe4eaf85972`  
		Last Modified: Mon, 02 Dec 2019 15:36:38 GMT  
		Size: 26.7 MB (26682614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a41d4cb1d5afc1b8f4eae9e396114b62cf41ee529e6a8cfcc4e9e0544b367e2`  
		Last Modified: Thu, 19 Dec 2019 01:20:12 GMT  
		Size: 31.1 KB (31086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8358d099aa1117065a579db0fbe5d90d7155d19f7fd417351329550e1eb99bf4`  
		Last Modified: Thu, 19 Dec 2019 01:20:12 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d3bd335eb5fc325d2f62d526e7ab44b723439a5d4d8ae4fb0d64933d06bce2`  
		Last Modified: Thu, 19 Dec 2019 01:20:12 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02539a417e5b9025347775483e865e15280d755e29bc26f5a8ba4b9c7fec8bca`  
		Last Modified: Thu, 19 Dec 2019 01:58:59 GMT  
		Size: 6.1 MB (6136204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ab36f6b5bb001a73e2d668bcece72f514164de68f96fe0a57987244570e866`  
		Last Modified: Thu, 19 Dec 2019 01:58:59 GMT  
		Size: 3.4 MB (3431857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769983d7022c12733826096f80b2f8badcfdd0909ed9a35be1b54ecec4063240`  
		Last Modified: Thu, 19 Dec 2019 01:59:13 GMT  
		Size: 47.0 MB (46959871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
