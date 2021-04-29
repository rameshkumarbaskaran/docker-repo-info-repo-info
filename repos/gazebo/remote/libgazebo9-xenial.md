## `gazebo:libgazebo9-xenial`

```console
$ docker pull gazebo@sha256:8f09987feef6612efd592ce83776c37f8c65ce0a488e20bf8662229cd7abe869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-xenial` - linux; amd64

```console
$ docker pull gazebo@sha256:4297f5cc5bdcc26c40fd1fbcbfe30c413f0221b543970b3b9e17b5b792755b1c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.4 MB (495434520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d1c3ed4c39ad91c3cb3d8aa7fce7e7a1ff597ddd4fd3945ffe7fb15eb82c9c`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:48:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:48:33 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 23 Apr 2021 23:48:34 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Wed, 28 Apr 2021 19:05:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.17.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 28 Apr 2021 19:05:33 GMT
EXPOSE 11345
# Wed, 28 Apr 2021 19:05:33 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 28 Apr 2021 19:05:33 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 28 Apr 2021 19:05:34 GMT
CMD ["gzserver"]
# Wed, 28 Apr 2021 19:09:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.17.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340f215ec5582c3709c8edd826b45865536aee4a0e309b5eaf54bbae4ec4bf2f`  
		Last Modified: Sat, 24 Apr 2021 00:15:49 GMT  
		Size: 16.3 MB (16279968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9887fad184bfee18f93dc0728afcc29ef5a9413cc8e7dd66e94fb7a803959a87`  
		Last Modified: Sat, 24 Apr 2021 00:15:45 GMT  
		Size: 14.8 KB (14759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaaacc64da264322798a93c66aec28cfa0fea4a1cb0cebe2694cd18209fe74a8`  
		Last Modified: Sat, 24 Apr 2021 00:15:45 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5680ec8f99db4c4e5829e2d9d0fa07bbc48283956e97a4acf18748fcadb5903`  
		Last Modified: Wed, 28 Apr 2021 19:18:12 GMT  
		Size: 208.1 MB (208107667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc43beaaffbed249b82082f7a46abcf704a03fd57ec97d63722c0652a91f897`  
		Last Modified: Wed, 28 Apr 2021 19:17:45 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a3e00a1658db4a823a1f59a93f3ff677777d33e225d1505d0334cd3eb14753`  
		Last Modified: Wed, 28 Apr 2021 19:19:01 GMT  
		Size: 224.8 MB (224770390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
