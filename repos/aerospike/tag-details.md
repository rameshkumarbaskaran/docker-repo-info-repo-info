<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-5.7.0.11`](#aerospikece-57011)
-	[`aerospike:ee-5.7.0.11`](#aerospikeee-57011)

## `aerospike:ce-5.7.0.11`

```console
$ docker pull aerospike@sha256:b2d4c90a87261c6fe782360bec820f6b90b7f22533d1aa8430ca3f4d1ebf5d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-5.7.0.11` - linux; amd64

```console
$ docker pull aerospike@sha256:c47788c218b005938b412fc259337241a1cb5960fd60ec49dcba68078842f6a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81536275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c134699fbec9ccff960b601ea2d886f8389da8a9d7b98ea925da3364c088a352`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:25:25 GMT
ENV AEROSPIKE_VERSION=5.7.0.11
# Fri, 18 Mar 2022 06:25:53 GMT
ENV AEROSPIKE_SHA256=bd0d9962c8d068270746833df313d32117ef9e9c3e2367f8ac6902cf97d66142
# Fri, 18 Mar 2022 06:26:12 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Fri, 18 Mar 2022 06:26:13 GMT
COPY file:1897c4aae07efbc61bf2d8c2c7b0dfb0990174e11cc787eac71d5adf767abaed in /etc/aerospike/aerospike.template.conf 
# Fri, 18 Mar 2022 06:26:13 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Fri, 18 Mar 2022 06:26:13 GMT
EXPOSE 3000 3001 3002
# Fri, 18 Mar 2022 06:26:13 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Fri, 18 Mar 2022 06:26:13 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f342b2351b9b57710bb425a764682ac3a1c63b960b73f21f487a75360d6fa4d`  
		Last Modified: Fri, 18 Mar 2022 06:26:50 GMT  
		Size: 54.4 MB (54380425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f6aef3a1b41a85ad7a066dac631a878d0e2771ca18aa47c57ae01f7abf3f33`  
		Last Modified: Fri, 18 Mar 2022 06:26:39 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23df580e5e040a4afc2563a8dda503b064f2551e540495ad502db626affe4bf`  
		Last Modified: Fri, 18 Mar 2022 06:26:39 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:ee-5.7.0.11`

```console
$ docker pull aerospike@sha256:01afcbf0ce3d10bcce62ae66f8a13265b475be2d2ee8598d2d7bb4d8620e4ce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-5.7.0.11` - linux; amd64

```console
$ docker pull aerospike@sha256:967f277692d2c26e6f4a389140e6867bdf0e89b43d36d20b66d520fb0f9c29e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83905763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74dd0f4e603b4795489601af5087e33f01735fc9a029089704568824ee6906c`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:25:25 GMT
ENV AEROSPIKE_VERSION=5.7.0.11
# Fri, 18 Mar 2022 06:25:25 GMT
ENV AEROSPIKE_SHA256=f43f38680e39429976ef359f7b72034f8c1a9bf624d94826d61b898212e91766
# Fri, 18 Mar 2022 06:25:25 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Fri, 18 Mar 2022 06:25:46 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static -O /usr/bin/as-tini-static   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://download.aerospike.com/artifacts/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Fri, 18 Mar 2022 06:25:47 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Fri, 18 Mar 2022 06:25:47 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Fri, 18 Mar 2022 06:25:47 GMT
EXPOSE 3000 3001 3002
# Fri, 18 Mar 2022 06:25:47 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 18 Mar 2022 06:25:47 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7d64383b3538ec8df7a1d82386b1e208c27264a9668291e62a78c7481ad5cf`  
		Last Modified: Fri, 18 Mar 2022 06:26:32 GMT  
		Size: 56.7 MB (56749856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f023894d132198017382eaecd5193f1edb1c03ea07e93a456ebc5cea4dfdc340`  
		Last Modified: Fri, 18 Mar 2022 06:26:23 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0203fc13f97b7d220abfe54d1057f12e4011258166417ca778755ccbb19f7a`  
		Last Modified: Fri, 18 Mar 2022 06:26:23 GMT  
		Size: 907.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
