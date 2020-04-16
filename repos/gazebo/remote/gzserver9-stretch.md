## `gazebo:gzserver9-stretch`

```console
$ docker pull gazebo@sha256:141f047cbf368a648888334b4979cd49b6b3585563bf839e0886b31e2db35a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver9-stretch` - linux; amd64

```console
$ docker pull gazebo@sha256:631d52d4ea72800decf7c1a205c95e6baba5775d6eea9141f5d6260c6abf24b0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.3 MB (346348606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ad46ddba43f924b40af03831b7cbd994eee3106ab978ed36ef09265f9ab6c8`
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
