## `aerospike:ce-6.0.0.4`

```console
$ docker pull aerospike@sha256:cef02d007b97485a35bc90a4cfac8de000d00ba7258a13dfac6624b4a1bc0996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-6.0.0.4` - linux; amd64

```console
$ docker pull aerospike@sha256:1333133949da491a76acd5368af52476421af2036b146b1a2f2f761c6b5798c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101872581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a740008180046068da7bfd0eb80071db45ca9006e0324dfeaf7d7aa13cd1ff1`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Sat, 20 Aug 2022 00:19:21 GMT
ENV AEROSPIKE_VERSION=6.0.0.4
# Sat, 20 Aug 2022 00:19:49 GMT
ENV AEROSPIKE_SHA256=df05478abc56add36a14c9fbed315d35a641061295493d26cc98a5637ba23d4b
# Sat, 20 Aug 2022 00:20:10 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && if [ -d '/opt/aerospike/bin/asadm' ];   then   mv /opt/aerospike/bin/asadm /usr/lib/;   ln -s /usr/lib/asadm/asadm /usr/bin/asadm;   fi   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Sat, 20 Aug 2022 00:20:11 GMT
COPY file:f497c4c6974a190f79a562efd9c9c0d6b753efe43e62c3fcc2536f74ad08238d in /etc/aerospike/aerospike.template.conf 
# Sat, 20 Aug 2022 00:20:11 GMT
COPY file:fe302e12e47afe1731a34ed4ed29328c6901a3f2c9e32e307220e65cb76d53a2 in /entrypoint.sh 
# Sat, 20 Aug 2022 00:20:11 GMT
EXPOSE 3000 3001 3002
# Sat, 20 Aug 2022 00:20:11 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Sat, 20 Aug 2022 00:20:11 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622caf3a89688ed83a07fd31b9e3d365db86ec139dc55477421589e5620511a4`  
		Last Modified: Sat, 20 Aug 2022 00:20:52 GMT  
		Size: 74.7 MB (74730672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbdf70980907f91facd62c4272946a16e5f24a80fa6372075d30f8a8efa3c27`  
		Last Modified: Sat, 20 Aug 2022 00:20:41 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41df754a4cb106ea64ebf21db355f8634998ebe655d6ca305c63d1ff55057604`  
		Last Modified: Sat, 20 Aug 2022 00:20:41 GMT  
		Size: 808.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
