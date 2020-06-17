## `buildpack-deps:groovy-curl`

```console
$ docker pull buildpack-deps@sha256:b82ea3632d3281780858cf378bd7c9b05c83b9c841b178e926ee3aac126306fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:groovy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7a7c1b02d57bdd1cbd1cff649fb1fed7e9a8b8045e79d0a512b0ddead401179d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38647385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef14e463a3989cbcd10c934ebab802aaeb81024ce59e20b41d70f82bf94494ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:05 GMT
ADD file:92952db7a9177df30b622431b9f8fefbcd7a939849c42bf0c4f13bc351e4afcb in / 
# Wed, 17 Jun 2020 01:21:06 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:21:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:08 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:08 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:06:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:06:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0b4f5d796ad9b8be2c7e6e6bf2af20f7c4d7767f09d685031e8d2f74f88aa976`  
		Last Modified: Mon, 15 Jun 2020 15:48:18 GMT  
		Size: 28.2 MB (28170426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ee7132703b3afff26639216d0405c82708835c086de365d565d615e3f0921f`  
		Last Modified: Wed, 17 Jun 2020 01:22:12 GMT  
		Size: 31.8 KB (31847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672e5b34dda87e71c8d1974483aa2b77b73924fedab54ffe098b2a7c51fa4cf1`  
		Last Modified: Wed, 17 Jun 2020 01:22:12 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3af786f5e76b85e0e94a65a039de3975fc9e68d8bb556a69b78a2b0ac7fda9e`  
		Last Modified: Wed, 17 Jun 2020 01:22:12 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc47e1a433fb6c2ae6f980146437f404f65015e26ad681b7545a55fa027947cb`  
		Last Modified: Wed, 17 Jun 2020 02:15:24 GMT  
		Size: 6.9 MB (6858029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c072bc86be0632ba75054e6c24eba79b00be53f93ba09cb7a2fa8991a81efe`  
		Last Modified: Wed, 17 Jun 2020 02:15:22 GMT  
		Size: 3.6 MB (3586070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:93ec3fc2e5c1066981faef35c62c6561d1badc68998794db48b4c03fedc8bbad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37102610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6fa415ac4690c8a0473c84c41e93072fc3177194747d4d5d631d6f64911154`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:47 GMT
ADD file:79a5e9ec755c39a63ddb87e95abbaa4e7f58c2b21f6fdc989988bc596132fb0f in / 
# Wed, 17 Jun 2020 01:43:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:54 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:54 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:24:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:25:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8feffc3ef06df85a0b885c9ed0142729b9b6ab40b1ae0e1c80acf8a166828332`  
		Last Modified: Mon, 15 Jun 2020 15:48:52 GMT  
		Size: 26.8 MB (26776408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1d229880df445d6616abd62f73150dd4f69ec83ea2518df98a22cec7717992`  
		Last Modified: Wed, 17 Jun 2020 01:45:32 GMT  
		Size: 31.8 KB (31828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ebd8c9dbc7b239e6537d01cb2f8917d318937078b6d819e53d9a3a917c87cb`  
		Last Modified: Wed, 17 Jun 2020 01:45:31 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9ddb4021ce9fc1951e508097c3b6a69b56a2c35e4ba359eaf7d34f4a2a7d98`  
		Last Modified: Wed, 17 Jun 2020 01:45:32 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a569956bd7671cd8fa38ddb4bab5fc8fceeaa983e4e8087038713c1151ca5a`  
		Last Modified: Wed, 17 Jun 2020 02:37:48 GMT  
		Size: 6.7 MB (6723097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3a7850e58c8474f9bab15e156d61b1b420b0d2312ede7dcb08d6538d7e3329`  
		Last Modified: Wed, 17 Jun 2020 02:37:46 GMT  
		Size: 3.6 MB (3570240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d0638ff4248b696ed256d28252ea5547b973ced87e0d09073591fd0f2a5f449a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45123073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8c7bbad6389807c52855bdb81ff1dc9b30b954a1211da0d3c7e7874b9770da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:26:10 GMT
ADD file:29a6559bb2b42840ad4a326cb87ec57e3d7acff070142d3c445e95a498608e9d in / 
# Wed, 17 Jun 2020 01:26:27 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:26:36 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:26:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:26:47 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:49:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:49:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b25075d60966612c3c64d57b4795ad61c96f1b6726b5f4e2bbe9895da022ab69`  
		Last Modified: Mon, 15 Jun 2020 15:49:24 GMT  
		Size: 32.8 MB (32831214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3ca039867a3a4d1f0bdce8cd95a4d5cae3bf26445e7da18368ea1a321552ef`  
		Last Modified: Wed, 17 Jun 2020 01:29:17 GMT  
		Size: 31.6 KB (31650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74cdff241e2c333351680e082de3609a7cbaaf2ad00a453b5b11f5d36990e02`  
		Last Modified: Wed, 17 Jun 2020 01:29:18 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9272e5603032808e3b694ab411de4202c12aa58e48b2e449ae98b88773a4684c`  
		Last Modified: Wed, 17 Jun 2020 01:29:18 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727bc1b8e91666a8974c3b58eec9076ddc3b3a8f1bf6fda0bedb6064373e2d70`  
		Last Modified: Wed, 17 Jun 2020 03:22:28 GMT  
		Size: 7.8 MB (7812013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed55ac2d20649312273a481dfa5a2c4d4577a25c3d297ac000ab717ccab6d14c`  
		Last Modified: Wed, 17 Jun 2020 03:22:25 GMT  
		Size: 4.4 MB (4447156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:97bf09371142ac49ebd6e095a37493e1501d957fa187a5f78d84509d4c7125f8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37051931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d0f249c37ecdc8b90ad04b1b3ad3651a419ec1a9fc61ceafe862416b0348b1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:22 GMT
ADD file:271767b03c56875ae656e017e3c7389388ad47f76199b62a9188f46587b7b8e4 in / 
# Wed, 17 Jun 2020 01:42:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:26 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:26 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:37:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:37:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ce848246baeb65370922009ba1a68f81697374faaccebca9d168de1b299f5a96`  
		Last Modified: Mon, 15 Jun 2020 15:49:42 GMT  
		Size: 26.9 MB (26892779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54205417978121761bc6d0aeb87a054c9299a29ebd368915b2487a4e0fcfef9`  
		Last Modified: Wed, 17 Jun 2020 01:43:26 GMT  
		Size: 32.5 KB (32481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a19a2a15c4483fbd611d89807936673906424b87bebf0fe9779e52501a6e8e`  
		Last Modified: Wed, 17 Jun 2020 01:43:27 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd67384e75b503499b1230515e4344c34ca7b8874e1c4434ca9c7c8aaf182a88`  
		Last Modified: Wed, 17 Jun 2020 01:43:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40490d592a8cd1f58b74c5ab9479b0f5996fce82c1a8ebad3df5fb56c0e7f4e0`  
		Last Modified: Wed, 17 Jun 2020 02:55:55 GMT  
		Size: 6.5 MB (6545783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7d09e6bfb23a33201aa2de56373348cb15af99961b8ac6fbf3b572010b958e`  
		Last Modified: Wed, 17 Jun 2020 02:56:00 GMT  
		Size: 3.6 MB (3579853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
