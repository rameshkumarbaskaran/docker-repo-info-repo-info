## `aerospike:ce-5.7.0.17`

```console
$ docker pull aerospike@sha256:dddaeeebc242bd167a896de131b5ae4bf62143eedda155ee9548b77a81569e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-5.7.0.17` - linux; amd64

```console
$ docker pull aerospike@sha256:da6f28ba86e2b90e97d24dc43ced94e9f1c7d6158c501c81404f4f0bdf88acb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81545717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9425b22a566104f682d1bff18dd0b1927d2d9bafc3458a38db14007028c9d882`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Sat, 23 Apr 2022 01:19:10 GMT
ENV AEROSPIKE_VERSION=5.7.0.17
# Sat, 23 Apr 2022 01:19:38 GMT
ENV AEROSPIKE_SHA256=9bee7924812060fae4cf6971adbc7b3b9db34ac221bb992f6469cdfe20086390
# Sat, 23 Apr 2022 01:19:56 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Sat, 23 Apr 2022 01:19:57 GMT
COPY file:57aa54f8d05380c639ff298f99e0387bafe493553aa29e39911c8342f60a0f0e in /etc/aerospike/aerospike.template.conf 
# Sat, 23 Apr 2022 01:19:57 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Sat, 23 Apr 2022 01:19:57 GMT
EXPOSE 3000 3001 3002
# Sat, 23 Apr 2022 01:19:57 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Sat, 23 Apr 2022 01:19:57 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2629617b4a6b780c6bcf19f25d00b153b4d48fe21af21dcd01ebce10f76c541d`  
		Last Modified: Sat, 23 Apr 2022 01:20:30 GMT  
		Size: 54.4 MB (54403021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3de73af68f7b950a1cfb149475ab6a4af8be9ea0f6bbb545468de15fb572946`  
		Last Modified: Sat, 23 Apr 2022 01:20:22 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a760a021b8b3dd1eabe1425cf7847c276e59fadd0790b3fc1b2144ad344d89c`  
		Last Modified: Sat, 23 Apr 2022 01:20:22 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
