## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:eb6d33222edcb9b3d72993c835ab713dd05b7bbf7c9db538f536d744c0f269e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `mongo:4-nanoserver` - windows version 10.0.17763.2237; amd64

```console
$ docker pull mongo@sha256:7efc617e91afaed43b07b398d4d11a488b2b3455d513f4333b2c15460448ff9c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.4 MB (334360530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1779b6455a2324b129fef7ba7b4d40ed19134b17de29b12e7567be9c90766250`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 07 Oct 2021 08:01:14 GMT
RUN Apply image 1809-amd64
# Wed, 13 Oct 2021 12:53:34 GMT
SHELL [cmd /S /C]
# Thu, 14 Oct 2021 01:40:20 GMT
USER ContainerAdministrator
# Thu, 14 Oct 2021 01:40:33 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 14 Oct 2021 01:40:34 GMT
USER ContainerUser
# Thu, 14 Oct 2021 01:40:36 GMT
COPY multi:0196f9e96f60ad3e2b92fd0773f8d0fe3a8235e1eefbb9ef1a1f0d672e6a711c in C:\Windows\System32\ 
# Thu, 14 Oct 2021 01:53:27 GMT
ENV MONGO_VERSION=4.4.9
# Thu, 14 Oct 2021 01:53:50 GMT
COPY dir:a23fdbd476f8fa78c67afab345541b41b0096410745b10ee6fa2d9b825d3648b in C:\mongodb 
# Thu, 14 Oct 2021 01:54:12 GMT
RUN mongo --version && mongod --version
# Thu, 14 Oct 2021 01:54:13 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 14 Oct 2021 01:54:14 GMT
EXPOSE 27017
# Thu, 14 Oct 2021 01:54:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:934e212983f208dc2bebc5de38259a6a62f1761868aacfee2cb3585a13b1e24b`  
		Size: 102.7 MB (102661372 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:372f5dac265602794d3a4ddc20bd9845caf2acda0cec410704843c213a880da9`  
		Last Modified: Wed, 13 Oct 2021 13:29:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfae37dcc2021e3d10496776687736e4d2565f4b93492b8286aa9bd4a663324a`  
		Last Modified: Thu, 14 Oct 2021 02:19:23 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b099be52eef9112df652bed33f01c48930744f308329472c54e09e00e77e79`  
		Last Modified: Thu, 14 Oct 2021 02:19:21 GMT  
		Size: 70.2 KB (70170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7102d479d05ed3a9336a5c5e5829142fb9489c43e80f3bcbcc9f22c71f1042f6`  
		Last Modified: Thu, 14 Oct 2021 02:19:21 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455297daaaa79153573901a8796f77c2dd232e2709aeb8638e0b766abbc6875c`  
		Last Modified: Thu, 14 Oct 2021 02:19:21 GMT  
		Size: 274.0 KB (273992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab255d9d8fdc8f4e2e097c5291a33fdf2a533cb1bf025bf64163d9ed63af376`  
		Last Modified: Thu, 14 Oct 2021 02:28:46 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf09d1ee72deba446cdbd0621c56bb86d3d20070e427ae96b4efabae12f55c26`  
		Last Modified: Thu, 14 Oct 2021 02:29:31 GMT  
		Size: 231.3 MB (231270238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e124cc05c3c2a54a2ceb9122a287dff09a88d5f4a0865b26aab3ed256be56f01`  
		Last Modified: Thu, 14 Oct 2021 02:28:45 GMT  
		Size: 76.8 KB (76762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc477303ca446ec70a572cf92d996d60db076939b6236d0225172e826479a07`  
		Last Modified: Thu, 14 Oct 2021 02:28:44 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142235b1a88e5df6eec143911232d5f9eb93f041bf9dd03b1f48532c12c00d46`  
		Last Modified: Thu, 14 Oct 2021 02:28:44 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a45e51e934317bcef07cad5765863b28523c373d164d2d6260f05d6d4de647`  
		Last Modified: Thu, 14 Oct 2021 02:28:44 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
