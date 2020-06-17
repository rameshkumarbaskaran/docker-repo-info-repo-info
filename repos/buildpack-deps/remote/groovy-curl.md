## `buildpack-deps:groovy-curl`

```console
$ docker pull buildpack-deps@sha256:9d8b7cfc61c6cbc2445c4c68f06f3bc87132fdb65d23b599108f99ca45b8701e
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
$ docker pull buildpack-deps@sha256:24d3073c536f9e42359d99ac30b88794dc1c141e218ab4166bf8e26433651d42
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45377966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c79a1786c5cb84e30035d6066a19111d0c70045231980ae715882fa333186de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 06 May 2020 18:53:34 GMT
ADD file:38bef3b89ab78f35a240c77d3bfd2424cfe83a3bf6c80a86755d0757378faac3 in / 
# Wed, 06 May 2020 18:53:42 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 06 May 2020 18:53:46 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 06 May 2020 18:53:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 06 May 2020 18:53:53 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2020 18:20:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 11 May 2020 18:20:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d4b677207667f6a9c31fb95628b1688e43185c1e68507b8ce69c6f753fa6ba0b`  
		Last Modified: Wed, 06 May 2020 18:55:08 GMT  
		Size: 32.8 MB (32830571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a7e3233f42ddeee42ce7307c2f23c2e22479c24ac6391bebc3673d1acedd3e`  
		Last Modified: Wed, 06 May 2020 18:55:01 GMT  
		Size: 31.6 KB (31614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f21b6f278fbf61dc1503c0ae1118b76024acb128bddbbd2588268e7b0649f91`  
		Last Modified: Wed, 06 May 2020 18:55:01 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a08354d087a0cd2da0584d4775ad4cd0dc224a90d08ba7bdb69f3617e83688e`  
		Last Modified: Wed, 06 May 2020 18:55:01 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9641d94e47a948c31373f5d11e71cf0507deb3964f344b8bdb7f49293f8aeb`  
		Last Modified: Mon, 11 May 2020 18:33:19 GMT  
		Size: 7.8 MB (7813663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1a3e6208b1cfd7270677514d1f2db85afab8cf34dfb830c72dd011bd388c59`  
		Last Modified: Mon, 11 May 2020 18:33:18 GMT  
		Size: 4.7 MB (4701080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:38c0eaf9a65cabb40de9d4377ae20bd572f645d7c3ba4b2b2474f74d91c37aad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37273783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44615101589dc8dac3044916659c690ed1577711006dd52b3bf621d21bd5e2e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 06 May 2020 19:11:33 GMT
ADD file:18b80c063e2b39052a6f2524611163983a5b6c8e1528240afb20fc3b41886101 in / 
# Wed, 06 May 2020 19:11:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 06 May 2020 19:11:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 06 May 2020 19:11:40 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 06 May 2020 19:11:41 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2020 18:43:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 11 May 2020 18:44:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8ed64b725cc4ff032cc93a2ea3abdb156d4ad0bd348733dd539bad2cac6bbed4`  
		Last Modified: Wed, 06 May 2020 19:12:19 GMT  
		Size: 26.9 MB (26896707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c313a26839bd4356dfd3e27dbe2c5a6987cabd276b1be0796a0a4f11ee03f`  
		Last Modified: Wed, 06 May 2020 19:12:16 GMT  
		Size: 32.5 KB (32456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80258349596dcffe60b09a96aa544fb2e8e215f2bf5f84b131d5a9be69df01e8`  
		Last Modified: Wed, 06 May 2020 19:12:21 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a213a1263d4ddd1b0655fdd29fbcd9a8bbe45007f72b6e9b37a3b0e770423cdf`  
		Last Modified: Wed, 06 May 2020 19:12:16 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e0df22201c8478d4407b1096292794871599aa21ad630b45d6ede37b0dae4e`  
		Last Modified: Mon, 11 May 2020 18:47:41 GMT  
		Size: 6.5 MB (6548064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cdd7894b14e9dee6298a895f30b09c83ce10efb5bf2ef94966eee2b9d495a0`  
		Last Modified: Mon, 11 May 2020 18:47:41 GMT  
		Size: 3.8 MB (3795522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
