<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `notary`

-	[`notary:server`](#notaryserver)
-	[`notary:server-0.7.0`](#notaryserver-070)
-	[`notary:signer`](#notarysigner)
-	[`notary:signer-0.7.0`](#notarysigner-070)

## `notary:server`

```console
$ docker pull notary@sha256:75b9b70205f68ecd17ca28ed623e4423fd5dd5c46715dd0e106dd63445f74830
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `notary:server` - linux; amd64

```console
$ docker pull notary@sha256:4c3d07b2fed560ab0012452aa8a6f58533ddf2d4a3845fa89b74d9455816b454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7957746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8b42cfd53b749f9c6d5aa0b6b385577be0f52c83726122990f436ec7aa41f4`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab53671fb67541f4e8ae603428eb0311fc3a8efaad071fc498271f210d5a592`  
		Last Modified: Fri, 01 Dec 2023 00:11:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4589312f8e61782f6c201afae5ad8569f42d02bc720733f28331e703f967662`  
		Last Modified: Fri, 01 Dec 2023 00:11:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d705f15fab07b30bd16a1e7a7b1e58fde1ef7dc6215bd9a66af8a14f549f7d19`  
		Last Modified: Fri, 01 Dec 2023 00:11:15 GMT  
		Size: 5.1 MB (5147844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9f2d4861b86300614077b6db220f6d7c34cf8948fd19353439cbba79168ffd`  
		Last Modified: Fri, 01 Dec 2023 00:11:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4052bc9339763126620fcfb66fad1f265fadb1124e6480899a0fda5929f0372`  
		Last Modified: Fri, 01 Dec 2023 00:11:15 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:692819af7e57efe94abadb451e05aa5eb042a540a2eae7095d37507dbd66dc94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 KB (110688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d70c1f71390e0ace1053d285ab3b637d482f5d3327f2e5d4a035af20a0a5331`

```dockerfile
```

-	Layers:
	-	`sha256:b88b97ec5fbc734c852063a2789a72146a83b64bd2339ba28cbfcd8101d8796b`  
		Last Modified: Fri, 01 Dec 2023 00:11:15 GMT  
		Size: 91.5 KB (91458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d6b3844c1927b5a9facc9ac048e1e41876bddc6cad9e94358c1ffc9aa574e06`  
		Last Modified: Fri, 01 Dec 2023 00:11:15 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server` - linux; arm variant v6

```console
$ docker pull notary@sha256:9f245d4b08cfa9f6934e315f60699db5caacbf638d012c4c6f16dfa10066ae4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a1921e9cff1b4a1e2f42a76d36cba332469c640e928fdd53a1f88c2aa9feb2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cde69ed9ff455c9499e13b92a67b8722a1710401c31263561cf43c64193c3d80 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:b76d44755a1732ac572a54d4df4cfff9671b9466b719f4c80a81fd9397dbc3dc`  
		Last Modified: Thu, 30 Nov 2023 22:50:02 GMT  
		Size: 2.6 MB (2615844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f45e9feb3ba2edfc080d49db4581485558c6233268178d4453fe2a8325279b`  
		Last Modified: Fri, 01 Dec 2023 12:31:22 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954094d4258a2c95977f780bff4e8892d99f25ce049f6a44b07e674e102c6b5a`  
		Last Modified: Fri, 01 Dec 2023 12:31:22 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59be483442a177ddfc2b11ddd623f549cd5354794cd0ff706dd6d0bf64e40286`  
		Last Modified: Fri, 01 Dec 2023 12:31:23 GMT  
		Size: 4.9 MB (4893562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e05adab9286a8bb4aff1c122c42d0226ea9168665ea394ec523ab969750dddb`  
		Last Modified: Fri, 01 Dec 2023 12:31:22 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b8755f11a0174dd0e29522350fc4f07395492e9ff4f68f1014eb39dba21d0c`  
		Last Modified: Fri, 01 Dec 2023 12:31:22 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:d147a2dd70b2bc88049efd0032dd9cc20e01aa0833db2bc1702b2775dab2baaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f672acd668849ed1cfdb5c5e3040dd835e50b024d9491c53c6136d9cddeaa3ee`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202c4dd0f102d31afdf745598c8b608887eb3b4142b5fbb8619d8b431ab3d348`  
		Last Modified: Mon, 07 Aug 2023 22:45:27 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565afe3e3634f553e5e4798c9171e212127f00b3c23c93faa1eb17c3027fad79`  
		Last Modified: Mon, 07 Aug 2023 22:45:27 GMT  
		Size: 118.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6128cc3d34da4edf1351e0397480921013481a869739484a9b6366c2a03448`  
		Last Modified: Mon, 07 Aug 2023 22:45:27 GMT  
		Size: 4.7 MB (4734458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73788bca9233077876bfb7ad08ab7e664745b8945cc9734482694a0be8bbd5e4`  
		Last Modified: Mon, 07 Aug 2023 22:45:28 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad868bcf088e64171900901ed63038b26bb0c717b90d360356dce16d10e14ee`  
		Last Modified: Mon, 07 Aug 2023 22:45:28 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:2dde0ea7564373ff977abd5a03af7adae5459d7bfca5e8106f7f8cbd4abe5462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 KB (109918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5164b3b1e32bde933e4f3fb90aa6b0cc87ef8a2f1a28b66470fd7528e973ab43`

```dockerfile
```

-	Layers:
	-	`sha256:c5e21a9ebe71e38ee55dfa7571bd14d011af379320ec54dfbea371c42ddba1ba`  
		Last Modified: Tue, 17 Oct 2023 20:05:04 GMT  
		Size: 91.5 KB (91503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b40bcdcaceed0964ba033068a0997859daa570f689c80a594c44c40ace101d`  
		Last Modified: Tue, 17 Oct 2023 20:05:04 GMT  
		Size: 18.4 KB (18415 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server` - linux; 386

```console
$ docker pull notary@sha256:9d3d4b1aa6185b8da72a0e97e7a8a4156287ce89479edc87f77633ded278e567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7763475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f1ead4bf0ac898f792abd5585cb36385ee20dc3d39e6cb78a436dc4829c565`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:c06b4f6991638e506d4d0a4d70c4a78ba30b971767802af4c6b837cdf59d4303 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:be0d19c155de823c6b37eaaba7cdec9085e8f1e39b1dd5982a19acb6c8c97cc5`  
		Last Modified: Mon, 07 Aug 2023 19:39:20 GMT  
		Size: 2.8 MB (2810553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f5e07cf5dd2ddef185d26fcd872c6ea88a977881e1ae912091ac7e0c58352a`  
		Last Modified: Tue, 17 Oct 2023 18:59:59 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284bb3fb32d977ba57e02dd08118bff966afe825f4fdf6077ef41b8133bd8128`  
		Last Modified: Tue, 17 Oct 2023 18:59:59 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bed0c7971721a02c14ed33f5192db014c950291eb24de851fdaf1f8e8514163`  
		Last Modified: Tue, 17 Oct 2023 19:00:00 GMT  
		Size: 5.0 MB (4950790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2c554b9ba2aa841b79ec575972569cdb690ee928dc74a607600c9ef2943094`  
		Last Modified: Tue, 17 Oct 2023 18:59:59 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22abeb4c57a42516cce9452f32a3da9f0be57623f5c8d3f459024a76fd0f79bb`  
		Last Modified: Tue, 17 Oct 2023 19:00:00 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:e153fe40e9c6609781db699d49882ba1ba3b5601d6924e4ead6ec278d02d651a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b322c21f5f52b15e50942a957fdd2457c4edb0908c3758bbf12d67844e4831a3`

```dockerfile
```

-	Layers:
	-	`sha256:ae75b198267a3c988fd304e1eed6c176324f92c3c08808c146879b901b618edf`  
		Last Modified: Tue, 17 Oct 2023 18:59:59 GMT  
		Size: 19.0 KB (18986 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server` - linux; ppc64le

```console
$ docker pull notary@sha256:ead953dd52edeea966545664b2c9fec2e1bb4d3a79671f95190819095351f641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f69cab61b19b8e233d0f48988b8f46e0b56cf4115298d94d3bb1e858c730fa`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:41dd492ac8086a6a7ae54f70f208d397f81d19c9ada61f7e52b1f678c0e08ae3 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:ae6fb3870f7991147b39ddb2fee9e659464482f341bd584e2b45ba18fbe5b39d`  
		Last Modified: Thu, 30 Nov 2023 23:20:26 GMT  
		Size: 2.8 MB (2802949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bfd048ed14aaf67fd63563fa3533db27519d50152d35a987605aea84e79d96`  
		Last Modified: Fri, 01 Dec 2023 12:03:35 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d895143619321e2f5df1823f92cce72ac1311f9650ddff6203e0e5284f2af5cd`  
		Last Modified: Fri, 01 Dec 2023 12:03:35 GMT  
		Size: 118.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1b4db90ea623800b14880bfb3fe5c53813ce621ea63cf187da4fdab824a472`  
		Last Modified: Fri, 01 Dec 2023 12:03:36 GMT  
		Size: 4.6 MB (4639148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c83b1ae127182358a49736bdebe57f1dd4b5205d01acde1b5e2d8a8d944623`  
		Last Modified: Fri, 01 Dec 2023 12:03:37 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96da171b30ddf5f9a201a836648d290a6cb21215a10b4db44c7a6033a737f9e`  
		Last Modified: Fri, 01 Dec 2023 12:03:37 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:6235a23c8e809f36b0e6a6ef45efe0079f9a92ddb62d4ac397241074b79d42c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 KB (109110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9c42df43111b1428916743d29a54283985650e719bcd3abceb966531210761`

```dockerfile
```

-	Layers:
	-	`sha256:e1ba859e0109480897409839c91fd296e46f5d31c3e8877c45693a06b59d6121`  
		Last Modified: Fri, 01 Dec 2023 12:03:36 GMT  
		Size: 89.8 KB (89844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e8e65ceb602e34f6264a29adb069f34af5ac3736ef7ae4fc65ed981d1e246d6`  
		Last Modified: Fri, 01 Dec 2023 12:03:35 GMT  
		Size: 19.3 KB (19266 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server` - linux; s390x

```console
$ docker pull notary@sha256:66118e7982bb814a9d939808797fc0e073194732d5bcdb0afaa98c515d17ab23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7570735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375dd24b82c69922bcaab7aedbd6c4aa53455221175e092aaa73af2229bc6f37`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:f7a7034bb4c8ab0fed6e2c4b09f15f3e7076270496340adceac7e01aabf87857 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:3710549eb8868990a62c8d4471b58594422f5b4b00b9f1301ab37536932fc449`  
		Last Modified: Thu, 30 Nov 2023 22:43:07 GMT  
		Size: 2.6 MB (2592110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3051463e76e45694bdac001475d6401201e997fcc6b1064dd5714221e9522`  
		Last Modified: Fri, 01 Dec 2023 11:05:17 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e2029cbe168ad538ca4f618f818e1776db4675da9dcf5cb1cafb1ae26c4c73`  
		Last Modified: Fri, 01 Dec 2023 11:05:17 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386697fcd6409c5fbe81e26bbcda06c92d97ea3c6a67b361b36d903e6ef46765`  
		Last Modified: Fri, 01 Dec 2023 11:05:17 GMT  
		Size: 5.0 MB (4976494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa463bb75cc612787401b3735a60f0c49ce27958de1bdb663835241ff3a3a44`  
		Last Modified: Fri, 01 Dec 2023 11:05:18 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9601e931117156c90946d2ee4dcf71edebc280bb2927e29c98e360fc8f2b67`  
		Last Modified: Fri, 01 Dec 2023 11:05:18 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:c35c2d748647d9150a218c6f9bba1ba76b2857c71608e21de4dea7e277400a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 KB (109052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd9c541de7f41ff1349988fe6c4a04896f2fbbd710e780110c9bfb08d9d0c9c`

```dockerfile
```

-	Layers:
	-	`sha256:564eda7af0ad5159f164187d1ae3bd39c19dc74b7a48b04c99c67d2b422b5029`  
		Last Modified: Fri, 01 Dec 2023 11:05:17 GMT  
		Size: 89.8 KB (89822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e73fd057c7a07056164b551f7e7bf9b6a82dfd98fcf9a3d0cf56ea66dd7a88b`  
		Last Modified: Fri, 01 Dec 2023 11:05:17 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json

## `notary:server-0.7.0`

```console
$ docker pull notary@sha256:75b9b70205f68ecd17ca28ed623e4423fd5dd5c46715dd0e106dd63445f74830
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `notary:server-0.7.0` - linux; amd64

```console
$ docker pull notary@sha256:4c3d07b2fed560ab0012452aa8a6f58533ddf2d4a3845fa89b74d9455816b454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7957746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8b42cfd53b749f9c6d5aa0b6b385577be0f52c83726122990f436ec7aa41f4`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab53671fb67541f4e8ae603428eb0311fc3a8efaad071fc498271f210d5a592`  
		Last Modified: Fri, 01 Dec 2023 00:11:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4589312f8e61782f6c201afae5ad8569f42d02bc720733f28331e703f967662`  
		Last Modified: Fri, 01 Dec 2023 00:11:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d705f15fab07b30bd16a1e7a7b1e58fde1ef7dc6215bd9a66af8a14f549f7d19`  
		Last Modified: Fri, 01 Dec 2023 00:11:15 GMT  
		Size: 5.1 MB (5147844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9f2d4861b86300614077b6db220f6d7c34cf8948fd19353439cbba79168ffd`  
		Last Modified: Fri, 01 Dec 2023 00:11:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4052bc9339763126620fcfb66fad1f265fadb1124e6480899a0fda5929f0372`  
		Last Modified: Fri, 01 Dec 2023 00:11:15 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:692819af7e57efe94abadb451e05aa5eb042a540a2eae7095d37507dbd66dc94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 KB (110688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d70c1f71390e0ace1053d285ab3b637d482f5d3327f2e5d4a035af20a0a5331`

```dockerfile
```

-	Layers:
	-	`sha256:b88b97ec5fbc734c852063a2789a72146a83b64bd2339ba28cbfcd8101d8796b`  
		Last Modified: Fri, 01 Dec 2023 00:11:15 GMT  
		Size: 91.5 KB (91458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d6b3844c1927b5a9facc9ac048e1e41876bddc6cad9e94358c1ffc9aa574e06`  
		Last Modified: Fri, 01 Dec 2023 00:11:15 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:9f245d4b08cfa9f6934e315f60699db5caacbf638d012c4c6f16dfa10066ae4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a1921e9cff1b4a1e2f42a76d36cba332469c640e928fdd53a1f88c2aa9feb2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cde69ed9ff455c9499e13b92a67b8722a1710401c31263561cf43c64193c3d80 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:b76d44755a1732ac572a54d4df4cfff9671b9466b719f4c80a81fd9397dbc3dc`  
		Last Modified: Thu, 30 Nov 2023 22:50:02 GMT  
		Size: 2.6 MB (2615844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f45e9feb3ba2edfc080d49db4581485558c6233268178d4453fe2a8325279b`  
		Last Modified: Fri, 01 Dec 2023 12:31:22 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954094d4258a2c95977f780bff4e8892d99f25ce049f6a44b07e674e102c6b5a`  
		Last Modified: Fri, 01 Dec 2023 12:31:22 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59be483442a177ddfc2b11ddd623f549cd5354794cd0ff706dd6d0bf64e40286`  
		Last Modified: Fri, 01 Dec 2023 12:31:23 GMT  
		Size: 4.9 MB (4893562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e05adab9286a8bb4aff1c122c42d0226ea9168665ea394ec523ab969750dddb`  
		Last Modified: Fri, 01 Dec 2023 12:31:22 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b8755f11a0174dd0e29522350fc4f07395492e9ff4f68f1014eb39dba21d0c`  
		Last Modified: Fri, 01 Dec 2023 12:31:22 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:d147a2dd70b2bc88049efd0032dd9cc20e01aa0833db2bc1702b2775dab2baaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f672acd668849ed1cfdb5c5e3040dd835e50b024d9491c53c6136d9cddeaa3ee`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202c4dd0f102d31afdf745598c8b608887eb3b4142b5fbb8619d8b431ab3d348`  
		Last Modified: Mon, 07 Aug 2023 22:45:27 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565afe3e3634f553e5e4798c9171e212127f00b3c23c93faa1eb17c3027fad79`  
		Last Modified: Mon, 07 Aug 2023 22:45:27 GMT  
		Size: 118.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6128cc3d34da4edf1351e0397480921013481a869739484a9b6366c2a03448`  
		Last Modified: Mon, 07 Aug 2023 22:45:27 GMT  
		Size: 4.7 MB (4734458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73788bca9233077876bfb7ad08ab7e664745b8945cc9734482694a0be8bbd5e4`  
		Last Modified: Mon, 07 Aug 2023 22:45:28 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad868bcf088e64171900901ed63038b26bb0c717b90d360356dce16d10e14ee`  
		Last Modified: Mon, 07 Aug 2023 22:45:28 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:2dde0ea7564373ff977abd5a03af7adae5459d7bfca5e8106f7f8cbd4abe5462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 KB (109918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5164b3b1e32bde933e4f3fb90aa6b0cc87ef8a2f1a28b66470fd7528e973ab43`

```dockerfile
```

-	Layers:
	-	`sha256:c5e21a9ebe71e38ee55dfa7571bd14d011af379320ec54dfbea371c42ddba1ba`  
		Last Modified: Tue, 17 Oct 2023 20:05:04 GMT  
		Size: 91.5 KB (91503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b40bcdcaceed0964ba033068a0997859daa570f689c80a594c44c40ace101d`  
		Last Modified: Tue, 17 Oct 2023 20:05:04 GMT  
		Size: 18.4 KB (18415 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server-0.7.0` - linux; 386

```console
$ docker pull notary@sha256:9d3d4b1aa6185b8da72a0e97e7a8a4156287ce89479edc87f77633ded278e567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7763475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f1ead4bf0ac898f792abd5585cb36385ee20dc3d39e6cb78a436dc4829c565`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:c06b4f6991638e506d4d0a4d70c4a78ba30b971767802af4c6b837cdf59d4303 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:be0d19c155de823c6b37eaaba7cdec9085e8f1e39b1dd5982a19acb6c8c97cc5`  
		Last Modified: Mon, 07 Aug 2023 19:39:20 GMT  
		Size: 2.8 MB (2810553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f5e07cf5dd2ddef185d26fcd872c6ea88a977881e1ae912091ac7e0c58352a`  
		Last Modified: Tue, 17 Oct 2023 18:59:59 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284bb3fb32d977ba57e02dd08118bff966afe825f4fdf6077ef41b8133bd8128`  
		Last Modified: Tue, 17 Oct 2023 18:59:59 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bed0c7971721a02c14ed33f5192db014c950291eb24de851fdaf1f8e8514163`  
		Last Modified: Tue, 17 Oct 2023 19:00:00 GMT  
		Size: 5.0 MB (4950790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2c554b9ba2aa841b79ec575972569cdb690ee928dc74a607600c9ef2943094`  
		Last Modified: Tue, 17 Oct 2023 18:59:59 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22abeb4c57a42516cce9452f32a3da9f0be57623f5c8d3f459024a76fd0f79bb`  
		Last Modified: Tue, 17 Oct 2023 19:00:00 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:e153fe40e9c6609781db699d49882ba1ba3b5601d6924e4ead6ec278d02d651a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b322c21f5f52b15e50942a957fdd2457c4edb0908c3758bbf12d67844e4831a3`

```dockerfile
```

-	Layers:
	-	`sha256:ae75b198267a3c988fd304e1eed6c176324f92c3c08808c146879b901b618edf`  
		Last Modified: Tue, 17 Oct 2023 18:59:59 GMT  
		Size: 19.0 KB (18986 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:ead953dd52edeea966545664b2c9fec2e1bb4d3a79671f95190819095351f641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f69cab61b19b8e233d0f48988b8f46e0b56cf4115298d94d3bb1e858c730fa`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:41dd492ac8086a6a7ae54f70f208d397f81d19c9ada61f7e52b1f678c0e08ae3 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:ae6fb3870f7991147b39ddb2fee9e659464482f341bd584e2b45ba18fbe5b39d`  
		Last Modified: Thu, 30 Nov 2023 23:20:26 GMT  
		Size: 2.8 MB (2802949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bfd048ed14aaf67fd63563fa3533db27519d50152d35a987605aea84e79d96`  
		Last Modified: Fri, 01 Dec 2023 12:03:35 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d895143619321e2f5df1823f92cce72ac1311f9650ddff6203e0e5284f2af5cd`  
		Last Modified: Fri, 01 Dec 2023 12:03:35 GMT  
		Size: 118.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1b4db90ea623800b14880bfb3fe5c53813ce621ea63cf187da4fdab824a472`  
		Last Modified: Fri, 01 Dec 2023 12:03:36 GMT  
		Size: 4.6 MB (4639148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c83b1ae127182358a49736bdebe57f1dd4b5205d01acde1b5e2d8a8d944623`  
		Last Modified: Fri, 01 Dec 2023 12:03:37 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96da171b30ddf5f9a201a836648d290a6cb21215a10b4db44c7a6033a737f9e`  
		Last Modified: Fri, 01 Dec 2023 12:03:37 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:6235a23c8e809f36b0e6a6ef45efe0079f9a92ddb62d4ac397241074b79d42c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 KB (109110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9c42df43111b1428916743d29a54283985650e719bcd3abceb966531210761`

```dockerfile
```

-	Layers:
	-	`sha256:e1ba859e0109480897409839c91fd296e46f5d31c3e8877c45693a06b59d6121`  
		Last Modified: Fri, 01 Dec 2023 12:03:36 GMT  
		Size: 89.8 KB (89844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e8e65ceb602e34f6264a29adb069f34af5ac3736ef7ae4fc65ed981d1e246d6`  
		Last Modified: Fri, 01 Dec 2023 12:03:35 GMT  
		Size: 19.3 KB (19266 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:66118e7982bb814a9d939808797fc0e073194732d5bcdb0afaa98c515d17ab23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7570735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375dd24b82c69922bcaab7aedbd6c4aa53455221175e092aaa73af2229bc6f37`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:f7a7034bb4c8ab0fed6e2c4b09f15f3e7076270496340adceac7e01aabf87857 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:3710549eb8868990a62c8d4471b58594422f5b4b00b9f1301ab37536932fc449`  
		Last Modified: Thu, 30 Nov 2023 22:43:07 GMT  
		Size: 2.6 MB (2592110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3051463e76e45694bdac001475d6401201e997fcc6b1064dd5714221e9522`  
		Last Modified: Fri, 01 Dec 2023 11:05:17 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e2029cbe168ad538ca4f618f818e1776db4675da9dcf5cb1cafb1ae26c4c73`  
		Last Modified: Fri, 01 Dec 2023 11:05:17 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386697fcd6409c5fbe81e26bbcda06c92d97ea3c6a67b361b36d903e6ef46765`  
		Last Modified: Fri, 01 Dec 2023 11:05:17 GMT  
		Size: 5.0 MB (4976494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa463bb75cc612787401b3735a60f0c49ce27958de1bdb663835241ff3a3a44`  
		Last Modified: Fri, 01 Dec 2023 11:05:18 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9601e931117156c90946d2ee4dcf71edebc280bb2927e29c98e360fc8f2b67`  
		Last Modified: Fri, 01 Dec 2023 11:05:18 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:c35c2d748647d9150a218c6f9bba1ba76b2857c71608e21de4dea7e277400a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 KB (109052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd9c541de7f41ff1349988fe6c4a04896f2fbbd710e780110c9bfb08d9d0c9c`

```dockerfile
```

-	Layers:
	-	`sha256:564eda7af0ad5159f164187d1ae3bd39c19dc74b7a48b04c99c67d2b422b5029`  
		Last Modified: Fri, 01 Dec 2023 11:05:17 GMT  
		Size: 89.8 KB (89822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e73fd057c7a07056164b551f7e7bf9b6a82dfd98fcf9a3d0cf56ea66dd7a88b`  
		Last Modified: Fri, 01 Dec 2023 11:05:17 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json

## `notary:signer`

```console
$ docker pull notary@sha256:7fc172c063a6ed68134432c1db849dfda2a191a61d9b7a43d14f6aacba51d0cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `notary:signer` - linux; amd64

```console
$ docker pull notary@sha256:a5f3cf14ec1f9dbe64f5038168764468bf8cf36023f8c1d763abd3bcbe2a5952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7572933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61447c100d57a41cd6d7de0b918e258904d083cab09c7b290a8e5cddf1a383a4`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0a66a0a7b087da7f9fa9bcdc96d80ae3321e565fc4a638465abdeb792ea1ab`  
		Last Modified: Fri, 01 Dec 2023 00:11:09 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f52aecd80f774b20144d76df7a1bd30afde4c022a082345e77412724e5de78d`  
		Last Modified: Fri, 01 Dec 2023 00:11:09 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8e5637f614944c20b445d103b62cbf9d5075cffbc97f04ac7e7934dccdcfde`  
		Last Modified: Fri, 01 Dec 2023 00:11:09 GMT  
		Size: 4.8 MB (4763081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6da303ea01f1dcceeed1c542f07d37db7d2365b66f40e36af725411bb4f125`  
		Last Modified: Fri, 01 Dec 2023 00:11:10 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b01e3f98461ce88ec08bac5847e6bee5cab2727f844407e5ffb58c77e9a1ac6`  
		Last Modified: Fri, 01 Dec 2023 00:11:10 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:9346c6fe8bf3d29a34e0e1d10f1730feff4461a2e4e2cec704a90490be890d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 KB (107256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64d8edc2c7e9d523a11d6b1ea4764f09f5f5fc6fe7551968068c4294c1c0f48`

```dockerfile
```

-	Layers:
	-	`sha256:f05c794c11c4670ee3b2bf18f481970753817e33407b854e72b92746a6734dee`  
		Last Modified: Fri, 01 Dec 2023 00:11:09 GMT  
		Size: 88.0 KB (88011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:080d7a72705ea449c50069d2ca075026c7cfb046eed5d6d3923af5215bc7dbca`  
		Last Modified: Fri, 01 Dec 2023 00:11:09 GMT  
		Size: 19.2 KB (19245 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer` - linux; arm variant v6

```console
$ docker pull notary@sha256:65861e496c2a89861f24aae1e230413422204f5d85529405e213e137c03ddf53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25fc96cf0be3836d3e800e2e675a5fa860ab4ac12bed105b2de1d2099dcf6dbb`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cde69ed9ff455c9499e13b92a67b8722a1710401c31263561cf43c64193c3d80 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:b76d44755a1732ac572a54d4df4cfff9671b9466b719f4c80a81fd9397dbc3dc`  
		Last Modified: Thu, 30 Nov 2023 22:50:02 GMT  
		Size: 2.6 MB (2615844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f45e9feb3ba2edfc080d49db4581485558c6233268178d4453fe2a8325279b`  
		Last Modified: Fri, 01 Dec 2023 12:31:22 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f02f663975232742358fed9118fd56abed084a8b0350c9dd332e90c9becea4`  
		Last Modified: Fri, 01 Dec 2023 12:31:42 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03397ec88fc769559ee4b471e98c53345450eea8a2f0ac146b93cf38b9f3b6cf`  
		Last Modified: Fri, 01 Dec 2023 12:31:43 GMT  
		Size: 4.5 MB (4526083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22e564c80a0e1d630759a8adf2715c6f3e9eea6922d07743cbfca49340c8688`  
		Last Modified: Fri, 01 Dec 2023 12:31:42 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c311966ad150702a111c2fbfb2141efab1f7b273d7d218d95ac68c55dc840b`  
		Last Modified: Fri, 01 Dec 2023 12:31:42 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:d0b2157e191e4ba482b1840f736d0d5f8e03e69cd939e2997b53bf9bb70cb016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7103175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69eec41fd3d6cf59d8bb581a10497f7417bffab2b543059ee887a590df99b84`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202c4dd0f102d31afdf745598c8b608887eb3b4142b5fbb8619d8b431ab3d348`  
		Last Modified: Mon, 07 Aug 2023 22:45:27 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f88739c04bec4884bc40c7d216e4e9211441e2d033c5861f631bb0925b478fa`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 118.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f13b4a5fcaf14870b0afd1801c5ea0380125660000fd5e65bc19c7ae8dee6d`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 4.4 MB (4393084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b200dfa82abb58b4aa87e1cda3b731e8020c5ca1217d041b2c3c0284514c9c4`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da7244fcfdb45e21dcac9ea3d397ec3d43317799fbc86f16ec39bc6827ade69`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:244799276b035bce3224f3f79c4b7b9e0aded1870794878003a52a9d8cf3781a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 KB (106071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afda2c6f5dcb6f88ab10fcb1bcd90bd754e6d4d6b6edb0dfa41e75749e23832c`

```dockerfile
```

-	Layers:
	-	`sha256:7c9c855ac1ab70995fcbf9fe9684adc44c7aa1c882133bf2d8dc85721cb2d860`  
		Last Modified: Tue, 17 Oct 2023 19:00:44 GMT  
		Size: 87.6 KB (87640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdca200e6121df920c204dc77a79b981b9384195ab438933a829f9c1d6ab18ca`  
		Last Modified: Tue, 17 Oct 2023 19:00:45 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer` - linux; 386

```console
$ docker pull notary@sha256:c3c9cfa8a3e89ea14663516300287f199daaed5aef0c6a0063ba451673d9c085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d486e4ae2bb3d2cab2dde433f02130da8ae238b161d56700c17325b5e77093`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:c06b4f6991638e506d4d0a4d70c4a78ba30b971767802af4c6b837cdf59d4303 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:be0d19c155de823c6b37eaaba7cdec9085e8f1e39b1dd5982a19acb6c8c97cc5`  
		Last Modified: Mon, 07 Aug 2023 19:39:20 GMT  
		Size: 2.8 MB (2810553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596da12c2e0de93c921f09f80dc157315fd51dc526c26c681e009068df5568c8`  
		Last Modified: Tue, 17 Oct 2023 18:59:50 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bb43db3153fdcdf459b45889c76eeaca751b5a0febc7091e481cba1037f6eb`  
		Last Modified: Tue, 17 Oct 2023 18:59:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b757696a027c52ff6a4f41267a37af932d79007fe75adef68a03e4db29cab75b`  
		Last Modified: Tue, 17 Oct 2023 18:59:50 GMT  
		Size: 4.6 MB (4579028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9801338c9c3995199351989ccf7a80c57e88a1a2ba79e8b71870abe62355662c`  
		Last Modified: Tue, 17 Oct 2023 18:59:50 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e6f75c5fee4e0b872d36961655c4e8103de49fe771f2390af597ea1dc591bf`  
		Last Modified: Tue, 17 Oct 2023 18:59:50 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:2a7832d044b996c0336436dcdb25e356d5267cb1be5438344c16b4f1368a55a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2c1e17b9b29692bdea190cc1626243bc46b522299047c6b7ec5a764c5f987e`

```dockerfile
```

-	Layers:
	-	`sha256:eae9624154b2c579a780e1c33f1d0df3e69761a24ad7d3414c420d01c825a058`  
		Last Modified: Tue, 17 Oct 2023 18:59:50 GMT  
		Size: 19.0 KB (19002 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer` - linux; ppc64le

```console
$ docker pull notary@sha256:8eb5fb1e9d7895f95d2c6485df3c1d62ae867114699be79bf388b931c587865d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7101990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc77dc06e2f6fd97a37ffd4c11036a2d71048ba31e0f8bcbc8306a3e0b39a44`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:41dd492ac8086a6a7ae54f70f208d397f81d19c9ada61f7e52b1f678c0e08ae3 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:ae6fb3870f7991147b39ddb2fee9e659464482f341bd584e2b45ba18fbe5b39d`  
		Last Modified: Thu, 30 Nov 2023 23:20:26 GMT  
		Size: 2.8 MB (2802949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bfd048ed14aaf67fd63563fa3533db27519d50152d35a987605aea84e79d96`  
		Last Modified: Fri, 01 Dec 2023 12:03:35 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9421ec33edc3cb3d38249f1ba62d9fa1f6baae3d87de84d82a4657879b79bc10`  
		Last Modified: Fri, 01 Dec 2023 12:04:37 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800ce24dc1465688b4bef5c02eb0c0c0b42e23f89b86abdc4cc5ca9a0fda4f54`  
		Last Modified: Fri, 01 Dec 2023 12:04:38 GMT  
		Size: 4.3 MB (4296972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2decdf73454ce64d52b01b21838de42d299e8cb05629b8f17f4954025e8164`  
		Last Modified: Fri, 01 Dec 2023 12:04:37 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9887737212ebd2747b8706ac29a46ca6ea9f12d9335e5a88c10d41439e5fab43`  
		Last Modified: Fri, 01 Dec 2023 12:04:37 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:d777a1b17cf821e4518af7210ec644a565bb09521fc8fed18cbb00b146457adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 KB (104857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6d08dc0a6a1b5a92a376fdb0dde82d83399fbe8e6169a69699872414eeb10c`

```dockerfile
```

-	Layers:
	-	`sha256:2c2659606c62b1e9915fe53cfb8c14bf6aee517c8fe16d376a3b1a5935f78e80`  
		Last Modified: Fri, 01 Dec 2023 12:04:37 GMT  
		Size: 86.4 KB (86397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccc12d34ee1496a677496fb2a132e19f51bec955dbb5deb594179e53cd344070`  
		Last Modified: Fri, 01 Dec 2023 12:04:37 GMT  
		Size: 18.5 KB (18460 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer` - linux; s390x

```console
$ docker pull notary@sha256:23b5119f61f785a5bc3d0e08d81069495e7b7812a69f15f6894ff355737dee38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2769d25e3c0fd0dd829d59aeff8c1f0a3ebe2a1bc017678473a5f6f4f3d5df`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:f7a7034bb4c8ab0fed6e2c4b09f15f3e7076270496340adceac7e01aabf87857 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:3710549eb8868990a62c8d4471b58594422f5b4b00b9f1301ab37536932fc449`  
		Last Modified: Thu, 30 Nov 2023 22:43:07 GMT  
		Size: 2.6 MB (2592110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3051463e76e45694bdac001475d6401201e997fcc6b1064dd5714221e9522`  
		Last Modified: Fri, 01 Dec 2023 11:05:17 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ca950734db4b88a8271bdb375716842b44f57947be9a32ce1832cc959ce05d`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720d0e7d288849a47e06194310df9a8c2bd5638f0c5cce65be749c4da7e6fbf3`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 4.6 MB (4606704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9556c8fc916d6d56403f96617359720b8239dceec8ae11ca4e259228c84f7f1`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0921e503e64d527f3a5b47ee31cc425598e2d4e5f4b074d69210fa19e9f5dbd`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:c84dbdb9b42aafc6e1def960ec053709e57577b1eb06ea6cdb66da0e94acc640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 KB (104799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c89d20e11e1a8b94999e93299a89fb110480ceecf6ed20bcaba85641e50c0ca`

```dockerfile
```

-	Layers:
	-	`sha256:0f50abc9fa459207c91633f207420e89dee36d1dec0d0a16ee61f045320df614`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 86.4 KB (86375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3029f7c5714f65e0d9cb914f5bbd69e4a57ef31e8cfa027d7de49000dc85b32`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json

## `notary:signer-0.7.0`

```console
$ docker pull notary@sha256:7fc172c063a6ed68134432c1db849dfda2a191a61d9b7a43d14f6aacba51d0cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `notary:signer-0.7.0` - linux; amd64

```console
$ docker pull notary@sha256:a5f3cf14ec1f9dbe64f5038168764468bf8cf36023f8c1d763abd3bcbe2a5952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7572933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61447c100d57a41cd6d7de0b918e258904d083cab09c7b290a8e5cddf1a383a4`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0a66a0a7b087da7f9fa9bcdc96d80ae3321e565fc4a638465abdeb792ea1ab`  
		Last Modified: Fri, 01 Dec 2023 00:11:09 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f52aecd80f774b20144d76df7a1bd30afde4c022a082345e77412724e5de78d`  
		Last Modified: Fri, 01 Dec 2023 00:11:09 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8e5637f614944c20b445d103b62cbf9d5075cffbc97f04ac7e7934dccdcfde`  
		Last Modified: Fri, 01 Dec 2023 00:11:09 GMT  
		Size: 4.8 MB (4763081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6da303ea01f1dcceeed1c542f07d37db7d2365b66f40e36af725411bb4f125`  
		Last Modified: Fri, 01 Dec 2023 00:11:10 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b01e3f98461ce88ec08bac5847e6bee5cab2727f844407e5ffb58c77e9a1ac6`  
		Last Modified: Fri, 01 Dec 2023 00:11:10 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:9346c6fe8bf3d29a34e0e1d10f1730feff4461a2e4e2cec704a90490be890d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 KB (107256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64d8edc2c7e9d523a11d6b1ea4764f09f5f5fc6fe7551968068c4294c1c0f48`

```dockerfile
```

-	Layers:
	-	`sha256:f05c794c11c4670ee3b2bf18f481970753817e33407b854e72b92746a6734dee`  
		Last Modified: Fri, 01 Dec 2023 00:11:09 GMT  
		Size: 88.0 KB (88011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:080d7a72705ea449c50069d2ca075026c7cfb046eed5d6d3923af5215bc7dbca`  
		Last Modified: Fri, 01 Dec 2023 00:11:09 GMT  
		Size: 19.2 KB (19245 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:65861e496c2a89861f24aae1e230413422204f5d85529405e213e137c03ddf53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25fc96cf0be3836d3e800e2e675a5fa860ab4ac12bed105b2de1d2099dcf6dbb`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cde69ed9ff455c9499e13b92a67b8722a1710401c31263561cf43c64193c3d80 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:b76d44755a1732ac572a54d4df4cfff9671b9466b719f4c80a81fd9397dbc3dc`  
		Last Modified: Thu, 30 Nov 2023 22:50:02 GMT  
		Size: 2.6 MB (2615844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f45e9feb3ba2edfc080d49db4581485558c6233268178d4453fe2a8325279b`  
		Last Modified: Fri, 01 Dec 2023 12:31:22 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f02f663975232742358fed9118fd56abed084a8b0350c9dd332e90c9becea4`  
		Last Modified: Fri, 01 Dec 2023 12:31:42 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03397ec88fc769559ee4b471e98c53345450eea8a2f0ac146b93cf38b9f3b6cf`  
		Last Modified: Fri, 01 Dec 2023 12:31:43 GMT  
		Size: 4.5 MB (4526083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22e564c80a0e1d630759a8adf2715c6f3e9eea6922d07743cbfca49340c8688`  
		Last Modified: Fri, 01 Dec 2023 12:31:42 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c311966ad150702a111c2fbfb2141efab1f7b273d7d218d95ac68c55dc840b`  
		Last Modified: Fri, 01 Dec 2023 12:31:42 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:d0b2157e191e4ba482b1840f736d0d5f8e03e69cd939e2997b53bf9bb70cb016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7103175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69eec41fd3d6cf59d8bb581a10497f7417bffab2b543059ee887a590df99b84`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202c4dd0f102d31afdf745598c8b608887eb3b4142b5fbb8619d8b431ab3d348`  
		Last Modified: Mon, 07 Aug 2023 22:45:27 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f88739c04bec4884bc40c7d216e4e9211441e2d033c5861f631bb0925b478fa`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 118.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f13b4a5fcaf14870b0afd1801c5ea0380125660000fd5e65bc19c7ae8dee6d`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 4.4 MB (4393084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b200dfa82abb58b4aa87e1cda3b731e8020c5ca1217d041b2c3c0284514c9c4`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da7244fcfdb45e21dcac9ea3d397ec3d43317799fbc86f16ec39bc6827ade69`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:244799276b035bce3224f3f79c4b7b9e0aded1870794878003a52a9d8cf3781a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 KB (106071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afda2c6f5dcb6f88ab10fcb1bcd90bd754e6d4d6b6edb0dfa41e75749e23832c`

```dockerfile
```

-	Layers:
	-	`sha256:7c9c855ac1ab70995fcbf9fe9684adc44c7aa1c882133bf2d8dc85721cb2d860`  
		Last Modified: Tue, 17 Oct 2023 19:00:44 GMT  
		Size: 87.6 KB (87640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdca200e6121df920c204dc77a79b981b9384195ab438933a829f9c1d6ab18ca`  
		Last Modified: Tue, 17 Oct 2023 19:00:45 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; 386

```console
$ docker pull notary@sha256:c3c9cfa8a3e89ea14663516300287f199daaed5aef0c6a0063ba451673d9c085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d486e4ae2bb3d2cab2dde433f02130da8ae238b161d56700c17325b5e77093`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:c06b4f6991638e506d4d0a4d70c4a78ba30b971767802af4c6b837cdf59d4303 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:be0d19c155de823c6b37eaaba7cdec9085e8f1e39b1dd5982a19acb6c8c97cc5`  
		Last Modified: Mon, 07 Aug 2023 19:39:20 GMT  
		Size: 2.8 MB (2810553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596da12c2e0de93c921f09f80dc157315fd51dc526c26c681e009068df5568c8`  
		Last Modified: Tue, 17 Oct 2023 18:59:50 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bb43db3153fdcdf459b45889c76eeaca751b5a0febc7091e481cba1037f6eb`  
		Last Modified: Tue, 17 Oct 2023 18:59:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b757696a027c52ff6a4f41267a37af932d79007fe75adef68a03e4db29cab75b`  
		Last Modified: Tue, 17 Oct 2023 18:59:50 GMT  
		Size: 4.6 MB (4579028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9801338c9c3995199351989ccf7a80c57e88a1a2ba79e8b71870abe62355662c`  
		Last Modified: Tue, 17 Oct 2023 18:59:50 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e6f75c5fee4e0b872d36961655c4e8103de49fe771f2390af597ea1dc591bf`  
		Last Modified: Tue, 17 Oct 2023 18:59:50 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:2a7832d044b996c0336436dcdb25e356d5267cb1be5438344c16b4f1368a55a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2c1e17b9b29692bdea190cc1626243bc46b522299047c6b7ec5a764c5f987e`

```dockerfile
```

-	Layers:
	-	`sha256:eae9624154b2c579a780e1c33f1d0df3e69761a24ad7d3414c420d01c825a058`  
		Last Modified: Tue, 17 Oct 2023 18:59:50 GMT  
		Size: 19.0 KB (19002 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:8eb5fb1e9d7895f95d2c6485df3c1d62ae867114699be79bf388b931c587865d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7101990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc77dc06e2f6fd97a37ffd4c11036a2d71048ba31e0f8bcbc8306a3e0b39a44`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:41dd492ac8086a6a7ae54f70f208d397f81d19c9ada61f7e52b1f678c0e08ae3 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:ae6fb3870f7991147b39ddb2fee9e659464482f341bd584e2b45ba18fbe5b39d`  
		Last Modified: Thu, 30 Nov 2023 23:20:26 GMT  
		Size: 2.8 MB (2802949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bfd048ed14aaf67fd63563fa3533db27519d50152d35a987605aea84e79d96`  
		Last Modified: Fri, 01 Dec 2023 12:03:35 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9421ec33edc3cb3d38249f1ba62d9fa1f6baae3d87de84d82a4657879b79bc10`  
		Last Modified: Fri, 01 Dec 2023 12:04:37 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800ce24dc1465688b4bef5c02eb0c0c0b42e23f89b86abdc4cc5ca9a0fda4f54`  
		Last Modified: Fri, 01 Dec 2023 12:04:38 GMT  
		Size: 4.3 MB (4296972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2decdf73454ce64d52b01b21838de42d299e8cb05629b8f17f4954025e8164`  
		Last Modified: Fri, 01 Dec 2023 12:04:37 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9887737212ebd2747b8706ac29a46ca6ea9f12d9335e5a88c10d41439e5fab43`  
		Last Modified: Fri, 01 Dec 2023 12:04:37 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:d777a1b17cf821e4518af7210ec644a565bb09521fc8fed18cbb00b146457adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 KB (104857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6d08dc0a6a1b5a92a376fdb0dde82d83399fbe8e6169a69699872414eeb10c`

```dockerfile
```

-	Layers:
	-	`sha256:2c2659606c62b1e9915fe53cfb8c14bf6aee517c8fe16d376a3b1a5935f78e80`  
		Last Modified: Fri, 01 Dec 2023 12:04:37 GMT  
		Size: 86.4 KB (86397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccc12d34ee1496a677496fb2a132e19f51bec955dbb5deb594179e53cd344070`  
		Last Modified: Fri, 01 Dec 2023 12:04:37 GMT  
		Size: 18.5 KB (18460 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:23b5119f61f785a5bc3d0e08d81069495e7b7812a69f15f6894ff355737dee38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2769d25e3c0fd0dd829d59aeff8c1f0a3ebe2a1bc017678473a5f6f4f3d5df`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:f7a7034bb4c8ab0fed6e2c4b09f15f3e7076270496340adceac7e01aabf87857 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:3710549eb8868990a62c8d4471b58594422f5b4b00b9f1301ab37536932fc449`  
		Last Modified: Thu, 30 Nov 2023 22:43:07 GMT  
		Size: 2.6 MB (2592110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3051463e76e45694bdac001475d6401201e997fcc6b1064dd5714221e9522`  
		Last Modified: Fri, 01 Dec 2023 11:05:17 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ca950734db4b88a8271bdb375716842b44f57947be9a32ce1832cc959ce05d`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720d0e7d288849a47e06194310df9a8c2bd5638f0c5cce65be749c4da7e6fbf3`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 4.6 MB (4606704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9556c8fc916d6d56403f96617359720b8239dceec8ae11ca4e259228c84f7f1`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0921e503e64d527f3a5b47ee31cc425598e2d4e5f4b074d69210fa19e9f5dbd`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:c84dbdb9b42aafc6e1def960ec053709e57577b1eb06ea6cdb66da0e94acc640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 KB (104799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c89d20e11e1a8b94999e93299a89fb110480ceecf6ed20bcaba85641e50c0ca`

```dockerfile
```

-	Layers:
	-	`sha256:0f50abc9fa459207c91633f207420e89dee36d1dec0d0a16ee61f045320df614`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 86.4 KB (86375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3029f7c5714f65e0d9cb914f5bbd69e4a57ef31e8cfa027d7de49000dc85b32`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
