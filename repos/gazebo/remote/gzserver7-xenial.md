## `gazebo:gzserver7-xenial`

```console
$ docker pull gazebo@sha256:b3fb1480b84d54e98e818e50a52ccfdbb341b266cd92a73d09f40f47515a3a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver7-xenial` - linux; amd64

```console
$ docker pull gazebo@sha256:1f4c48ce6bc7e189632cdd175c52ad5cbe657b5ec0429bda7ce8088723fdd760
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250605122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f89164eee6489f5ad1d7f3159a86ee6a3829e479f3c306446542e6fae401d86e`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 16 Jan 2020 01:21:30 GMT
ADD file:4b2eb5cd0b37ca0154f3c5ad9212f5bc7244a35806395a9c76a96723d708b83a in / 
# Thu, 16 Jan 2020 01:21:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 01:21:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:21:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:21:32 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 01:54:04 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 01:54:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 16 Jan 2020 01:54:05 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 16 Jan 2020 01:56:23 GMT
RUN apt-get update && apt-get install -q -y     gazebo7=7.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 01:56:23 GMT
EXPOSE 11345
# Thu, 16 Jan 2020 01:56:23 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 16 Jan 2020 01:56:24 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 16 Jan 2020 01:56:24 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:0a01a72a686c389637334de1e2d0012da298960366f6d8f358b8e10dc3b5e330`  
		Last Modified: Wed, 15 Jan 2020 14:20:15 GMT  
		Size: 44.1 MB (44149770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc899a5544da1a6cfb970d2484d32c063f8df26a430d92f39c98e72261e226f2`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 525.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19197c55075519928dd2ff059745665a2c9b72f4e8af6f7a1ce662e696d339bd`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716d454e56b61d1343a01f3b1829574333e2e3df20e77d1958d7b0b939ea1b61`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa669e9848039af3697ca0e6d605e17f073c3474b60533ee0c0bcce38078522`  
		Last Modified: Thu, 16 Jan 2020 02:13:16 GMT  
		Size: 16.7 MB (16657692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346b316b49a866dd51d8b3521df79b57140abb2e1f147ad354151ba6a01a2cfd`  
		Last Modified: Thu, 16 Jan 2020 02:13:11 GMT  
		Size: 13.1 KB (13114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f206383aa581dbf560a4a47b28fff4e4dd87358714faaaa1ff9a31533b4d0cd4`  
		Last Modified: Thu, 16 Jan 2020 02:13:11 GMT  
		Size: 5.5 KB (5520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd12cad64b48aa557d003ce06904bc7010022d04a7b51512bad3c3b9788cb06`  
		Last Modified: Thu, 16 Jan 2020 02:13:42 GMT  
		Size: 189.8 MB (189777301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d09d9dfc4bc9c8bd174f689b7299d614d9943827d08ddfab510e2ca5879da8f`  
		Last Modified: Thu, 16 Jan 2020 02:13:11 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
