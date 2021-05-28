<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-5.6.0.4`](#aerospikece-5604)
-	[`aerospike:ee-5.6.0.4`](#aerospikeee-5604)

## `aerospike:ce-5.6.0.4`

```console
$ docker pull aerospike@sha256:618ae4442618a737d366005a50e5c77126b7de0c2050e6416403404c4ca0739d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:ce-5.6.0.4` - linux; amd64

```console
$ docker pull aerospike@sha256:769e76961b64df95f6e44d4090a22cd2d228dc007d11524dbdfc50cc3e16aefb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80604737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e7dafec0369d583d475358eac3e86b2c3bc6dad9eba58a5d6982206ee09381`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Thu, 27 May 2021 19:19:20 GMT
ENV AEROSPIKE_VERSION=5.6.0.4
# Thu, 27 May 2021 19:19:45 GMT
ENV AEROSPIKE_SHA256=1717dc48edf3c7b8595c7ee12580fdfab382ac1c0af86c7f9d95fbf0037b99dd
# Thu, 27 May 2021 19:20:04 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Thu, 27 May 2021 19:20:05 GMT
COPY file:1897c4aae07efbc61bf2d8c2c7b0dfb0990174e11cc787eac71d5adf767abaed in /etc/aerospike/aerospike.template.conf 
# Thu, 27 May 2021 19:20:05 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Thu, 27 May 2021 19:20:05 GMT
EXPOSE 3000 3001 3002
# Thu, 27 May 2021 19:20:06 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Thu, 27 May 2021 19:20:06 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26fa4a54a730f13b753f9f76c20d381562cf63f7b83cdeae6e3c8fa8278bdb0`  
		Last Modified: Thu, 27 May 2021 19:20:41 GMT  
		Size: 53.5 MB (53456801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028b791d4b33f9816085b1c350166687ac6ccfa7e59bd4cd86a5351651ba84bc`  
		Last Modified: Thu, 27 May 2021 19:20:33 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba36893349920ca7237c3a590d553116941cf33e783c9660dd4521a653fb4774`  
		Last Modified: Thu, 27 May 2021 19:20:33 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:ee-5.6.0.4`

```console
$ docker pull aerospike@sha256:0727af3ba17fcdcb2df56e7f6ba0cb81c4c37324fb9d2913c26fa0dfda440b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:ee-5.6.0.4` - linux; amd64

```console
$ docker pull aerospike@sha256:d5aa45a678db2753365ac5e05b5dde3c8a1351d876fbd1923632bf3de05085a3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82469106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b984b00dae6d333e98f923f03ebd244326c9f2a6ce8ce4f0793c365a4dd5d1cc`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Thu, 27 May 2021 19:19:20 GMT
ENV AEROSPIKE_VERSION=5.6.0.4
# Thu, 27 May 2021 19:19:20 GMT
ENV AEROSPIKE_SHA256=cb98684e30b5e55071c03f0c3eda460941c2fede645b93834e3060ea8a1899cd
# Thu, 27 May 2021 19:19:41 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget "https://www.aerospike.com/enterprise/download/server/${AEROSPIKE_VERSION}/artifact/debian10" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Thu, 27 May 2021 19:19:42 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Thu, 27 May 2021 19:19:42 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Thu, 27 May 2021 19:19:42 GMT
EXPOSE 3000 3001 3002
# Thu, 27 May 2021 19:19:42 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Thu, 27 May 2021 19:19:43 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba65d0edc785f30d76319d9a0c88aa1e09b012dec63166afcbeb65b6651db2d`  
		Last Modified: Thu, 27 May 2021 19:20:25 GMT  
		Size: 55.3 MB (55321109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e4c56dc9bb6b696518797dbf146f218347907f8583b7d42b75b065e3b6fad3`  
		Last Modified: Thu, 27 May 2021 19:20:16 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd7be73785483f0d582cc05478c4fda3ad21583fade5e8ae48f5fcb3c310820`  
		Last Modified: Thu, 27 May 2021 19:20:16 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
