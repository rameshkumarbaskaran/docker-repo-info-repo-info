## `buildpack-deps:groovy-scm`

```console
$ docker pull buildpack-deps@sha256:b31913c16346e60bbd13f1ccc22cb71319f2e8bb832f51d0da9622f6669c68fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:groovy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e7298b2a984443a537188f19c4a8bfd3270d8a9fe0d652f844ff8d078131d497
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100638049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c4765730f5812d8fc8b733b50b7d7ec02d5790aef30bc635edc22b1437ecba`
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
# Wed, 17 Jun 2020 02:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:5f9773c2692b253ed280140e56d8faa5519fd085cb20f576cc6e2c9d2987cb18`  
		Last Modified: Wed, 17 Jun 2020 02:15:42 GMT  
		Size: 62.0 MB (61990664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5b90d1e108df2bc6fa25e4a24352b0cd3c266d02a79d56bcf000b315c8c342c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99193383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f64439559de9a44da475db4ac814c608845936fad437eac33e0ea1af0c47ee`
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
# Wed, 17 Jun 2020 02:26:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:0cd45f17062a5035e4d4b1a2453e85b8409d78d72fcbb7485c3960c112140f52`  
		Last Modified: Wed, 17 Jun 2020 02:38:15 GMT  
		Size: 62.1 MB (62090773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4df19e61851bf20f3ae0b1742e2ebc583ae49318130c08d8df7ff46c7dd470ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117305836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8a76444ecb1c09d72b93c1310300375afb472c262f7dbca2d1fe9064bfa871`
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
# Mon, 11 May 2020 18:24:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:22253cdb40902ecc0b1f5770fd187606bf265971c911aa33a44804223204708f`  
		Last Modified: Mon, 11 May 2020 18:34:41 GMT  
		Size: 71.9 MB (71927870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5950d372ec5d55efae469f921b4bc2f40ae5b678e270553ee47f0f42a5e9ddc7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (100035298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8b2bdadb296213576ae19b9f66baf91919abd213123feb51907b3b2b8127f8`
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
# Mon, 11 May 2020 18:45:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:253d089777b2e8e500acc9b4f9c4149b4a50a57fe8c80bf3017844af7d5b8031`  
		Last Modified: Mon, 11 May 2020 18:47:56 GMT  
		Size: 62.8 MB (62761515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
