## `kong:latest`

```console
$ docker pull kong@sha256:39b9d3226a26daa2eba233c8d6096b59f8f26c1bbc0595a44dabea00a6c01a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:40fa6b31f86ff5759b0b21083393cc57676a831b94b57cc16e48015188ecfe69
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49298472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abec1dd8af91867d1d02f6ef349df6b95137e20202a42c83512da12f8cafb4a8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:21:07 GMT
LABEL maintainer=Kong Core Team <team-core@konghq.com>
# Mon, 09 Mar 2020 23:24:37 GMT
ENV KONG_VERSION=2.0.2
# Mon, 09 Mar 2020 23:24:37 GMT
ENV KONG_SHA256=befe736bfde51e27ae51a0d6a827df44a1669099dea459d430aef0d570cc4db7
# Mon, 09 Mar 2020 23:24:48 GMT
RUN adduser -S kong 	&& mkdir -p "/usr/local/kong" 	&& apk add --no-cache --virtual .build-deps curl wget tar ca-certificates 	&& apk add --no-cache libgcc openssl pcre perl tzdata libcap su-exec zip 	&& wget -O kong.tar.gz "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" 	&& echo "$KONG_SHA256 *kong.tar.gz" | sha256sum -c - 	&& tar -xzf kong.tar.gz -C /tmp 	&& rm -f kong.tar.gz 	&& cp -R /tmp/usr / 	&& rm -rf /tmp/usr 	&& cp -R /tmp/etc / 	&& rm -rf /tmp/etc 	&& chown -R kong:0 /usr/local/kong 	&& chmod -R g=u /usr/local/kong
# Mon, 09 Mar 2020 23:24:48 GMT
USER kong
# Mon, 09 Mar 2020 23:24:48 GMT
COPY file:d4cc11e4d968fd7df92b7b157746b27dc40d08cd20ca769e15cffc687cea9b5c in /docker-entrypoint.sh 
# Mon, 09 Mar 2020 23:24:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 09 Mar 2020 23:24:49 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 09 Mar 2020 23:24:49 GMT
STOPSIGNAL SIGQUIT
# Mon, 09 Mar 2020 23:24:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f12465f7519d6534a30402d7d4cdee33191f606b3354f8d2a9b184ff6c81211`  
		Last Modified: Mon, 09 Mar 2020 23:27:57 GMT  
		Size: 46.5 MB (46511154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0844b942a3e9c7ebf29943dbea5cbac25eebea10df1b6322394e59111468d48a`  
		Last Modified: Mon, 09 Mar 2020 23:27:13 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
