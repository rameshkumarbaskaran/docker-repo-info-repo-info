## `aerospike:ce-6.0.0.2`

```console
$ docker pull aerospike@sha256:7d02766fad19b16050c3bdae6a4a4da4b56460a2ba93e2e7bc76c75418c1718a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-6.0.0.2` - linux; amd64

```console
$ docker pull aerospike@sha256:90804c114d898ade501663a06ba0620b8bd9dd2319d5b80d8d7948b5ae7e0513
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100927489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b498e4572705802f84b46e8f0b10ce3841f9ccdb1e4d9d1b95a344b1a312206`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Wed, 06 Jul 2022 18:19:22 GMT
ENV AEROSPIKE_VERSION=6.0.0.2
# Wed, 06 Jul 2022 18:19:50 GMT
ENV AEROSPIKE_SHA256=c521897b21909dde726e067f5164a6397177feb84ae52712e224f2b694dbf7ad
# Wed, 06 Jul 2022 18:20:10 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Wed, 06 Jul 2022 18:20:11 GMT
COPY file:f497c4c6974a190f79a562efd9c9c0d6b753efe43e62c3fcc2536f74ad08238d in /etc/aerospike/aerospike.template.conf 
# Wed, 06 Jul 2022 18:20:11 GMT
COPY file:fe302e12e47afe1731a34ed4ed29328c6901a3f2c9e32e307220e65cb76d53a2 in /entrypoint.sh 
# Wed, 06 Jul 2022 18:20:11 GMT
EXPOSE 3000 3001 3002
# Wed, 06 Jul 2022 18:20:11 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Wed, 06 Jul 2022 18:20:11 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4294aae62e2c8d7aa5288485c0e7cca0d6375118851147dc194d3e491455bb0`  
		Last Modified: Wed, 06 Jul 2022 18:20:47 GMT  
		Size: 73.8 MB (73785616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6012cf92fe1eaa4e21ad12b41a9a3a0c1a0ec2e0746652fb849f870a7da19dd3`  
		Last Modified: Wed, 06 Jul 2022 18:20:37 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3436da10b84a58fe5dc04277dd6bc7a2b1b6e8d3a786f45fa33ce7ee2a1e20d6`  
		Last Modified: Wed, 06 Jul 2022 18:20:37 GMT  
		Size: 811.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
