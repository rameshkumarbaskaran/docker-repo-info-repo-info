## `gazebo:libgazebo9-stretch`

```console
$ docker pull gazebo@sha256:ef48ba2c0885f17ca4a8036e9ec4d1bc13dc0997a0f06b003a41419772010651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-stretch` - linux; amd64

```console
$ docker pull gazebo@sha256:c9624faa91e57030486d0b760200135a11a56b2b75d646c2c129c5fa4401bfb7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.0 MB (650964267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346620b7954e4b34997f644aee42009ee4672af9eb4ad4a1a71a284ad24fc6a0`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:22 GMT
ADD file:9f6f0c8b90de3204ad5db95d10d8aa76b42454def6ac811c888ad4e274292c9c in / 
# Thu, 16 Apr 2020 03:27:22 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 23:02:35 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 23:02:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 16 Apr 2020 23:02:39 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 16 Apr 2020 23:04:10 GMT
RUN apt-get update && apt-get install -q -y     gazebo9=9.12.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 23:04:11 GMT
EXPOSE 11345
# Thu, 16 Apr 2020 23:04:11 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 16 Apr 2020 23:04:11 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 16 Apr 2020 23:04:12 GMT
CMD ["gzserver"]
# Thu, 16 Apr 2020 23:06:07 GMT
RUN apt-get update && apt-get install -q -y     libgazebo9-dev=9.12.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7568c21980bd8003ca9d23a218302c6386aac91e069cc0c0be6bedf45476f056`  
		Last Modified: Thu, 16 Apr 2020 03:34:47 GMT  
		Size: 45.4 MB (45375910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288e794c64092ed2a165c6ff45b8c186dbb86290c8fa63c76e71fcd6433d54c2`  
		Last Modified: Thu, 16 Apr 2020 23:06:54 GMT  
		Size: 21.1 MB (21095203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cabf3a51b9e8b499322e4f305b4581934df69682701118eef52d8a324051390`  
		Last Modified: Thu, 16 Apr 2020 23:06:49 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03e89f32e0bbc8222b3304d66f14086b924fbfce22b6a9a385f199cfeaa3a0b`  
		Last Modified: Thu, 16 Apr 2020 23:06:49 GMT  
		Size: 5.0 KB (4980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544ec9a02516016e614710fd10581cc81ac242727f3b9bcd0906acfa7eafb681`  
		Last Modified: Thu, 16 Apr 2020 23:07:34 GMT  
		Size: 279.9 MB (279870905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3faca25932adfea2cd9b9b702e891c50ab5565061fcf0e63add4307d84184f1e`  
		Last Modified: Thu, 16 Apr 2020 23:06:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefbf854e8f0afd01813a3d6de11ad8d7f205216765d937703764f3fd448f92c`  
		Last Modified: Thu, 16 Apr 2020 23:08:54 GMT  
		Size: 304.6 MB (304615661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
