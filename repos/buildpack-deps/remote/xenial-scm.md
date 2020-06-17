## `buildpack-deps:xenial-scm`

```console
$ docker pull buildpack-deps@sha256:ffc78b050ff0144d7d61e3b2f209f7a4d7a2d7a41a87f1b5fd70cd255076e40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:xenial-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2a76b6cd05cfe03d3c6618b5485cc29379aa2bd3eba6800e16d39916a9e0132c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93461154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755c96f0983899d522c26a70dfabb608b48254d51c7edde8eb03ab5d59faedd4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:26 GMT
ADD file:52af30f80ba214985a59cb0ef7073c64f8514d58396c0de48f8d7056dec2a58a in / 
# Wed, 17 Jun 2020 01:21:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:09:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:09:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Jun 2020 02:09:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b5e173e44934e01d8d2674bc8b1da00f761c4fe796e0fb2bee1bd1129d2e4ae1`  
		Last Modified: Fri, 15 May 2020 13:20:22 GMT  
		Size: 44.3 MB (44320272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29047100b0407dff554ea80b8005380d62b13a66d7fe2e2adb07b9c091b9f2c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 531.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15743a713c2a4033877dab08fb3989280f8c856234227158a4011811c7991372`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc9e2987763aa991b7dfd742be04c7b3bb04448982ffe88e58d55c93b76d4`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28f4fbc8f95e6f96e8ebaf99fc8370a6bf2d69a5aaad0605ca75d6b2055c987`  
		Last Modified: Wed, 17 Jun 2020 02:16:22 GMT  
		Size: 7.3 MB (7285591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23f039efba1163dafa71c8704a849420d9808a064a1815467ca7e85e3fb1979`  
		Last Modified: Wed, 17 Jun 2020 02:16:42 GMT  
		Size: 41.9 MB (41853735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:236f02d57c4c1df1513571f55484beb78fcde8327d49209d1f65fdf48942eb89
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83219970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64f23c3b7bd2cd42d3075f6f001a75f8071ab9b45696f9886faa1e82448be35`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 02:04:31 GMT
ADD file:6cc12f5b0908f30b9097dd8947a769888e2fed5c2a25671d1e4cd93ac0ef7a2a in / 
# Wed, 17 Jun 2020 02:04:43 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:04:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 02:05:08 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 02:05:12 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:43:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:43:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Jun 2020 02:44:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:964b1ad4ea33c6edf524b0fba723b83aa90e37a66419cf5e514392304bd73309`  
		Last Modified: Mon, 18 May 2020 15:50:57 GMT  
		Size: 39.0 MB (38964390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b1c0566b01f5b9247bdf23fee3adfd14071d248058523063939ce8c482863c`  
		Last Modified: Wed, 17 Jun 2020 02:05:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5534a4581c7bc4061f7f3c35130d6daa15345f5791fe5c4c90cbe06def252991`  
		Last Modified: Wed, 17 Jun 2020 02:05:53 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0db3772af551e10afa4bced33b87cf3a0716943e901e4a9da41b1caac84b55`  
		Last Modified: Wed, 17 Jun 2020 02:05:53 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b278ad964fd160d99e9ddc624867de7dd1928e6d1b2d57e8761791c5d511d77`  
		Last Modified: Wed, 17 Jun 2020 02:50:28 GMT  
		Size: 6.1 MB (6134556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73aba4c7bcfea301c64ff05056717924ba949b8be3f7b95752b2113fc114e01d`  
		Last Modified: Wed, 17 Jun 2020 02:50:46 GMT  
		Size: 38.1 MB (38119497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8e61c775f98388286ec33e0baa2b027490a6b2a7a760e74fcc7a2e389db6cba9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86114067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9063ece1849f5bce96015b20aea7aea1f98a05005cdc68d9037ec57f905373`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:44:20 GMT
ADD file:e359a3b06531f763adba716802e252fa49b2e6126f0d3dae1451fc94f5617a13 in / 
# Wed, 17 Jun 2020 01:44:24 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:44:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:44:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:44:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:29:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:29:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Jun 2020 02:30:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:13340090a20bfb81868e7119dc439546fe30dcfccce42509f0fb4d998a1d1fee`  
		Last Modified: Fri, 15 May 2020 16:25:35 GMT  
		Size: 40.0 MB (40003935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eea8c54eb3d5e45521f4ba5c57ede8436f58690cb8a37da90cfcda5efc25f7`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857f69e728f2821d6dce88bd1c73ebda9481628a80b563e677ec423b08fdba87`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b20459bfc0dfbc19d643cff0a457a117336e167bb8051554fb88aee48feff`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719c4f98cdfa1b94b180a6679d163ca4158b94cd0c07c451bd37677caba1afdf`  
		Last Modified: Wed, 17 Jun 2020 02:39:05 GMT  
		Size: 6.3 MB (6342219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faca2a26651e7f79c9a6824295e208709872e18f3008867a9a75eef2aae92a0`  
		Last Modified: Wed, 17 Jun 2020 02:39:23 GMT  
		Size: 39.8 MB (39766418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7bffbaca1c6fd0e508e053cf3185aaf229dffccbb12249e7d72531450b0623ce
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94524063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0b98c7262fe7e99465bb6e463c1c1ffb5963f21daec3ca10e4f3af4196346b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:39:24 GMT
ADD file:59bc1e3c513e2a53f34d3c366fbd90221f9f66cc28580092ad98761704e297c2 in / 
# Wed, 17 Jun 2020 01:39:25 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:39:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:39:27 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:39:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:04:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:04:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Jun 2020 02:04:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:886386dac43ac74334fbfea18a9bdd374fea3c200e555719e76e3c8ab4a42b24`  
		Last Modified: Mon, 18 May 2020 15:50:47 GMT  
		Size: 44.3 MB (44256143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8e8acdf7169f36f991a88019ded1aa3b079e34a068e816f23b5cc36b39e45c`  
		Last Modified: Wed, 17 Jun 2020 01:40:03 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4082258b52ba5c66a1b6ffcc2d870f1bc91bf8d76a23f3bf77cf6fe1d77b91c6`  
		Last Modified: Wed, 17 Jun 2020 01:40:02 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede304431cec0498213d3a4a9c15ef75cf249e7c83825ba0c7ad3274308934ad`  
		Last Modified: Wed, 17 Jun 2020 01:40:03 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d91010a19dec56e92a1a1ffd0979a27787ae3c295a5ffdfdabb3fa082afdfa`  
		Last Modified: Wed, 17 Jun 2020 02:10:00 GMT  
		Size: 7.4 MB (7428894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10505779a333a17a44bf4070629094e08613dd9595322d00253f510dc92e1ac6`  
		Last Modified: Wed, 17 Jun 2020 02:10:17 GMT  
		Size: 42.8 MB (42837491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ac912332555d6b384e679d385de3eca537eae682cba4c17dd64d45d6b7b35b7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98478006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4579425655bb8747a630eb37d94603295f3481dddb38fddc3480c13df2fafec3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:27:13 GMT
ADD file:d522ca8cc867b1005aecf011d2ebce51b45c03f4a939ff6402b93677899b6deb in / 
# Wed, 17 Jun 2020 01:27:26 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:27:33 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:27:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:27:46 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:02:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:02:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Jun 2020 03:04:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e5edfd8804acbddee0cc3d44c618a9b6091d13eed1ee94389f0582dd6e1517f`  
		Last Modified: Mon, 18 May 2020 15:51:40 GMT  
		Size: 46.2 MB (46175202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f957dd8506a4f76ec7e46e59773faf6c8b06035c6efb16135ac9dd052c7c28ef`  
		Last Modified: Wed, 17 Jun 2020 01:29:40 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f405a18af8f06aed09d754b2dfa5895076d09ec15a74e48406cb51a11779e0`  
		Last Modified: Wed, 17 Jun 2020 01:29:39 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8467f4c0538fe8863f2b0ee45e8b91f6a89337b16dc34624ef60cce0c18675`  
		Last Modified: Wed, 17 Jun 2020 01:29:39 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecc9fab4fcbe297dfe3ff8a3f7fdacdf73972ee410e8ae9d95afb7022c517c8`  
		Last Modified: Wed, 17 Jun 2020 03:23:51 GMT  
		Size: 7.2 MB (7186073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e41a43ff9c6e8d676e6ee9834ad17d8aed83730138ae81467ac1327f822cef`  
		Last Modified: Wed, 17 Jun 2020 03:24:13 GMT  
		Size: 45.1 MB (45115225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:10b2ff0c3a374fb4632db05ea1a1d70e2eb19ae1825428660c27c73b516da856
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92551096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a9a00c3115c0d83f40deb773b844491abe32256a5147e4cf4d6c1e28bcc7d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:35 GMT
ADD file:10bdfc967b8d5968cd7b7364aa8e93b3c2516128d782e6ef85dbc4a7f83e4b7a in / 
# Wed, 17 Jun 2020 01:42:38 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:42:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:39 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:40 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:43:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:43:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Jun 2020 02:46:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d0a0ed0c47429688bb895e35ebcd84f8b5bbd593eac2f0151603dd77dc50069e`  
		Last Modified: Mon, 18 May 2020 15:51:52 GMT  
		Size: 42.9 MB (42880585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81edf201d946558ead9d7e8425aec01524979f0532cb691919fe10d4dc3de238`  
		Last Modified: Wed, 17 Jun 2020 01:43:37 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141251eec5140d685bca36b9c230fd293ae4af1e90c04b66e7b2cf84bcea2010`  
		Last Modified: Wed, 17 Jun 2020 01:43:37 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4537a6d0859ba64cb05517eb056a0afb61ce29c65c43f9f8ddb388b4f6f75e90`  
		Last Modified: Wed, 17 Jun 2020 01:43:37 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6146265980b57663866b6f735db1d50b5990895e4a9ac4aaaeaf2d1c073a65b`  
		Last Modified: Wed, 17 Jun 2020 02:56:49 GMT  
		Size: 7.0 MB (7019632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bace58d8db98e3911e8528684bd985a8030979e549426ec91ff8bc7ecfa7878`  
		Last Modified: Wed, 17 Jun 2020 02:57:01 GMT  
		Size: 42.6 MB (42649393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
