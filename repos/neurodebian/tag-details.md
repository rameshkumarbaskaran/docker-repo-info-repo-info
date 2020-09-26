<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bionic`](#neurodebianbionic)
-	[`neurodebian:bionic-non-free`](#neurodebianbionic-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:buster`](#neurodebianbuster)
-	[`neurodebian:buster-non-free`](#neurodebianbuster-non-free)
-	[`neurodebian:focal`](#neurodebianfocal)
-	[`neurodebian:focal-non-free`](#neurodebianfocal-non-free)
-	[`neurodebian:jessie`](#neurodebianjessie)
-	[`neurodebian:jessie-non-free`](#neurodebianjessie-non-free)
-	[`neurodebian:latest`](#neurodebianlatest)
-	[`neurodebian:nd`](#neurodebiannd)
-	[`neurodebian:nd100`](#neurodebiannd100)
-	[`neurodebian:nd100-non-free`](#neurodebiannd100-non-free)
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd14.04`](#neurodebiannd1404)
-	[`neurodebian:nd14.04-non-free`](#neurodebiannd1404-non-free)
-	[`neurodebian:nd16.04`](#neurodebiannd1604)
-	[`neurodebian:nd16.04-non-free`](#neurodebiannd1604-non-free)
-	[`neurodebian:nd18.04`](#neurodebiannd1804)
-	[`neurodebian:nd18.04-non-free`](#neurodebiannd1804-non-free)
-	[`neurodebian:nd20.04`](#neurodebiannd2004)
-	[`neurodebian:nd20.04-non-free`](#neurodebiannd2004-non-free)
-	[`neurodebian:nd80`](#neurodebiannd80)
-	[`neurodebian:nd80-non-free`](#neurodebiannd80-non-free)
-	[`neurodebian:nd90`](#neurodebiannd90)
-	[`neurodebian:nd90-non-free`](#neurodebiannd90-non-free)
-	[`neurodebian:nd-non-free`](#neurodebiannd-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)
-	[`neurodebian:sid`](#neurodebiansid)
-	[`neurodebian:sid-non-free`](#neurodebiansid-non-free)
-	[`neurodebian:stretch`](#neurodebianstretch)
-	[`neurodebian:stretch-non-free`](#neurodebianstretch-non-free)
-	[`neurodebian:trusty`](#neurodebiantrusty)
-	[`neurodebian:trusty-non-free`](#neurodebiantrusty-non-free)
-	[`neurodebian:xenial`](#neurodebianxenial)
-	[`neurodebian:xenial-non-free`](#neurodebianxenial-non-free)

## `neurodebian:bionic`

```console
$ docker pull neurodebian@sha256:85acd966296883289faa1839bb6b1adcd1d3d9726fff79dc3b8d466286a5dd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bionic` - linux; amd64

```console
$ docker pull neurodebian@sha256:0d977a7a5f8a222df7ce2d4a887d29c7c68cc242f49483ec5d02eaf6c26720a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31757684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49576f7ce5a19425020ce1954ca006500b51ce2f173ef31cbe54fee42c1efa10`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 01:07:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:07:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 26 Sep 2020 01:07:34 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 26 Sep 2020 01:07:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50c53e2a25ca3792036286aabb87dd1678477b8bd30341a6873f21a97c592e6`  
		Last Modified: Sat, 26 Sep 2020 01:09:23 GMT  
		Size: 4.8 MB (4811597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ae9df2b02bdd2590f906c5622c6779321a3f4725ea6e6d692ef162adebd00a`  
		Last Modified: Sat, 26 Sep 2020 01:09:22 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db7991c7027cd67f18dd0dfad7c8bafd3bee6580c907ed40c5f242df1de4fd5`  
		Last Modified: Sat, 26 Sep 2020 01:09:22 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176f1326428a403b8ba0a877d8feb71c57f0705debe0a1841df6a7db25957659`  
		Last Modified: Sat, 26 Sep 2020 01:09:22 GMT  
		Size: 240.1 KB (240071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bionic-non-free`

```console
$ docker pull neurodebian@sha256:ebe1c2ba1b4864991a4135797ec1610c577d6acf86c5933ff2ba2abee62e3e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bionic-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b99c25965b7d29db2ce061e781e87b7579ecc9b8ddedce2988978a27981d878f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31757941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b697f9ce94a66c4b456b622e06165d9b3bdced3934c2b8945fe1f2bb15f283`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 01:07:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:07:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 26 Sep 2020 01:07:34 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 26 Sep 2020 01:07:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:07:45 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50c53e2a25ca3792036286aabb87dd1678477b8bd30341a6873f21a97c592e6`  
		Last Modified: Sat, 26 Sep 2020 01:09:23 GMT  
		Size: 4.8 MB (4811597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ae9df2b02bdd2590f906c5622c6779321a3f4725ea6e6d692ef162adebd00a`  
		Last Modified: Sat, 26 Sep 2020 01:09:22 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db7991c7027cd67f18dd0dfad7c8bafd3bee6580c907ed40c5f242df1de4fd5`  
		Last Modified: Sat, 26 Sep 2020 01:09:22 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176f1326428a403b8ba0a877d8feb71c57f0705debe0a1841df6a7db25957659`  
		Last Modified: Sat, 26 Sep 2020 01:09:22 GMT  
		Size: 240.1 KB (240071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2ddfde3dca6410d3608c0613df2e294049195067d0599821f8881760e220e9`  
		Last Modified: Sat, 26 Sep 2020 01:09:26 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:75c5dcaac96b692d06c45735287a123382ecd92ccfc8b30d9ba92a546e6f6b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:c2e9fedd5e7fdefbf69374f36f8aa63d478361419b20435e5bced8fa3814ad73
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63255428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e3fac3b197d0ae834a46bd4a4330a52b8c0f45e370a47ff1c4927fa84179c9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:20:54 GMT
ADD file:375c01cd4aba0ddf77202decfeed5df5e3119ce460fcbf1f3b47f540a70b3864 in / 
# Thu, 10 Sep 2020 00:20:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:30:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:30:38 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:30:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:08d7334100fee80149028a0d0df44589b68e0c31592157808d18b68e6a572fd3`  
		Last Modified: Thu, 10 Sep 2020 00:33:04 GMT  
		Size: 51.9 MB (51906528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097e1f2a4104cccb08e4ebb1070cb616cc8236ceb3bef30386232738027c8d1`  
		Last Modified: Thu, 10 Sep 2020 12:32:14 GMT  
		Size: 11.0 MB (11048112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df42e5e80b44094569cd2182335dd6836096e2b59a73bbc60f2a8954a839076d`  
		Last Modified: Thu, 10 Sep 2020 12:32:12 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426ea32ef57970562a16018ae9eb5ca81d1ae43c4b53dc1070d3fbc96b2be4c3`  
		Last Modified: Thu, 10 Sep 2020 12:32:12 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a541b17e9df3c1774a284d312af41f23d684cbe13dc3c10c111e93cab815d73`  
		Last Modified: Thu, 10 Sep 2020 12:32:12 GMT  
		Size: 298.8 KB (298777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:b1b981ecb89928db19bcbdc993aec4d1c3401b98137b8cd41f5b89e330dc079a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:640e3df9e4534d11a9a3ddb222692cbf072d8a3f5824aa24a701299db25035b9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63255795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2fc6426dc97948ce484f6edd20201687eeb6e7a4cedf32fc36aacd6c8cfcbf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:20:54 GMT
ADD file:375c01cd4aba0ddf77202decfeed5df5e3119ce460fcbf1f3b47f540a70b3864 in / 
# Thu, 10 Sep 2020 00:20:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:30:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:30:38 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:30:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:48 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:08d7334100fee80149028a0d0df44589b68e0c31592157808d18b68e6a572fd3`  
		Last Modified: Thu, 10 Sep 2020 00:33:04 GMT  
		Size: 51.9 MB (51906528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097e1f2a4104cccb08e4ebb1070cb616cc8236ceb3bef30386232738027c8d1`  
		Last Modified: Thu, 10 Sep 2020 12:32:14 GMT  
		Size: 11.0 MB (11048112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df42e5e80b44094569cd2182335dd6836096e2b59a73bbc60f2a8954a839076d`  
		Last Modified: Thu, 10 Sep 2020 12:32:12 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426ea32ef57970562a16018ae9eb5ca81d1ae43c4b53dc1070d3fbc96b2be4c3`  
		Last Modified: Thu, 10 Sep 2020 12:32:12 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a541b17e9df3c1774a284d312af41f23d684cbe13dc3c10c111e93cab815d73`  
		Last Modified: Thu, 10 Sep 2020 12:32:12 GMT  
		Size: 298.8 KB (298777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28c8493a6fba4e132eddeabb99fb6827fbe71e39be45fa65694c2e77f381144`  
		Last Modified: Thu, 10 Sep 2020 12:32:17 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:fbeadbc84c0d933d0c7d4165684b90a02d4cccae0f4a7370e7aad4be1e861b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:836a5fbff762c5e1a6d7381372eef851aafd9f5fcf515b1fa3fdda5baa6b3fc2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61197798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db91714a76db2bdef7cdbbb9dc061a96b05d176e9bc2e9f759bd7635ad405c7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:22:55 GMT
ADD file:07a6578d6f507bd9c51bdf4fe41402db5dcf3b9fdf51cd4315778c27da1add39 in / 
# Thu, 10 Sep 2020 00:22:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:30:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:30:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:30:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57df1a1f1ad841deaf50c8f662d77e93b4b17af776ed66148116607f9aceffa8`  
		Last Modified: Thu, 10 Sep 2020 00:33:42 GMT  
		Size: 50.4 MB (50395913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01055b20d07d59a424b183bd6dfbb2ec7a88dc0831e537dc89dcda9480d6e58`  
		Last Modified: Thu, 10 Sep 2020 12:31:59 GMT  
		Size: 10.5 MB (10497383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ee86778a6afcf27d72ed312b2bc7aff2407328b679eace013e7db52c24257a`  
		Last Modified: Thu, 10 Sep 2020 12:31:57 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545f8b6fa1a1cef490b9634419d25e2d9485df08590dddc719c6122b511a9984`  
		Last Modified: Thu, 10 Sep 2020 12:31:57 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2688e3d25dddfb63592b78855f80db9183ced870d79f4c73dc10b1305dd24b`  
		Last Modified: Thu, 10 Sep 2020 12:31:57 GMT  
		Size: 302.5 KB (302494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:8e4d0b4c133bfe0ab5324024e2ae502018166ce3df678938b8e02781e854760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:255ea9ef034d146944fb30a078897c5a7181664d08430d214e353a1ea959598e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61198164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9865397025821087d8bae10799e33d279e2f85a91a7b249f176a580ea2134b20`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:22:55 GMT
ADD file:07a6578d6f507bd9c51bdf4fe41402db5dcf3b9fdf51cd4315778c27da1add39 in / 
# Thu, 10 Sep 2020 00:22:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:30:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:30:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:30:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:25 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:57df1a1f1ad841deaf50c8f662d77e93b4b17af776ed66148116607f9aceffa8`  
		Last Modified: Thu, 10 Sep 2020 00:33:42 GMT  
		Size: 50.4 MB (50395913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01055b20d07d59a424b183bd6dfbb2ec7a88dc0831e537dc89dcda9480d6e58`  
		Last Modified: Thu, 10 Sep 2020 12:31:59 GMT  
		Size: 10.5 MB (10497383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ee86778a6afcf27d72ed312b2bc7aff2407328b679eace013e7db52c24257a`  
		Last Modified: Thu, 10 Sep 2020 12:31:57 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545f8b6fa1a1cef490b9634419d25e2d9485df08590dddc719c6122b511a9984`  
		Last Modified: Thu, 10 Sep 2020 12:31:57 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2688e3d25dddfb63592b78855f80db9183ced870d79f4c73dc10b1305dd24b`  
		Last Modified: Thu, 10 Sep 2020 12:31:57 GMT  
		Size: 302.5 KB (302494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c38865b12cd448a3fc6f7e8f349c096c84248cf5d63ebb69c0f058422a72dae`  
		Last Modified: Thu, 10 Sep 2020 12:32:08 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:7dee1ccf5300cf541d4594715ecbedfd2ca8d789a798198f46abce2297cf8a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:4408525687f0817511d391749397c9465a6f5ced05eb28b45b31ec053060d49c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34286348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ca12916bf31f0cb06a55d1fadd22531b55a8021477a514339caebe684ed7d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:34:27 GMT
ADD file:da80f59399481ffc32f84353830dcf598f31a97785222e75d643bfb8a9aa14e7 in / 
# Fri, 25 Sep 2020 22:34:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:34:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:34:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:34:30 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 01:07:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:07:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 26 Sep 2020 01:07:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 26 Sep 2020 01:08:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d72e567cc804d0b637182ba23f8b9ffe101e753a39bf52cd4db6b89eb089f13b`  
		Last Modified: Fri, 25 Sep 2020 15:20:50 GMT  
		Size: 28.6 MB (28558050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3630e5ff08d73b6ec0e22736a5c8d2d666e7b568c16f6a4ffadf8c21b9b1ad`  
		Last Modified: Fri, 25 Sep 2020 22:36:58 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a83d81d1f4f942d37e1f17195d9c519969ed3040fc3e444740b884e44dec33`  
		Last Modified: Fri, 25 Sep 2020 22:36:58 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e20467b6488121d1149180452e041eed77018b499d0a78f653b8a9d19c3c6b6`  
		Last Modified: Sat, 26 Sep 2020 01:09:31 GMT  
		Size: 5.5 MB (5488504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6be1a2a3c814cb90954ec8a930eedd305776371558ebe85207b0befaf45b572`  
		Last Modified: Sat, 26 Sep 2020 01:09:30 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc7c9f67c83092316f2c1c2f398bdea68e6544ce12fc86880479258afb35d5c`  
		Last Modified: Sat, 26 Sep 2020 01:09:30 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875315ba91983585082ebec42caa3e65c9b6d3d9ab01d017e3fc39daf768b331`  
		Last Modified: Sat, 26 Sep 2020 01:09:30 GMT  
		Size: 236.8 KB (236783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:751599a9302f526314fc217c0b7ec6ab3dd3f7f9e720da27df63dec1248dafd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b8fc70b8841e66592bb4aa95fc07620a20c61a5c1d0d60947e2524be6eb6ad4b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34286605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946a91e5012c71216b7b1e2b24062a236b7c292c54413148489fc4522b262083`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:34:27 GMT
ADD file:da80f59399481ffc32f84353830dcf598f31a97785222e75d643bfb8a9aa14e7 in / 
# Fri, 25 Sep 2020 22:34:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:34:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:34:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:34:30 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 01:07:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:07:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 26 Sep 2020 01:07:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 26 Sep 2020 01:08:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:08:09 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:d72e567cc804d0b637182ba23f8b9ffe101e753a39bf52cd4db6b89eb089f13b`  
		Last Modified: Fri, 25 Sep 2020 15:20:50 GMT  
		Size: 28.6 MB (28558050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3630e5ff08d73b6ec0e22736a5c8d2d666e7b568c16f6a4ffadf8c21b9b1ad`  
		Last Modified: Fri, 25 Sep 2020 22:36:58 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a83d81d1f4f942d37e1f17195d9c519969ed3040fc3e444740b884e44dec33`  
		Last Modified: Fri, 25 Sep 2020 22:36:58 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e20467b6488121d1149180452e041eed77018b499d0a78f653b8a9d19c3c6b6`  
		Last Modified: Sat, 26 Sep 2020 01:09:31 GMT  
		Size: 5.5 MB (5488504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6be1a2a3c814cb90954ec8a930eedd305776371558ebe85207b0befaf45b572`  
		Last Modified: Sat, 26 Sep 2020 01:09:30 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc7c9f67c83092316f2c1c2f398bdea68e6544ce12fc86880479258afb35d5c`  
		Last Modified: Sat, 26 Sep 2020 01:09:30 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875315ba91983585082ebec42caa3e65c9b6d3d9ab01d017e3fc39daf768b331`  
		Last Modified: Sat, 26 Sep 2020 01:09:30 GMT  
		Size: 236.8 KB (236783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d7cfb97fc49a3d9b25ddce2381f8391e1905f878d90683d18d2580b48e8344`  
		Last Modified: Sat, 26 Sep 2020 01:09:34 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:jessie`

```console
$ docker pull neurodebian@sha256:3faaf9a3ccccbace6eee2bab84ad311885c1752ed818322b47189d5b0ea68c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:jessie` - linux; amd64

```console
$ docker pull neurodebian@sha256:1f044077a16842caa0c7d0b4878fce60654b1d15987c2503a127ce0b96d4fb62
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54694675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0dfb5c222e241ba49e7b0bd7034602278706b1ae3181eedae1802f37512d54`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:24:00 GMT
ADD file:ca64ef47722e4bf4beeab729a34cd854fe7293a0a2a0a2a92e6f1347c071dfe9 in / 
# Thu, 10 Sep 2020 00:24:01 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:26:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:27:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:27:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jessie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jessie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:29:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:290431e500161a90ac38ac8631791acb27e14a913613b60b3df58f839168df40`  
		Last Modified: Thu, 10 Sep 2020 00:34:21 GMT  
		Size: 54.4 MB (54389019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad4db44776143b9a026ac08b9bf9da391ec3f2f9f731ed6f5a7024581bc3501`  
		Last Modified: Thu, 10 Sep 2020 12:31:39 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb00c01d04704818d9fe732f2add0bc451e96528034b710ded6ad71d8f741793`  
		Last Modified: Thu, 10 Sep 2020 12:31:39 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9f5f67cb9bd973ba9564e4bae2483095e86db4967856fbd75a9f06439d36fb`  
		Last Modified: Thu, 10 Sep 2020 12:31:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae45c876b7e649386bce7a477d255b7bd6f538cdc1a87d619dd951940556a7c`  
		Last Modified: Thu, 10 Sep 2020 12:31:40 GMT  
		Size: 302.0 KB (301967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:jessie-non-free`

```console
$ docker pull neurodebian@sha256:c078b71c5763bc7ee0446efd9713e09c3c2750dd428c309d365eaa5abfca9ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:jessie-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:92dfd20339f50b73c926687b3c6fd8a3e41c240ee1acf0e42c3ee50996dce093
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54695039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea3bb379527b23a190b882474d2119a1a46909fdf92a3d503a425b3339cdd18`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:24:00 GMT
ADD file:ca64ef47722e4bf4beeab729a34cd854fe7293a0a2a0a2a92e6f1347c071dfe9 in / 
# Thu, 10 Sep 2020 00:24:01 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:26:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:27:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:27:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jessie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jessie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:29:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:29:34 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:290431e500161a90ac38ac8631791acb27e14a913613b60b3df58f839168df40`  
		Last Modified: Thu, 10 Sep 2020 00:34:21 GMT  
		Size: 54.4 MB (54389019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad4db44776143b9a026ac08b9bf9da391ec3f2f9f731ed6f5a7024581bc3501`  
		Last Modified: Thu, 10 Sep 2020 12:31:39 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb00c01d04704818d9fe732f2add0bc451e96528034b710ded6ad71d8f741793`  
		Last Modified: Thu, 10 Sep 2020 12:31:39 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9f5f67cb9bd973ba9564e4bae2483095e86db4967856fbd75a9f06439d36fb`  
		Last Modified: Thu, 10 Sep 2020 12:31:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae45c876b7e649386bce7a477d255b7bd6f538cdc1a87d619dd951940556a7c`  
		Last Modified: Thu, 10 Sep 2020 12:31:40 GMT  
		Size: 302.0 KB (301967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffb82c82f0b941ccb4a8c4816a5bb175c47e4455f93f294b5a83b7fa5243118`  
		Last Modified: Thu, 10 Sep 2020 12:31:43 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:fbeadbc84c0d933d0c7d4165684b90a02d4cccae0f4a7370e7aad4be1e861b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:836a5fbff762c5e1a6d7381372eef851aafd9f5fcf515b1fa3fdda5baa6b3fc2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61197798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db91714a76db2bdef7cdbbb9dc061a96b05d176e9bc2e9f759bd7635ad405c7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:22:55 GMT
ADD file:07a6578d6f507bd9c51bdf4fe41402db5dcf3b9fdf51cd4315778c27da1add39 in / 
# Thu, 10 Sep 2020 00:22:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:30:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:30:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:30:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57df1a1f1ad841deaf50c8f662d77e93b4b17af776ed66148116607f9aceffa8`  
		Last Modified: Thu, 10 Sep 2020 00:33:42 GMT  
		Size: 50.4 MB (50395913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01055b20d07d59a424b183bd6dfbb2ec7a88dc0831e537dc89dcda9480d6e58`  
		Last Modified: Thu, 10 Sep 2020 12:31:59 GMT  
		Size: 10.5 MB (10497383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ee86778a6afcf27d72ed312b2bc7aff2407328b679eace013e7db52c24257a`  
		Last Modified: Thu, 10 Sep 2020 12:31:57 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545f8b6fa1a1cef490b9634419d25e2d9485df08590dddc719c6122b511a9984`  
		Last Modified: Thu, 10 Sep 2020 12:31:57 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2688e3d25dddfb63592b78855f80db9183ced870d79f4c73dc10b1305dd24b`  
		Last Modified: Thu, 10 Sep 2020 12:31:57 GMT  
		Size: 302.5 KB (302494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:2f70946306e8fbd31c98affc914b834e7902bfa32c2d66e23a0aedf833bd9080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:3e55621984d4a80ee9301a64ed80ba798ed26c8858baf4a292c196d7d8b3cc36
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63836878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427642ccc0b21f556c2caa2344b60d606ac0bfc41fa0f830ff2b8d6e7c5f391c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:28:02 GMT
ADD file:d09d72986a18210fc325abfbe18d3d35fef6de8ede47304410bea7528e5ab5e6 in / 
# Thu, 10 Sep 2020 00:28:02 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:31:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:31:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:31:02 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:31:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5da2bf34dd483faff62b98f29a31447619812af8afb0cdee07c188e866571393`  
		Last Modified: Thu, 10 Sep 2020 00:35:58 GMT  
		Size: 52.5 MB (52488092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4892cd45687a8a6ce479d5ed7baeba7f25872e2269bae55597a8d89a5a2789a3`  
		Last Modified: Thu, 10 Sep 2020 12:32:23 GMT  
		Size: 11.0 MB (11048048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a4eefd16cac44fe531009a5853e37995d9daf8922fe32da710c6a40e83dba2`  
		Last Modified: Thu, 10 Sep 2020 12:32:21 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d539dda8df2b6367d15d7441b7c8e85849646c793b8e0c67cb4db03e5dd7c781`  
		Last Modified: Thu, 10 Sep 2020 12:32:21 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad5f58fe39a0a8c59dc1b8bf17d41f71a4b7da57483daa2bcd9805979b96103`  
		Last Modified: Thu, 10 Sep 2020 12:32:21 GMT  
		Size: 298.7 KB (298739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100`

```console
$ docker pull neurodebian@sha256:fbeadbc84c0d933d0c7d4165684b90a02d4cccae0f4a7370e7aad4be1e861b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd100` - linux; amd64

```console
$ docker pull neurodebian@sha256:836a5fbff762c5e1a6d7381372eef851aafd9f5fcf515b1fa3fdda5baa6b3fc2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61197798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db91714a76db2bdef7cdbbb9dc061a96b05d176e9bc2e9f759bd7635ad405c7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:22:55 GMT
ADD file:07a6578d6f507bd9c51bdf4fe41402db5dcf3b9fdf51cd4315778c27da1add39 in / 
# Thu, 10 Sep 2020 00:22:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:30:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:30:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:30:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57df1a1f1ad841deaf50c8f662d77e93b4b17af776ed66148116607f9aceffa8`  
		Last Modified: Thu, 10 Sep 2020 00:33:42 GMT  
		Size: 50.4 MB (50395913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01055b20d07d59a424b183bd6dfbb2ec7a88dc0831e537dc89dcda9480d6e58`  
		Last Modified: Thu, 10 Sep 2020 12:31:59 GMT  
		Size: 10.5 MB (10497383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ee86778a6afcf27d72ed312b2bc7aff2407328b679eace013e7db52c24257a`  
		Last Modified: Thu, 10 Sep 2020 12:31:57 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545f8b6fa1a1cef490b9634419d25e2d9485df08590dddc719c6122b511a9984`  
		Last Modified: Thu, 10 Sep 2020 12:31:57 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2688e3d25dddfb63592b78855f80db9183ced870d79f4c73dc10b1305dd24b`  
		Last Modified: Thu, 10 Sep 2020 12:31:57 GMT  
		Size: 302.5 KB (302494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:8e4d0b4c133bfe0ab5324024e2ae502018166ce3df678938b8e02781e854760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:255ea9ef034d146944fb30a078897c5a7181664d08430d214e353a1ea959598e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61198164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9865397025821087d8bae10799e33d279e2f85a91a7b249f176a580ea2134b20`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:22:55 GMT
ADD file:07a6578d6f507bd9c51bdf4fe41402db5dcf3b9fdf51cd4315778c27da1add39 in / 
# Thu, 10 Sep 2020 00:22:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:30:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:30:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:30:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:25 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:57df1a1f1ad841deaf50c8f662d77e93b4b17af776ed66148116607f9aceffa8`  
		Last Modified: Thu, 10 Sep 2020 00:33:42 GMT  
		Size: 50.4 MB (50395913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01055b20d07d59a424b183bd6dfbb2ec7a88dc0831e537dc89dcda9480d6e58`  
		Last Modified: Thu, 10 Sep 2020 12:31:59 GMT  
		Size: 10.5 MB (10497383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ee86778a6afcf27d72ed312b2bc7aff2407328b679eace013e7db52c24257a`  
		Last Modified: Thu, 10 Sep 2020 12:31:57 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545f8b6fa1a1cef490b9634419d25e2d9485df08590dddc719c6122b511a9984`  
		Last Modified: Thu, 10 Sep 2020 12:31:57 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2688e3d25dddfb63592b78855f80db9183ced870d79f4c73dc10b1305dd24b`  
		Last Modified: Thu, 10 Sep 2020 12:31:57 GMT  
		Size: 302.5 KB (302494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c38865b12cd448a3fc6f7e8f349c096c84248cf5d63ebb69c0f058422a72dae`  
		Last Modified: Thu, 10 Sep 2020 12:32:08 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:75c5dcaac96b692d06c45735287a123382ecd92ccfc8b30d9ba92a546e6f6b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:c2e9fedd5e7fdefbf69374f36f8aa63d478361419b20435e5bced8fa3814ad73
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63255428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e3fac3b197d0ae834a46bd4a4330a52b8c0f45e370a47ff1c4927fa84179c9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:20:54 GMT
ADD file:375c01cd4aba0ddf77202decfeed5df5e3119ce460fcbf1f3b47f540a70b3864 in / 
# Thu, 10 Sep 2020 00:20:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:30:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:30:38 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:30:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:08d7334100fee80149028a0d0df44589b68e0c31592157808d18b68e6a572fd3`  
		Last Modified: Thu, 10 Sep 2020 00:33:04 GMT  
		Size: 51.9 MB (51906528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097e1f2a4104cccb08e4ebb1070cb616cc8236ceb3bef30386232738027c8d1`  
		Last Modified: Thu, 10 Sep 2020 12:32:14 GMT  
		Size: 11.0 MB (11048112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df42e5e80b44094569cd2182335dd6836096e2b59a73bbc60f2a8954a839076d`  
		Last Modified: Thu, 10 Sep 2020 12:32:12 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426ea32ef57970562a16018ae9eb5ca81d1ae43c4b53dc1070d3fbc96b2be4c3`  
		Last Modified: Thu, 10 Sep 2020 12:32:12 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a541b17e9df3c1774a284d312af41f23d684cbe13dc3c10c111e93cab815d73`  
		Last Modified: Thu, 10 Sep 2020 12:32:12 GMT  
		Size: 298.8 KB (298777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:b1b981ecb89928db19bcbdc993aec4d1c3401b98137b8cd41f5b89e330dc079a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:640e3df9e4534d11a9a3ddb222692cbf072d8a3f5824aa24a701299db25035b9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63255795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2fc6426dc97948ce484f6edd20201687eeb6e7a4cedf32fc36aacd6c8cfcbf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:20:54 GMT
ADD file:375c01cd4aba0ddf77202decfeed5df5e3119ce460fcbf1f3b47f540a70b3864 in / 
# Thu, 10 Sep 2020 00:20:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:30:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:30:38 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:30:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:48 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:08d7334100fee80149028a0d0df44589b68e0c31592157808d18b68e6a572fd3`  
		Last Modified: Thu, 10 Sep 2020 00:33:04 GMT  
		Size: 51.9 MB (51906528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097e1f2a4104cccb08e4ebb1070cb616cc8236ceb3bef30386232738027c8d1`  
		Last Modified: Thu, 10 Sep 2020 12:32:14 GMT  
		Size: 11.0 MB (11048112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df42e5e80b44094569cd2182335dd6836096e2b59a73bbc60f2a8954a839076d`  
		Last Modified: Thu, 10 Sep 2020 12:32:12 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426ea32ef57970562a16018ae9eb5ca81d1ae43c4b53dc1070d3fbc96b2be4c3`  
		Last Modified: Thu, 10 Sep 2020 12:32:12 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a541b17e9df3c1774a284d312af41f23d684cbe13dc3c10c111e93cab815d73`  
		Last Modified: Thu, 10 Sep 2020 12:32:12 GMT  
		Size: 298.8 KB (298777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28c8493a6fba4e132eddeabb99fb6827fbe71e39be45fa65694c2e77f381144`  
		Last Modified: Thu, 10 Sep 2020 12:32:17 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd14.04`

```console
$ docker pull neurodebian@sha256:61f75e4abeea8782e74192ec6ea67b2c16a0f00ef655d00d9354b87972ce4d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd14.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:7551c1062ab7b8567f2caad9797d2a8555a01b895e8c67f2d18936731d137e63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71469387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a08e59697a0190e47bbc5cb43d2a94dce470cc71a07584781f7390764239fcf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:23:42 GMT
ADD file:276b5d943a4d284f8a7b249176a31f93d95e852480c2b851de287e53ff622bba in / 
# Wed, 16 Sep 2020 22:21:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:21:53 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:21:54 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:21:54 GMT
CMD ["/bin/bash"]
# Wed, 16 Sep 2020 23:16:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:16:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Sep 2020 23:16:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trusty main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trusty main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Sep 2020 23:16:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e6e20c8e2e69fa5c3fcc310f419975cef5fbeb6f7f2fe1374071141281b6a06`  
		Last Modified: Wed, 18 Dec 2019 13:21:28 GMT  
		Size: 70.7 MB (70691577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95201152d9ff9544c4fb2487c9f8cebcce9d0d2119fd3cc5e77b894f7c03877a`  
		Last Modified: Wed, 16 Sep 2020 22:23:30 GMT  
		Size: 72.7 KB (72651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63a3b65493fda086d5cc1800f70f3fcca9fb1cc064166d937a790be6adf665`  
		Last Modified: Wed, 16 Sep 2020 22:23:30 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d64eb2f1e3414c5fc28cb24d1efecc2d82bc62063e1b88b69949b8a4a3beae8`  
		Last Modified: Wed, 16 Sep 2020 23:20:21 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4c1476ca5142782adc317345b5f7d56a1c410452e7aee53b6cbd2683c214e2`  
		Last Modified: Wed, 16 Sep 2020 23:20:20 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08226658b9502b30dfc714275ebc813b9b821fb4b36aa1e1abed711a8d8bd804`  
		Last Modified: Wed, 16 Sep 2020 23:20:20 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4afb1b4034a4c1ef533b6f60210084e2c72148a29c45a1e26809ba411eb60a6`  
		Last Modified: Wed, 16 Sep 2020 23:20:20 GMT  
		Size: 701.1 KB (701081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd14.04-non-free`

```console
$ docker pull neurodebian@sha256:95b106bc5f638258496d7d3dd05c27694ac434516cf210962d3a91f86a77fb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd14.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:20747ce188a9599ff190d97def9d912f4ea0f8a53d2c0155deff872e5254aa8a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71469644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02ebe7ca19515137aeb15e450443ef3abd4ec1f6023d32aa3904960aa2842bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:23:42 GMT
ADD file:276b5d943a4d284f8a7b249176a31f93d95e852480c2b851de287e53ff622bba in / 
# Wed, 16 Sep 2020 22:21:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:21:53 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:21:54 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:21:54 GMT
CMD ["/bin/bash"]
# Wed, 16 Sep 2020 23:16:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:16:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Sep 2020 23:16:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trusty main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trusty main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Sep 2020 23:16:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:17:05 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:2e6e20c8e2e69fa5c3fcc310f419975cef5fbeb6f7f2fe1374071141281b6a06`  
		Last Modified: Wed, 18 Dec 2019 13:21:28 GMT  
		Size: 70.7 MB (70691577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95201152d9ff9544c4fb2487c9f8cebcce9d0d2119fd3cc5e77b894f7c03877a`  
		Last Modified: Wed, 16 Sep 2020 22:23:30 GMT  
		Size: 72.7 KB (72651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63a3b65493fda086d5cc1800f70f3fcca9fb1cc064166d937a790be6adf665`  
		Last Modified: Wed, 16 Sep 2020 22:23:30 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d64eb2f1e3414c5fc28cb24d1efecc2d82bc62063e1b88b69949b8a4a3beae8`  
		Last Modified: Wed, 16 Sep 2020 23:20:21 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4c1476ca5142782adc317345b5f7d56a1c410452e7aee53b6cbd2683c214e2`  
		Last Modified: Wed, 16 Sep 2020 23:20:20 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08226658b9502b30dfc714275ebc813b9b821fb4b36aa1e1abed711a8d8bd804`  
		Last Modified: Wed, 16 Sep 2020 23:20:20 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4afb1b4034a4c1ef533b6f60210084e2c72148a29c45a1e26809ba411eb60a6`  
		Last Modified: Wed, 16 Sep 2020 23:20:20 GMT  
		Size: 701.1 KB (701081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5af9db306284fa1768d6c04aab7c4c6c0c9fa3039b26d95acdb2ed9de816b2`  
		Last Modified: Wed, 16 Sep 2020 23:20:24 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd16.04`

```console
$ docker pull neurodebian@sha256:5b1090209132b36ae2301d79fefc5ce261267f9af1bdec5cfaacf94f6759c7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd16.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:051ca58325f96ed9e60111b3a0f15b5906ef85dbddf3a7dbda7b25e95f4c1b14
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44748563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b15c254916cb61ef2cb10a91ef8395aecefa70e2040ddb18f1e57426c0b9264`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:36:27 GMT
ADD file:23a55d7e93b396e490b6d0893137e5c13e3e0a234e0feaea8b1cfd4079fb1882 in / 
# Fri, 25 Sep 2020 22:36:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:36:28 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 22:36:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:36:29 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 01:07:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:07:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 26 Sep 2020 01:07:06 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 26 Sep 2020 01:07:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f53fa4d2cf0e29c6a522433e0ac71a7ce0fdab158481052b2198b5518b83248`  
		Last Modified: Thu, 17 Sep 2020 13:19:58 GMT  
		Size: 44.5 MB (44517215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af7c939e38e8e3160fbbdcc26a32669529b962c79f7337df0a26bf0e9a76d59`  
		Last Modified: Fri, 25 Sep 2020 22:37:21 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903d0ffd64f6ca1355d2b2df702fc674f5663981dfd100fe4588fb390dd3382c`  
		Last Modified: Fri, 25 Sep 2020 22:37:21 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04feeed388b71fdca5cc3bce619d65a34f8a1a3e5b0ef03f8392d499970818eb`  
		Last Modified: Fri, 25 Sep 2020 22:37:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c515c4bbd57e5e060382435401656f8c75aeb4df3d35c05184742fb26b59afe`  
		Last Modified: Sat, 26 Sep 2020 01:09:10 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00844731137cb6a0c71ccda3cd3a38d73fb6a6b490e108d5d382f8aa1cbfd89e`  
		Last Modified: Sat, 26 Sep 2020 01:09:11 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5d9a7fdaab7fd68587b855c7f9fa89b54494976273fefcce9926b189b9f813`  
		Last Modified: Sat, 26 Sep 2020 01:09:10 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af001496b5497280afcb76671c6577ea2cbf1844db7dd662bc1ff4b8290af05`  
		Last Modified: Sat, 26 Sep 2020 01:09:10 GMT  
		Size: 226.2 KB (226231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd16.04-non-free`

```console
$ docker pull neurodebian@sha256:e4b04ae00e8cffa330e6a2f3aea5a3f70c550b809da5de905e71225e498b74db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd16.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:01f693ac267e5c4eab3a2cc62009d75604a5c4ea6865cd66b81d3faeb1143651
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44748819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03873e08f3e5d6802553cdfb8c6da0dc3b712a463dd6ee470403b54c6044d17d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:36:27 GMT
ADD file:23a55d7e93b396e490b6d0893137e5c13e3e0a234e0feaea8b1cfd4079fb1882 in / 
# Fri, 25 Sep 2020 22:36:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:36:28 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 22:36:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:36:29 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 01:07:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:07:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 26 Sep 2020 01:07:06 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 26 Sep 2020 01:07:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:07:19 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:4f53fa4d2cf0e29c6a522433e0ac71a7ce0fdab158481052b2198b5518b83248`  
		Last Modified: Thu, 17 Sep 2020 13:19:58 GMT  
		Size: 44.5 MB (44517215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af7c939e38e8e3160fbbdcc26a32669529b962c79f7337df0a26bf0e9a76d59`  
		Last Modified: Fri, 25 Sep 2020 22:37:21 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903d0ffd64f6ca1355d2b2df702fc674f5663981dfd100fe4588fb390dd3382c`  
		Last Modified: Fri, 25 Sep 2020 22:37:21 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04feeed388b71fdca5cc3bce619d65a34f8a1a3e5b0ef03f8392d499970818eb`  
		Last Modified: Fri, 25 Sep 2020 22:37:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c515c4bbd57e5e060382435401656f8c75aeb4df3d35c05184742fb26b59afe`  
		Last Modified: Sat, 26 Sep 2020 01:09:10 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00844731137cb6a0c71ccda3cd3a38d73fb6a6b490e108d5d382f8aa1cbfd89e`  
		Last Modified: Sat, 26 Sep 2020 01:09:11 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5d9a7fdaab7fd68587b855c7f9fa89b54494976273fefcce9926b189b9f813`  
		Last Modified: Sat, 26 Sep 2020 01:09:10 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af001496b5497280afcb76671c6577ea2cbf1844db7dd662bc1ff4b8290af05`  
		Last Modified: Sat, 26 Sep 2020 01:09:10 GMT  
		Size: 226.2 KB (226231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c600bfc3826fca35f18c4c9fa4ac03e8b61e388fc0e5c78985981576c3a582f`  
		Last Modified: Sat, 26 Sep 2020 01:09:19 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04`

```console
$ docker pull neurodebian@sha256:85acd966296883289faa1839bb6b1adcd1d3d9726fff79dc3b8d466286a5dd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd18.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:0d977a7a5f8a222df7ce2d4a887d29c7c68cc242f49483ec5d02eaf6c26720a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31757684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49576f7ce5a19425020ce1954ca006500b51ce2f173ef31cbe54fee42c1efa10`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 01:07:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:07:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 26 Sep 2020 01:07:34 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 26 Sep 2020 01:07:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50c53e2a25ca3792036286aabb87dd1678477b8bd30341a6873f21a97c592e6`  
		Last Modified: Sat, 26 Sep 2020 01:09:23 GMT  
		Size: 4.8 MB (4811597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ae9df2b02bdd2590f906c5622c6779321a3f4725ea6e6d692ef162adebd00a`  
		Last Modified: Sat, 26 Sep 2020 01:09:22 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db7991c7027cd67f18dd0dfad7c8bafd3bee6580c907ed40c5f242df1de4fd5`  
		Last Modified: Sat, 26 Sep 2020 01:09:22 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176f1326428a403b8ba0a877d8feb71c57f0705debe0a1841df6a7db25957659`  
		Last Modified: Sat, 26 Sep 2020 01:09:22 GMT  
		Size: 240.1 KB (240071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04-non-free`

```console
$ docker pull neurodebian@sha256:ebe1c2ba1b4864991a4135797ec1610c577d6acf86c5933ff2ba2abee62e3e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd18.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b99c25965b7d29db2ce061e781e87b7579ecc9b8ddedce2988978a27981d878f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31757941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b697f9ce94a66c4b456b622e06165d9b3bdced3934c2b8945fe1f2bb15f283`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 01:07:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:07:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 26 Sep 2020 01:07:34 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 26 Sep 2020 01:07:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:07:45 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50c53e2a25ca3792036286aabb87dd1678477b8bd30341a6873f21a97c592e6`  
		Last Modified: Sat, 26 Sep 2020 01:09:23 GMT  
		Size: 4.8 MB (4811597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ae9df2b02bdd2590f906c5622c6779321a3f4725ea6e6d692ef162adebd00a`  
		Last Modified: Sat, 26 Sep 2020 01:09:22 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db7991c7027cd67f18dd0dfad7c8bafd3bee6580c907ed40c5f242df1de4fd5`  
		Last Modified: Sat, 26 Sep 2020 01:09:22 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176f1326428a403b8ba0a877d8feb71c57f0705debe0a1841df6a7db25957659`  
		Last Modified: Sat, 26 Sep 2020 01:09:22 GMT  
		Size: 240.1 KB (240071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2ddfde3dca6410d3608c0613df2e294049195067d0599821f8881760e220e9`  
		Last Modified: Sat, 26 Sep 2020 01:09:26 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:7dee1ccf5300cf541d4594715ecbedfd2ca8d789a798198f46abce2297cf8a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:4408525687f0817511d391749397c9465a6f5ced05eb28b45b31ec053060d49c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34286348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ca12916bf31f0cb06a55d1fadd22531b55a8021477a514339caebe684ed7d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:34:27 GMT
ADD file:da80f59399481ffc32f84353830dcf598f31a97785222e75d643bfb8a9aa14e7 in / 
# Fri, 25 Sep 2020 22:34:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:34:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:34:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:34:30 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 01:07:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:07:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 26 Sep 2020 01:07:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 26 Sep 2020 01:08:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d72e567cc804d0b637182ba23f8b9ffe101e753a39bf52cd4db6b89eb089f13b`  
		Last Modified: Fri, 25 Sep 2020 15:20:50 GMT  
		Size: 28.6 MB (28558050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3630e5ff08d73b6ec0e22736a5c8d2d666e7b568c16f6a4ffadf8c21b9b1ad`  
		Last Modified: Fri, 25 Sep 2020 22:36:58 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a83d81d1f4f942d37e1f17195d9c519969ed3040fc3e444740b884e44dec33`  
		Last Modified: Fri, 25 Sep 2020 22:36:58 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e20467b6488121d1149180452e041eed77018b499d0a78f653b8a9d19c3c6b6`  
		Last Modified: Sat, 26 Sep 2020 01:09:31 GMT  
		Size: 5.5 MB (5488504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6be1a2a3c814cb90954ec8a930eedd305776371558ebe85207b0befaf45b572`  
		Last Modified: Sat, 26 Sep 2020 01:09:30 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc7c9f67c83092316f2c1c2f398bdea68e6544ce12fc86880479258afb35d5c`  
		Last Modified: Sat, 26 Sep 2020 01:09:30 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875315ba91983585082ebec42caa3e65c9b6d3d9ab01d017e3fc39daf768b331`  
		Last Modified: Sat, 26 Sep 2020 01:09:30 GMT  
		Size: 236.8 KB (236783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:751599a9302f526314fc217c0b7ec6ab3dd3f7f9e720da27df63dec1248dafd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b8fc70b8841e66592bb4aa95fc07620a20c61a5c1d0d60947e2524be6eb6ad4b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34286605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946a91e5012c71216b7b1e2b24062a236b7c292c54413148489fc4522b262083`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:34:27 GMT
ADD file:da80f59399481ffc32f84353830dcf598f31a97785222e75d643bfb8a9aa14e7 in / 
# Fri, 25 Sep 2020 22:34:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:34:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:34:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:34:30 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 01:07:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:07:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 26 Sep 2020 01:07:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 26 Sep 2020 01:08:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:08:09 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:d72e567cc804d0b637182ba23f8b9ffe101e753a39bf52cd4db6b89eb089f13b`  
		Last Modified: Fri, 25 Sep 2020 15:20:50 GMT  
		Size: 28.6 MB (28558050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3630e5ff08d73b6ec0e22736a5c8d2d666e7b568c16f6a4ffadf8c21b9b1ad`  
		Last Modified: Fri, 25 Sep 2020 22:36:58 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a83d81d1f4f942d37e1f17195d9c519969ed3040fc3e444740b884e44dec33`  
		Last Modified: Fri, 25 Sep 2020 22:36:58 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e20467b6488121d1149180452e041eed77018b499d0a78f653b8a9d19c3c6b6`  
		Last Modified: Sat, 26 Sep 2020 01:09:31 GMT  
		Size: 5.5 MB (5488504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6be1a2a3c814cb90954ec8a930eedd305776371558ebe85207b0befaf45b572`  
		Last Modified: Sat, 26 Sep 2020 01:09:30 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc7c9f67c83092316f2c1c2f398bdea68e6544ce12fc86880479258afb35d5c`  
		Last Modified: Sat, 26 Sep 2020 01:09:30 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875315ba91983585082ebec42caa3e65c9b6d3d9ab01d017e3fc39daf768b331`  
		Last Modified: Sat, 26 Sep 2020 01:09:30 GMT  
		Size: 236.8 KB (236783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d7cfb97fc49a3d9b25ddce2381f8391e1905f878d90683d18d2580b48e8344`  
		Last Modified: Sat, 26 Sep 2020 01:09:34 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd80`

```console
$ docker pull neurodebian@sha256:3faaf9a3ccccbace6eee2bab84ad311885c1752ed818322b47189d5b0ea68c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd80` - linux; amd64

```console
$ docker pull neurodebian@sha256:1f044077a16842caa0c7d0b4878fce60654b1d15987c2503a127ce0b96d4fb62
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54694675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0dfb5c222e241ba49e7b0bd7034602278706b1ae3181eedae1802f37512d54`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:24:00 GMT
ADD file:ca64ef47722e4bf4beeab729a34cd854fe7293a0a2a0a2a92e6f1347c071dfe9 in / 
# Thu, 10 Sep 2020 00:24:01 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:26:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:27:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:27:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jessie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jessie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:29:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:290431e500161a90ac38ac8631791acb27e14a913613b60b3df58f839168df40`  
		Last Modified: Thu, 10 Sep 2020 00:34:21 GMT  
		Size: 54.4 MB (54389019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad4db44776143b9a026ac08b9bf9da391ec3f2f9f731ed6f5a7024581bc3501`  
		Last Modified: Thu, 10 Sep 2020 12:31:39 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb00c01d04704818d9fe732f2add0bc451e96528034b710ded6ad71d8f741793`  
		Last Modified: Thu, 10 Sep 2020 12:31:39 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9f5f67cb9bd973ba9564e4bae2483095e86db4967856fbd75a9f06439d36fb`  
		Last Modified: Thu, 10 Sep 2020 12:31:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae45c876b7e649386bce7a477d255b7bd6f538cdc1a87d619dd951940556a7c`  
		Last Modified: Thu, 10 Sep 2020 12:31:40 GMT  
		Size: 302.0 KB (301967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd80-non-free`

```console
$ docker pull neurodebian@sha256:c078b71c5763bc7ee0446efd9713e09c3c2750dd428c309d365eaa5abfca9ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd80-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:92dfd20339f50b73c926687b3c6fd8a3e41c240ee1acf0e42c3ee50996dce093
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54695039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea3bb379527b23a190b882474d2119a1a46909fdf92a3d503a425b3339cdd18`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:24:00 GMT
ADD file:ca64ef47722e4bf4beeab729a34cd854fe7293a0a2a0a2a92e6f1347c071dfe9 in / 
# Thu, 10 Sep 2020 00:24:01 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:26:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:27:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:27:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jessie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jessie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:29:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:29:34 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:290431e500161a90ac38ac8631791acb27e14a913613b60b3df58f839168df40`  
		Last Modified: Thu, 10 Sep 2020 00:34:21 GMT  
		Size: 54.4 MB (54389019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad4db44776143b9a026ac08b9bf9da391ec3f2f9f731ed6f5a7024581bc3501`  
		Last Modified: Thu, 10 Sep 2020 12:31:39 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb00c01d04704818d9fe732f2add0bc451e96528034b710ded6ad71d8f741793`  
		Last Modified: Thu, 10 Sep 2020 12:31:39 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9f5f67cb9bd973ba9564e4bae2483095e86db4967856fbd75a9f06439d36fb`  
		Last Modified: Thu, 10 Sep 2020 12:31:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae45c876b7e649386bce7a477d255b7bd6f538cdc1a87d619dd951940556a7c`  
		Last Modified: Thu, 10 Sep 2020 12:31:40 GMT  
		Size: 302.0 KB (301967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffb82c82f0b941ccb4a8c4816a5bb175c47e4455f93f294b5a83b7fa5243118`  
		Last Modified: Thu, 10 Sep 2020 12:31:43 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd90`

```console
$ docker pull neurodebian@sha256:da56ec53c4c323b7e0263e1688b6d4cee39118cc4eb0a10d64bbe37de3eafd42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd90` - linux; amd64

```console
$ docker pull neurodebian@sha256:51608e23dbc6244fabac99b8a324e7937aadcaeb9e00650e1d7a76a31297e91b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52230768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943bd14b45e0b58857421e1dbbbf66eb53af637d70e8f3c537904bd83852121a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:29:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:29:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:29:49 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:29:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e820b59377bb61d09daa8ac34a9f3df25be48972003704bcb12e6e13a7f00009`  
		Last Modified: Thu, 10 Sep 2020 12:31:49 GMT  
		Size: 6.6 MB (6568552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bdb1d1978244c3811191c8254dd83e882436c19d036de00f8564404db24aa4`  
		Last Modified: Thu, 10 Sep 2020 12:31:48 GMT  
		Size: 3.2 KB (3154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a9d62565b438b5f15905601c72c67a69d1809d385530c74fdab53e8cc0db88`  
		Last Modified: Thu, 10 Sep 2020 12:31:48 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12442eb22cf1320c74e5fd16277cc2dce1ac630bbb80b8056d2a01847a8776f7`  
		Last Modified: Thu, 10 Sep 2020 12:31:48 GMT  
		Size: 292.1 KB (292093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd90-non-free`

```console
$ docker pull neurodebian@sha256:a40fba63307f3dc0b4d893d3a1cd4e63e6dedce10d39ee87a144c9f0f835929e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd90-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6fe795b37c83bc87e0bbab26feb801298af553a50cc884a9b33bebb26915ae02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52231134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af55ab4ccbc447fdfc620792e4b61eaf67c43795e5c448aa6e2c5f2bbf99c9c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:29:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:29:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:29:49 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:29:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:00 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e820b59377bb61d09daa8ac34a9f3df25be48972003704bcb12e6e13a7f00009`  
		Last Modified: Thu, 10 Sep 2020 12:31:49 GMT  
		Size: 6.6 MB (6568552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bdb1d1978244c3811191c8254dd83e882436c19d036de00f8564404db24aa4`  
		Last Modified: Thu, 10 Sep 2020 12:31:48 GMT  
		Size: 3.2 KB (3154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a9d62565b438b5f15905601c72c67a69d1809d385530c74fdab53e8cc0db88`  
		Last Modified: Thu, 10 Sep 2020 12:31:48 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12442eb22cf1320c74e5fd16277cc2dce1ac630bbb80b8056d2a01847a8776f7`  
		Last Modified: Thu, 10 Sep 2020 12:31:48 GMT  
		Size: 292.1 KB (292093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd4c3862e2ba86b98ac096657efa1bac320e289dffe4ef95a7267471b092815`  
		Last Modified: Thu, 10 Sep 2020 12:31:53 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:ed5ff94e0323eedaf05762e236245597f38a817521efdcdbb7df9ec408cbed33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b4f4b0c0964ad28188cff80b432a4f4cb5777995231c11af07289c52054a4b26
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63837196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9eb61ede6344ad1d599ba8c8c03a743ba050afe36f8a5d8adb674d4f9ba963b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:28:02 GMT
ADD file:d09d72986a18210fc325abfbe18d3d35fef6de8ede47304410bea7528e5ab5e6 in / 
# Thu, 10 Sep 2020 00:28:02 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:31:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:31:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:31:02 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:31:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:31:12 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:5da2bf34dd483faff62b98f29a31447619812af8afb0cdee07c188e866571393`  
		Last Modified: Thu, 10 Sep 2020 00:35:58 GMT  
		Size: 52.5 MB (52488092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4892cd45687a8a6ce479d5ed7baeba7f25872e2269bae55597a8d89a5a2789a3`  
		Last Modified: Thu, 10 Sep 2020 12:32:23 GMT  
		Size: 11.0 MB (11048048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a4eefd16cac44fe531009a5853e37995d9daf8922fe32da710c6a40e83dba2`  
		Last Modified: Thu, 10 Sep 2020 12:32:21 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d539dda8df2b6367d15d7441b7c8e85849646c793b8e0c67cb4db03e5dd7c781`  
		Last Modified: Thu, 10 Sep 2020 12:32:21 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad5f58fe39a0a8c59dc1b8bf17d41f71a4b7da57483daa2bcd9805979b96103`  
		Last Modified: Thu, 10 Sep 2020 12:32:21 GMT  
		Size: 298.7 KB (298739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6bdeaee5f394266f8545c56a12b233deeecf728b54f99ae287c1f257c1ea4b`  
		Last Modified: Thu, 10 Sep 2020 12:32:27 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:8e4d0b4c133bfe0ab5324024e2ae502018166ce3df678938b8e02781e854760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:255ea9ef034d146944fb30a078897c5a7181664d08430d214e353a1ea959598e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61198164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9865397025821087d8bae10799e33d279e2f85a91a7b249f176a580ea2134b20`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:22:55 GMT
ADD file:07a6578d6f507bd9c51bdf4fe41402db5dcf3b9fdf51cd4315778c27da1add39 in / 
# Thu, 10 Sep 2020 00:22:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:30:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:30:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:30:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:25 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:57df1a1f1ad841deaf50c8f662d77e93b4b17af776ed66148116607f9aceffa8`  
		Last Modified: Thu, 10 Sep 2020 00:33:42 GMT  
		Size: 50.4 MB (50395913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01055b20d07d59a424b183bd6dfbb2ec7a88dc0831e537dc89dcda9480d6e58`  
		Last Modified: Thu, 10 Sep 2020 12:31:59 GMT  
		Size: 10.5 MB (10497383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ee86778a6afcf27d72ed312b2bc7aff2407328b679eace013e7db52c24257a`  
		Last Modified: Thu, 10 Sep 2020 12:31:57 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545f8b6fa1a1cef490b9634419d25e2d9485df08590dddc719c6122b511a9984`  
		Last Modified: Thu, 10 Sep 2020 12:31:57 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2688e3d25dddfb63592b78855f80db9183ced870d79f4c73dc10b1305dd24b`  
		Last Modified: Thu, 10 Sep 2020 12:31:57 GMT  
		Size: 302.5 KB (302494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c38865b12cd448a3fc6f7e8f349c096c84248cf5d63ebb69c0f058422a72dae`  
		Last Modified: Thu, 10 Sep 2020 12:32:08 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:2f70946306e8fbd31c98affc914b834e7902bfa32c2d66e23a0aedf833bd9080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:3e55621984d4a80ee9301a64ed80ba798ed26c8858baf4a292c196d7d8b3cc36
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63836878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427642ccc0b21f556c2caa2344b60d606ac0bfc41fa0f830ff2b8d6e7c5f391c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:28:02 GMT
ADD file:d09d72986a18210fc325abfbe18d3d35fef6de8ede47304410bea7528e5ab5e6 in / 
# Thu, 10 Sep 2020 00:28:02 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:31:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:31:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:31:02 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:31:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5da2bf34dd483faff62b98f29a31447619812af8afb0cdee07c188e866571393`  
		Last Modified: Thu, 10 Sep 2020 00:35:58 GMT  
		Size: 52.5 MB (52488092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4892cd45687a8a6ce479d5ed7baeba7f25872e2269bae55597a8d89a5a2789a3`  
		Last Modified: Thu, 10 Sep 2020 12:32:23 GMT  
		Size: 11.0 MB (11048048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a4eefd16cac44fe531009a5853e37995d9daf8922fe32da710c6a40e83dba2`  
		Last Modified: Thu, 10 Sep 2020 12:32:21 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d539dda8df2b6367d15d7441b7c8e85849646c793b8e0c67cb4db03e5dd7c781`  
		Last Modified: Thu, 10 Sep 2020 12:32:21 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad5f58fe39a0a8c59dc1b8bf17d41f71a4b7da57483daa2bcd9805979b96103`  
		Last Modified: Thu, 10 Sep 2020 12:32:21 GMT  
		Size: 298.7 KB (298739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:ed5ff94e0323eedaf05762e236245597f38a817521efdcdbb7df9ec408cbed33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b4f4b0c0964ad28188cff80b432a4f4cb5777995231c11af07289c52054a4b26
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63837196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9eb61ede6344ad1d599ba8c8c03a743ba050afe36f8a5d8adb674d4f9ba963b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:28:02 GMT
ADD file:d09d72986a18210fc325abfbe18d3d35fef6de8ede47304410bea7528e5ab5e6 in / 
# Thu, 10 Sep 2020 00:28:02 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:31:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:31:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:31:02 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:31:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:31:12 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:5da2bf34dd483faff62b98f29a31447619812af8afb0cdee07c188e866571393`  
		Last Modified: Thu, 10 Sep 2020 00:35:58 GMT  
		Size: 52.5 MB (52488092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4892cd45687a8a6ce479d5ed7baeba7f25872e2269bae55597a8d89a5a2789a3`  
		Last Modified: Thu, 10 Sep 2020 12:32:23 GMT  
		Size: 11.0 MB (11048048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a4eefd16cac44fe531009a5853e37995d9daf8922fe32da710c6a40e83dba2`  
		Last Modified: Thu, 10 Sep 2020 12:32:21 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d539dda8df2b6367d15d7441b7c8e85849646c793b8e0c67cb4db03e5dd7c781`  
		Last Modified: Thu, 10 Sep 2020 12:32:21 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad5f58fe39a0a8c59dc1b8bf17d41f71a4b7da57483daa2bcd9805979b96103`  
		Last Modified: Thu, 10 Sep 2020 12:32:21 GMT  
		Size: 298.7 KB (298739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6bdeaee5f394266f8545c56a12b233deeecf728b54f99ae287c1f257c1ea4b`  
		Last Modified: Thu, 10 Sep 2020 12:32:27 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:stretch`

```console
$ docker pull neurodebian@sha256:da56ec53c4c323b7e0263e1688b6d4cee39118cc4eb0a10d64bbe37de3eafd42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:stretch` - linux; amd64

```console
$ docker pull neurodebian@sha256:51608e23dbc6244fabac99b8a324e7937aadcaeb9e00650e1d7a76a31297e91b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52230768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943bd14b45e0b58857421e1dbbbf66eb53af637d70e8f3c537904bd83852121a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:29:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:29:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:29:49 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:29:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e820b59377bb61d09daa8ac34a9f3df25be48972003704bcb12e6e13a7f00009`  
		Last Modified: Thu, 10 Sep 2020 12:31:49 GMT  
		Size: 6.6 MB (6568552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bdb1d1978244c3811191c8254dd83e882436c19d036de00f8564404db24aa4`  
		Last Modified: Thu, 10 Sep 2020 12:31:48 GMT  
		Size: 3.2 KB (3154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a9d62565b438b5f15905601c72c67a69d1809d385530c74fdab53e8cc0db88`  
		Last Modified: Thu, 10 Sep 2020 12:31:48 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12442eb22cf1320c74e5fd16277cc2dce1ac630bbb80b8056d2a01847a8776f7`  
		Last Modified: Thu, 10 Sep 2020 12:31:48 GMT  
		Size: 292.1 KB (292093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:stretch-non-free`

```console
$ docker pull neurodebian@sha256:a40fba63307f3dc0b4d893d3a1cd4e63e6dedce10d39ee87a144c9f0f835929e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:stretch-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6fe795b37c83bc87e0bbab26feb801298af553a50cc884a9b33bebb26915ae02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52231134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af55ab4ccbc447fdfc620792e4b61eaf67c43795e5c448aa6e2c5f2bbf99c9c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:29:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:29:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:29:49 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:29:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:00 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e820b59377bb61d09daa8ac34a9f3df25be48972003704bcb12e6e13a7f00009`  
		Last Modified: Thu, 10 Sep 2020 12:31:49 GMT  
		Size: 6.6 MB (6568552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bdb1d1978244c3811191c8254dd83e882436c19d036de00f8564404db24aa4`  
		Last Modified: Thu, 10 Sep 2020 12:31:48 GMT  
		Size: 3.2 KB (3154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a9d62565b438b5f15905601c72c67a69d1809d385530c74fdab53e8cc0db88`  
		Last Modified: Thu, 10 Sep 2020 12:31:48 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12442eb22cf1320c74e5fd16277cc2dce1ac630bbb80b8056d2a01847a8776f7`  
		Last Modified: Thu, 10 Sep 2020 12:31:48 GMT  
		Size: 292.1 KB (292093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd4c3862e2ba86b98ac096657efa1bac320e289dffe4ef95a7267471b092815`  
		Last Modified: Thu, 10 Sep 2020 12:31:53 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:trusty`

```console
$ docker pull neurodebian@sha256:61f75e4abeea8782e74192ec6ea67b2c16a0f00ef655d00d9354b87972ce4d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:trusty` - linux; amd64

```console
$ docker pull neurodebian@sha256:7551c1062ab7b8567f2caad9797d2a8555a01b895e8c67f2d18936731d137e63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71469387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a08e59697a0190e47bbc5cb43d2a94dce470cc71a07584781f7390764239fcf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:23:42 GMT
ADD file:276b5d943a4d284f8a7b249176a31f93d95e852480c2b851de287e53ff622bba in / 
# Wed, 16 Sep 2020 22:21:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:21:53 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:21:54 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:21:54 GMT
CMD ["/bin/bash"]
# Wed, 16 Sep 2020 23:16:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:16:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Sep 2020 23:16:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trusty main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trusty main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Sep 2020 23:16:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e6e20c8e2e69fa5c3fcc310f419975cef5fbeb6f7f2fe1374071141281b6a06`  
		Last Modified: Wed, 18 Dec 2019 13:21:28 GMT  
		Size: 70.7 MB (70691577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95201152d9ff9544c4fb2487c9f8cebcce9d0d2119fd3cc5e77b894f7c03877a`  
		Last Modified: Wed, 16 Sep 2020 22:23:30 GMT  
		Size: 72.7 KB (72651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63a3b65493fda086d5cc1800f70f3fcca9fb1cc064166d937a790be6adf665`  
		Last Modified: Wed, 16 Sep 2020 22:23:30 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d64eb2f1e3414c5fc28cb24d1efecc2d82bc62063e1b88b69949b8a4a3beae8`  
		Last Modified: Wed, 16 Sep 2020 23:20:21 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4c1476ca5142782adc317345b5f7d56a1c410452e7aee53b6cbd2683c214e2`  
		Last Modified: Wed, 16 Sep 2020 23:20:20 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08226658b9502b30dfc714275ebc813b9b821fb4b36aa1e1abed711a8d8bd804`  
		Last Modified: Wed, 16 Sep 2020 23:20:20 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4afb1b4034a4c1ef533b6f60210084e2c72148a29c45a1e26809ba411eb60a6`  
		Last Modified: Wed, 16 Sep 2020 23:20:20 GMT  
		Size: 701.1 KB (701081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:trusty-non-free`

```console
$ docker pull neurodebian@sha256:95b106bc5f638258496d7d3dd05c27694ac434516cf210962d3a91f86a77fb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:trusty-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:20747ce188a9599ff190d97def9d912f4ea0f8a53d2c0155deff872e5254aa8a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71469644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02ebe7ca19515137aeb15e450443ef3abd4ec1f6023d32aa3904960aa2842bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:23:42 GMT
ADD file:276b5d943a4d284f8a7b249176a31f93d95e852480c2b851de287e53ff622bba in / 
# Wed, 16 Sep 2020 22:21:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:21:53 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:21:54 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:21:54 GMT
CMD ["/bin/bash"]
# Wed, 16 Sep 2020 23:16:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:16:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Sep 2020 23:16:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trusty main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trusty main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Sep 2020 23:16:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:17:05 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:2e6e20c8e2e69fa5c3fcc310f419975cef5fbeb6f7f2fe1374071141281b6a06`  
		Last Modified: Wed, 18 Dec 2019 13:21:28 GMT  
		Size: 70.7 MB (70691577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95201152d9ff9544c4fb2487c9f8cebcce9d0d2119fd3cc5e77b894f7c03877a`  
		Last Modified: Wed, 16 Sep 2020 22:23:30 GMT  
		Size: 72.7 KB (72651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63a3b65493fda086d5cc1800f70f3fcca9fb1cc064166d937a790be6adf665`  
		Last Modified: Wed, 16 Sep 2020 22:23:30 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d64eb2f1e3414c5fc28cb24d1efecc2d82bc62063e1b88b69949b8a4a3beae8`  
		Last Modified: Wed, 16 Sep 2020 23:20:21 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4c1476ca5142782adc317345b5f7d56a1c410452e7aee53b6cbd2683c214e2`  
		Last Modified: Wed, 16 Sep 2020 23:20:20 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08226658b9502b30dfc714275ebc813b9b821fb4b36aa1e1abed711a8d8bd804`  
		Last Modified: Wed, 16 Sep 2020 23:20:20 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4afb1b4034a4c1ef533b6f60210084e2c72148a29c45a1e26809ba411eb60a6`  
		Last Modified: Wed, 16 Sep 2020 23:20:20 GMT  
		Size: 701.1 KB (701081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5af9db306284fa1768d6c04aab7c4c6c0c9fa3039b26d95acdb2ed9de816b2`  
		Last Modified: Wed, 16 Sep 2020 23:20:24 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:xenial`

```console
$ docker pull neurodebian@sha256:5b1090209132b36ae2301d79fefc5ce261267f9af1bdec5cfaacf94f6759c7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:xenial` - linux; amd64

```console
$ docker pull neurodebian@sha256:051ca58325f96ed9e60111b3a0f15b5906ef85dbddf3a7dbda7b25e95f4c1b14
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44748563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b15c254916cb61ef2cb10a91ef8395aecefa70e2040ddb18f1e57426c0b9264`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:36:27 GMT
ADD file:23a55d7e93b396e490b6d0893137e5c13e3e0a234e0feaea8b1cfd4079fb1882 in / 
# Fri, 25 Sep 2020 22:36:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:36:28 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 22:36:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:36:29 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 01:07:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:07:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 26 Sep 2020 01:07:06 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 26 Sep 2020 01:07:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f53fa4d2cf0e29c6a522433e0ac71a7ce0fdab158481052b2198b5518b83248`  
		Last Modified: Thu, 17 Sep 2020 13:19:58 GMT  
		Size: 44.5 MB (44517215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af7c939e38e8e3160fbbdcc26a32669529b962c79f7337df0a26bf0e9a76d59`  
		Last Modified: Fri, 25 Sep 2020 22:37:21 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903d0ffd64f6ca1355d2b2df702fc674f5663981dfd100fe4588fb390dd3382c`  
		Last Modified: Fri, 25 Sep 2020 22:37:21 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04feeed388b71fdca5cc3bce619d65a34f8a1a3e5b0ef03f8392d499970818eb`  
		Last Modified: Fri, 25 Sep 2020 22:37:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c515c4bbd57e5e060382435401656f8c75aeb4df3d35c05184742fb26b59afe`  
		Last Modified: Sat, 26 Sep 2020 01:09:10 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00844731137cb6a0c71ccda3cd3a38d73fb6a6b490e108d5d382f8aa1cbfd89e`  
		Last Modified: Sat, 26 Sep 2020 01:09:11 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5d9a7fdaab7fd68587b855c7f9fa89b54494976273fefcce9926b189b9f813`  
		Last Modified: Sat, 26 Sep 2020 01:09:10 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af001496b5497280afcb76671c6577ea2cbf1844db7dd662bc1ff4b8290af05`  
		Last Modified: Sat, 26 Sep 2020 01:09:10 GMT  
		Size: 226.2 KB (226231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:xenial-non-free`

```console
$ docker pull neurodebian@sha256:e4b04ae00e8cffa330e6a2f3aea5a3f70c550b809da5de905e71225e498b74db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:xenial-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:01f693ac267e5c4eab3a2cc62009d75604a5c4ea6865cd66b81d3faeb1143651
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44748819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03873e08f3e5d6802553cdfb8c6da0dc3b712a463dd6ee470403b54c6044d17d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:36:27 GMT
ADD file:23a55d7e93b396e490b6d0893137e5c13e3e0a234e0feaea8b1cfd4079fb1882 in / 
# Fri, 25 Sep 2020 22:36:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:36:28 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 22:36:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:36:29 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 01:07:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:07:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 26 Sep 2020 01:07:06 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 26 Sep 2020 01:07:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:07:19 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:4f53fa4d2cf0e29c6a522433e0ac71a7ce0fdab158481052b2198b5518b83248`  
		Last Modified: Thu, 17 Sep 2020 13:19:58 GMT  
		Size: 44.5 MB (44517215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af7c939e38e8e3160fbbdcc26a32669529b962c79f7337df0a26bf0e9a76d59`  
		Last Modified: Fri, 25 Sep 2020 22:37:21 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903d0ffd64f6ca1355d2b2df702fc674f5663981dfd100fe4588fb390dd3382c`  
		Last Modified: Fri, 25 Sep 2020 22:37:21 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04feeed388b71fdca5cc3bce619d65a34f8a1a3e5b0ef03f8392d499970818eb`  
		Last Modified: Fri, 25 Sep 2020 22:37:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c515c4bbd57e5e060382435401656f8c75aeb4df3d35c05184742fb26b59afe`  
		Last Modified: Sat, 26 Sep 2020 01:09:10 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00844731137cb6a0c71ccda3cd3a38d73fb6a6b490e108d5d382f8aa1cbfd89e`  
		Last Modified: Sat, 26 Sep 2020 01:09:11 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5d9a7fdaab7fd68587b855c7f9fa89b54494976273fefcce9926b189b9f813`  
		Last Modified: Sat, 26 Sep 2020 01:09:10 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af001496b5497280afcb76671c6577ea2cbf1844db7dd662bc1ff4b8290af05`  
		Last Modified: Sat, 26 Sep 2020 01:09:10 GMT  
		Size: 226.2 KB (226231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c600bfc3826fca35f18c4c9fa4ac03e8b61e388fc0e5c78985981576c3a582f`  
		Last Modified: Sat, 26 Sep 2020 01:09:19 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
