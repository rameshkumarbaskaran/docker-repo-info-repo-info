<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:4.7.0.13`](#aerospike47013)
-	[`aerospike:4.8.0.9`](#aerospike4809)
-	[`aerospike:4.9.0.5`](#aerospike4905)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:4.7.0.13`

```console
$ docker pull aerospike@sha256:1dbff02d08f4332b9be08e3630c16835c76467c8289970070bcce788dd6f8d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.7.0.13` - linux; amd64

```console
$ docker pull aerospike@sha256:522ace0049a268fa237a4958b44050887ea8d54ebf49806070a4c0fcfd0b84e8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51769375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7448a20eaf20298a425a19962a729069d2b815155adccd656ea48de4405cafb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:15:06 GMT
ENV AEROSPIKE_VERSION=4.7.0.13
# Thu, 23 Apr 2020 01:15:06 GMT
ENV AEROSPIKE_SHA256=05585d9f2e9e2e066d6fc2845bd83f764b104e84140b614b53fb71309e47695a
# Thu, 23 Apr 2020 01:15:25 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 23 Apr 2020 01:15:25 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 23 Apr 2020 01:15:25 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 23 Apr 2020 01:15:26 GMT
VOLUME [/opt/aerospike/data]
# Thu, 23 Apr 2020 01:15:26 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 23 Apr 2020 01:15:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 01:15:26 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aac6c5e43f0669be065797cc30ed546d867948a391d078190114bf2955a0318`  
		Last Modified: Thu, 23 Apr 2020 01:16:32 GMT  
		Size: 29.3 MB (29253833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee2300393abd474f5d7cae15724519608bd51c097cbedcb5130ac1dd640d69a`  
		Last Modified: Thu, 23 Apr 2020 01:16:26 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b03a8b2895423ef9a4dc595ab35578919e5645cd7e2421338f47330c4fa4630`  
		Last Modified: Thu, 23 Apr 2020 01:16:26 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.8.0.9`

```console
$ docker pull aerospike@sha256:a5bb8463394bcc27b19f95844bf8a6d8c970760708f7f107ff72944e6276d075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.8.0.9` - linux; amd64

```console
$ docker pull aerospike@sha256:c01fb84f08c3c9a507fff3fa661f390c94d8f86336f572c17c4df9b31a718591
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51846382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f908a1da20e847eeb6b59f928f24ba545e32b6a1af85b374e95af8fff909ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:15:31 GMT
ENV AEROSPIKE_VERSION=4.8.0.9
# Thu, 23 Apr 2020 01:15:31 GMT
ENV AEROSPIKE_SHA256=3af1b8c97d73d05054582c8941d435bea55b7ead9b04d2df42f1e9990ab7e0c3
# Thu, 23 Apr 2020 01:15:51 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 23 Apr 2020 01:15:51 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 23 Apr 2020 01:15:51 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 23 Apr 2020 01:15:51 GMT
VOLUME [/opt/aerospike/data]
# Thu, 23 Apr 2020 01:15:52 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 23 Apr 2020 01:15:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 01:15:52 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b95509a7f0fc5b582e7d87f298856cf31059edae80759712db40637ffd2d5d`  
		Last Modified: Thu, 23 Apr 2020 01:16:42 GMT  
		Size: 29.3 MB (29330839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e220000b1588e7a447b9c8cc061d836295c6658654aa6a7e4b6b950fcf11c8`  
		Last Modified: Thu, 23 Apr 2020 01:16:36 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b848d6168d2b03ef1995f9e1a8f8976ac50f3e231401f39ccaac03ea4ebfd74`  
		Last Modified: Thu, 23 Apr 2020 01:16:36 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.9.0.5`

```console
$ docker pull aerospike@sha256:8fa8e3f89b2ee72a7e1dc94d1df3d8f47bfdd7406d6a6be833d5e48fd60fefee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.9.0.5` - linux; amd64

```console
$ docker pull aerospike@sha256:19238b71f6d3abf64150f797a7ca1dc143e8bdad7ab885c5410eacef43f3c623
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53185991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded20b514848377f4988ef3294e74260c2f5a8ce14f3c0543e92204b388aa7ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:15:56 GMT
ENV AEROSPIKE_VERSION=4.9.0.5
# Thu, 23 Apr 2020 01:15:56 GMT
ENV AEROSPIKE_SHA256=7e9b345020e987d1a4d1c91034a8054c97fd80a0c917a8da04d4aad9127e8fe2
# Thu, 23 Apr 2020 01:16:15 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 23 Apr 2020 01:16:15 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 23 Apr 2020 01:16:16 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 23 Apr 2020 01:16:16 GMT
VOLUME [/opt/aerospike/data]
# Thu, 23 Apr 2020 01:16:16 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 23 Apr 2020 01:16:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 01:16:17 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c533c0c0e6a1d1eba72005e4498c1a0b315a851ce9ad958f06aaa9052bd2a8a2`  
		Last Modified: Thu, 23 Apr 2020 01:16:52 GMT  
		Size: 30.7 MB (30670450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e965ecf97b6ad45e3609bc928013aced0aae19a27131fd3d4f71086d031f8c5`  
		Last Modified: Thu, 23 Apr 2020 01:16:46 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bcd5b23cbd12c670a5723a3c7398fda706f249d69973e4e72fa2764e2c028c5`  
		Last Modified: Thu, 23 Apr 2020 01:16:46 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:8fa8e3f89b2ee72a7e1dc94d1df3d8f47bfdd7406d6a6be833d5e48fd60fefee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:19238b71f6d3abf64150f797a7ca1dc143e8bdad7ab885c5410eacef43f3c623
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53185991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded20b514848377f4988ef3294e74260c2f5a8ce14f3c0543e92204b388aa7ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:15:56 GMT
ENV AEROSPIKE_VERSION=4.9.0.5
# Thu, 23 Apr 2020 01:15:56 GMT
ENV AEROSPIKE_SHA256=7e9b345020e987d1a4d1c91034a8054c97fd80a0c917a8da04d4aad9127e8fe2
# Thu, 23 Apr 2020 01:16:15 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 23 Apr 2020 01:16:15 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 23 Apr 2020 01:16:16 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 23 Apr 2020 01:16:16 GMT
VOLUME [/opt/aerospike/data]
# Thu, 23 Apr 2020 01:16:16 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 23 Apr 2020 01:16:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 01:16:17 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c533c0c0e6a1d1eba72005e4498c1a0b315a851ce9ad958f06aaa9052bd2a8a2`  
		Last Modified: Thu, 23 Apr 2020 01:16:52 GMT  
		Size: 30.7 MB (30670450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e965ecf97b6ad45e3609bc928013aced0aae19a27131fd3d4f71086d031f8c5`  
		Last Modified: Thu, 23 Apr 2020 01:16:46 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bcd5b23cbd12c670a5723a3c7398fda706f249d69973e4e72fa2764e2c028c5`  
		Last Modified: Thu, 23 Apr 2020 01:16:46 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
