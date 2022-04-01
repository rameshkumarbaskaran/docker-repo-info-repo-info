<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-5.7.0.15`](#aerospikece-57015)
-	[`aerospike:ee-5.7.0.15`](#aerospikeee-57015)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:ce-5.7.0.15`

```console
$ docker pull aerospike@sha256:f1fbfd8788f840fc10805690bd1352b4a99acbc4c6d113912357b4211dcf56a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-5.7.0.15` - linux; amd64

```console
$ docker pull aerospike@sha256:c8a0acee44234768775bce42956e8d5d0f3c7fdb03bb873e1637dd7804d0c325
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81556878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2730ea08ed20fdb6ce7dbd3cc77450902e718b8f490be6db72b9b06c8b924e9d`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Fri, 01 Apr 2022 01:19:22 GMT
ENV AEROSPIKE_VERSION=5.7.0.15
# Fri, 01 Apr 2022 01:19:51 GMT
ENV AEROSPIKE_SHA256=4f639cae83b7c9066b1049567a1b90af76b63075e63697e953b2c74b312e4118
# Fri, 01 Apr 2022 01:20:10 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Fri, 01 Apr 2022 01:20:10 GMT
COPY file:1897c4aae07efbc61bf2d8c2c7b0dfb0990174e11cc787eac71d5adf767abaed in /etc/aerospike/aerospike.template.conf 
# Fri, 01 Apr 2022 01:20:10 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Fri, 01 Apr 2022 01:20:10 GMT
EXPOSE 3000 3001 3002
# Fri, 01 Apr 2022 01:20:10 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Fri, 01 Apr 2022 01:20:10 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28871b1a140aea647f735c13d0ba187cd3cbc6dc1746f77e892cbf86798eb4b`  
		Last Modified: Fri, 01 Apr 2022 01:20:46 GMT  
		Size: 54.4 MB (54402887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8997501762d27731168bc7b811178bcd263f8b4323e30e3e2d4aef8adc9874eb`  
		Last Modified: Fri, 01 Apr 2022 01:20:38 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882ec391dc9b1c8247c6ff70db5a40488fc282bfaeab26054589e2dcbfe5582d`  
		Last Modified: Fri, 01 Apr 2022 01:20:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:ee-5.7.0.15`

```console
$ docker pull aerospike@sha256:a87c120ada760b7d01f66e532ac984fa4af407186afdf0e602489373fb0d3b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-5.7.0.15` - linux; amd64

```console
$ docker pull aerospike@sha256:9bac9685c99b187856b94c3b5cee6a8921ee77d5b8d01f95ed763524bed60b49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83924537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0c18bffa22592aaa6ad730678572c04eb4d438e9490400f554ba10e8f99234`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Fri, 01 Apr 2022 01:19:22 GMT
ENV AEROSPIKE_VERSION=5.7.0.15
# Fri, 01 Apr 2022 01:19:22 GMT
ENV AEROSPIKE_SHA256=9b8bec8e189f02fc7b47c22d2f5f2c5cffe24b888ba147ec3d79aab665fc2274
# Fri, 01 Apr 2022 01:19:23 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Fri, 01 Apr 2022 01:19:47 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static -O /usr/bin/as-tini-static   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://download.aerospike.com/artifacts/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Fri, 01 Apr 2022 01:19:48 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Fri, 01 Apr 2022 01:19:48 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Fri, 01 Apr 2022 01:19:48 GMT
EXPOSE 3000 3001 3002
# Fri, 01 Apr 2022 01:19:48 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 01 Apr 2022 01:19:48 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03df0aef996c0bb0dd3a74fc7840bd41e0335101d621dffa957682f0cc389e92`  
		Last Modified: Fri, 01 Apr 2022 01:20:29 GMT  
		Size: 56.8 MB (56770488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32518a0f7fac1446d8fadf5fe90c13cc78ba18bca437fdb5abbdb7b7578a7c5`  
		Last Modified: Fri, 01 Apr 2022 01:20:20 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552df95ba6aa172611757da65d846a0b1874723d7def7c75f7cef82bf0bc3f94`  
		Last Modified: Fri, 01 Apr 2022 01:20:21 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:a87c120ada760b7d01f66e532ac984fa4af407186afdf0e602489373fb0d3b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:9bac9685c99b187856b94c3b5cee6a8921ee77d5b8d01f95ed763524bed60b49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83924537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0c18bffa22592aaa6ad730678572c04eb4d438e9490400f554ba10e8f99234`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Fri, 01 Apr 2022 01:19:22 GMT
ENV AEROSPIKE_VERSION=5.7.0.15
# Fri, 01 Apr 2022 01:19:22 GMT
ENV AEROSPIKE_SHA256=9b8bec8e189f02fc7b47c22d2f5f2c5cffe24b888ba147ec3d79aab665fc2274
# Fri, 01 Apr 2022 01:19:23 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Fri, 01 Apr 2022 01:19:47 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static -O /usr/bin/as-tini-static   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://download.aerospike.com/artifacts/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Fri, 01 Apr 2022 01:19:48 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Fri, 01 Apr 2022 01:19:48 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Fri, 01 Apr 2022 01:19:48 GMT
EXPOSE 3000 3001 3002
# Fri, 01 Apr 2022 01:19:48 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 01 Apr 2022 01:19:48 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03df0aef996c0bb0dd3a74fc7840bd41e0335101d621dffa957682f0cc389e92`  
		Last Modified: Fri, 01 Apr 2022 01:20:29 GMT  
		Size: 56.8 MB (56770488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32518a0f7fac1446d8fadf5fe90c13cc78ba18bca437fdb5abbdb7b7578a7c5`  
		Last Modified: Fri, 01 Apr 2022 01:20:20 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552df95ba6aa172611757da65d846a0b1874723d7def7c75f7cef82bf0bc3f94`  
		Last Modified: Fri, 01 Apr 2022 01:20:21 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
