## `aerospike:ee-6.0.0.2`

```console
$ docker pull aerospike@sha256:343ee698cf8ce53a7cac34c8d78c7245eccc362c864cce18e58cf7ee534ada5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-6.0.0.2` - linux; amd64

```console
$ docker pull aerospike@sha256:1f351c71e0e6255303d0893ead2182f159d30c8b5000223239a055c14cd978ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103320079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05fcfc2633fc683b1b0b55e3524dda46fbd30771fcfd6fee660630f68761852b`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Wed, 06 Jul 2022 18:19:22 GMT
ENV AEROSPIKE_VERSION=6.0.0.2
# Wed, 06 Jul 2022 18:19:22 GMT
ENV AEROSPIKE_SHA256=0b067053c3919cc41b90f519e4ea164ad1ed4d8bca934a877085ff0067469a65
# Wed, 06 Jul 2022 18:19:22 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Wed, 06 Jul 2022 18:19:44 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static -O /usr/bin/as-tini-static   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://download.aerospike.com/artifacts/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Wed, 06 Jul 2022 18:19:45 GMT
COPY file:f56e2e33c0b4bb66affff75053eaed44661e723b8b33d3ef3c10e305b506c350 in /etc/aerospike/aerospike.template.conf 
# Wed, 06 Jul 2022 18:19:46 GMT
COPY file:697e2123680798e87da7a3f98d1d70e76ffec66f0e1aafa90ff25047a11cca52 in /entrypoint.sh 
# Wed, 06 Jul 2022 18:19:46 GMT
EXPOSE 3000 3001 3002
# Wed, 06 Jul 2022 18:19:46 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 06 Jul 2022 18:19:46 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56235a48bfc7617a30baed3e2bd8c0431033da7d30654e52e50a87fe7281ee1f`  
		Last Modified: Wed, 06 Jul 2022 18:20:29 GMT  
		Size: 76.2 MB (76178150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a53eb249bfb02d41ae06eb53a5db60d2a885cb76d63b84c1ffb1dd59617d3f3`  
		Last Modified: Wed, 06 Jul 2022 18:20:20 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e875588bc5d9dd59cab1f17a14d2b7b00c84ace1684c1c7853b828d8a288f05`  
		Last Modified: Wed, 06 Jul 2022 18:20:20 GMT  
		Size: 840.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
