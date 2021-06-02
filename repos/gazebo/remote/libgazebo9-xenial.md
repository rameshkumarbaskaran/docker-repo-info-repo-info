## `gazebo:libgazebo9-xenial`

```console
$ docker pull gazebo@sha256:7c818dbc5a95d60bcc038212c9e903b4baa54b07acd62d7d2b7575a0b4e4bacf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-xenial` - linux; amd64

```console
$ docker pull gazebo@sha256:e1af0ba016072626f92404f43a9f11176618ab56cedadd94a2a7b4a5d9892a57
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.7 MB (500662276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8ade7641faa63d29760e26910ac741932bdb17aefd6c43eac4b04143a5f0a8`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 19 May 2021 19:45:15 GMT
ADD file:5dd161b04353d3cbc2b258d66ef3c79a8307faa944953a1c7920a3d97468520c in / 
# Wed, 19 May 2021 19:45:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:45:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 19:45:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:45:19 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 20:35:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 20:35:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Wed, 19 May 2021 20:35:27 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Wed, 02 Jun 2021 03:23:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.18.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Jun 2021 03:23:07 GMT
EXPOSE 11345
# Wed, 02 Jun 2021 03:23:07 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 02 Jun 2021 03:23:08 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 02 Jun 2021 03:23:08 GMT
CMD ["gzserver"]
# Wed, 02 Jun 2021 03:27:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.18.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80bce60046fa9e5ccbe54c9bd4bfa3f379ce7bc43bed493ae92389050de04024`  
		Last Modified: Thu, 29 Apr 2021 15:24:23 GMT  
		Size: 46.5 MB (46461779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a738a1554069bc9050c0a60b57fc93e98069e59822677a483cc74cafaf2bf7`  
		Last Modified: Wed, 19 May 2021 19:46:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19cf0706c6229033d11dbf952b3eb96ad70e1f32527960aeb3c83ad86f16551`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4cdd6c27d1f17cf5ff350e76b7efe80aceff4dc99fd518065bf048abd6494a`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1e1b9079fa5dd84cbf5cc4061f736323f316470de86bd85e89278aa955f82f`  
		Last Modified: Wed, 02 Jun 2021 03:48:20 GMT  
		Size: 16.3 MB (16280407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1737c6255e99e13efc21bbe179cb299f62e004cf6c5046b05308166c727b34db`  
		Last Modified: Wed, 02 Jun 2021 03:48:16 GMT  
		Size: 14.8 KB (14760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd95141fcc53b8e4275f45194d698579a11b007c3402da5b91c8e3daac99b0ba`  
		Last Modified: Wed, 02 Jun 2021 03:48:16 GMT  
		Size: 5.5 KB (5548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb414ee39cb698c88bad322f7c4e52f297463dc090ae5d5fb36666999014860a`  
		Last Modified: Wed, 02 Jun 2021 03:48:44 GMT  
		Size: 208.1 MB (208108574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e896b1ac995cd327228f2ce19410f43cd5554928ecceed240a2ba6e2afeb0b`  
		Last Modified: Wed, 02 Jun 2021 03:48:17 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8818752126b4947e6dd121e084c4588963a23f54f2de98a660f277d570cc29`  
		Last Modified: Wed, 02 Jun 2021 03:49:38 GMT  
		Size: 229.8 MB (229789473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
