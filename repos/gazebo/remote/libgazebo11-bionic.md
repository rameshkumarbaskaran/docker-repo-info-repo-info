## `gazebo:libgazebo11-bionic`

```console
$ docker pull gazebo@sha256:6be09bc0fc1b10931afe28ac1831d364a362b38543a44001ab1c8b527a1c5af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:ca954985891600a629c70c3fed5575392ab05968dbacbc144a3dfe8b173b12ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.3 MB (547329245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567dfda729fe5639e0f206d0fca6bc7f67807ba7c4129736d0c79bc51a38c68f`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:56:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:56:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:56:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 16 Mar 2023 02:56:45 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 16 Mar 2023 02:59:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.12.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:59:39 GMT
EXPOSE 11345
# Thu, 16 Mar 2023 02:59:39 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 16 Mar 2023 02:59:39 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 16 Mar 2023 02:59:39 GMT
CMD ["gzserver"]
# Thu, 16 Mar 2023 03:03:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.12.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cd150c608fee7837e3a5b28be5c7b540eaf4efa27b3b755d55326470691ce2df`  
		Last Modified: Sun, 12 Mar 2023 07:24:55 GMT  
		Size: 26.7 MB (26710746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73b43b50fc9056c1213c61cfa3193cd15f8faa751905b21e0e9019473426a74`  
		Last Modified: Thu, 16 Mar 2023 03:11:48 GMT  
		Size: 819.0 KB (818997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80805ef2e65269281acd286ca9672562476f0618eeea74bb1d815f4873b22a1e`  
		Last Modified: Thu, 16 Mar 2023 03:11:48 GMT  
		Size: 14.7 MB (14713955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5907d33b51597391f65d538022d4cd115384b11a944b4e3be7701dc74d01a6e`  
		Last Modified: Thu, 16 Mar 2023 03:11:46 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fa021a7315e59ff1601cae9d25dc652d7dd05f79e6ff4fa2e7c25d979be483`  
		Last Modified: Thu, 16 Mar 2023 03:11:46 GMT  
		Size: 5.5 KB (5455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0856a949877b90710be006eefbd852e13c3c48e8a4c1360ad0c94f644a3e8f38`  
		Last Modified: Thu, 16 Mar 2023 03:12:13 GMT  
		Size: 235.6 MB (235585158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b049871e3f6f2a996c2e1a8a317cad0c016b6a014584509af51016c05c87136a`  
		Last Modified: Thu, 16 Mar 2023 03:11:46 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4f59969ad0c4d299c55b0ce4222fb141ecd0fb73fc1aab9aa3c4da8ed1966c`  
		Last Modified: Thu, 16 Mar 2023 03:12:56 GMT  
		Size: 269.5 MB (269493307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
