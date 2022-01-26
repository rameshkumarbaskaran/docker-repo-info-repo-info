## `aerospike:ce-5.7.0.10`

```console
$ docker pull aerospike@sha256:754fd65f6772a3cef6e2d4d70d6e55f8e7315fe232f60d7070a6dac110c8ed3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-5.7.0.10` - linux; amd64

```console
$ docker pull aerospike@sha256:bf04bebe2405fe339909742ea7a8bca22fe7855e06cdbddabc4cb5fbb22a215f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81534485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e751bd0dc2bcd09c43358b0a3db02a6083218d2021a5de835347df7ff3507599`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:08:18 GMT
ENV AEROSPIKE_VERSION=5.7.0.10
# Wed, 26 Jan 2022 02:08:46 GMT
ENV AEROSPIKE_SHA256=6c17caabf03094c284c28406145447165ce7c40b954427879b8bd38d2824902b
# Wed, 26 Jan 2022 02:09:06 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Wed, 26 Jan 2022 02:09:07 GMT
COPY file:1897c4aae07efbc61bf2d8c2c7b0dfb0990174e11cc787eac71d5adf767abaed in /etc/aerospike/aerospike.template.conf 
# Wed, 26 Jan 2022 02:09:07 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Wed, 26 Jan 2022 02:09:07 GMT
EXPOSE 3000 3001 3002
# Wed, 26 Jan 2022 02:09:07 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Wed, 26 Jan 2022 02:09:07 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67d56a8ca0aa7e6731a821eb2387b507f85b38b6fbdd1b918658f7152509c54`  
		Last Modified: Wed, 26 Jan 2022 02:09:41 GMT  
		Size: 54.4 MB (54378734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccb0b93e5299a5e142ea8d43901f9e078fa9703f5a44f8cd14e8cf24c30256c`  
		Last Modified: Wed, 26 Jan 2022 02:09:33 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f35ee9ec59d18f540ce725fb908721cb9702939a69494aa94b571db886a702`  
		Last Modified: Wed, 26 Jan 2022 02:09:33 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
