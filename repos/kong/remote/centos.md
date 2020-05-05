## `kong:centos`

```console
$ docker pull kong@sha256:4e50333aadd8af20ffbacc6717d0b1a20e0e9efd23b9c7a0c076093baa38acd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:centos` - linux; amd64

```console
$ docker pull kong@sha256:7f849d88afd2e5cc6b12f6e6fae15ece9b027898d4dc87f6d9e0e1225041bffe
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125691825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a348f9e6180508b9a93712f13cad0dfcfc217dd37578530c93a570ab917ae0e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2020 00:21:02 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:21:02 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:21:02 GMT
ENV ASSET=ce
# Tue, 05 May 2020 00:21:02 GMT
COPY file:73044b225363e2703a176f55b132687ead4bab30398788756be18d2965fac2cd in /tmp/kong.rpm 
# Tue, 05 May 2020 00:21:02 GMT
ARG KONG_VERSION=2.0.4
# Tue, 05 May 2020 00:21:02 GMT
ENV KONG_VERSION=2.0.4
# Tue, 05 May 2020 00:21:03 GMT
ARG KONG_SHA256=16a934a7bc2e182f00f03bd75b67f4bdb483150b3820d33cab9b0c95539dd353
# Tue, 05 May 2020 00:21:03 GMT
ENV KONG_SHA256=16a934a7bc2e182f00f03bd75b67f4bdb483150b3820d33cab9b0c95539dd353
# Tue, 05 May 2020 00:21:24 GMT
RUN set -ex;     if [ "$ASSET" = "local" ] ; then exit 0 ;     elif [ "$ASSET" = "ce" ] ; then         curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm &&         echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;     fi;     yum install -y -q unzip shadow-utils 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong
# Tue, 05 May 2020 00:21:25 GMT
COPY file:c7c95ad9b95e03a404039e7ee878ca4bb52cbcb965cd2d12c91037eb7a3b7e65 in /docker-entrypoint.sh 
# Tue, 05 May 2020 00:21:25 GMT
USER kong
# Tue, 05 May 2020 00:21:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 May 2020 00:21:25 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 May 2020 00:21:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 May 2020 00:21:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdba7a3eeb67aa32a478b8587e94773a03b9f71661c2d3689e1bece702e9681d`  
		Last Modified: Tue, 05 May 2020 00:23:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cbd6c9798cbab0bae2f5c225583f0e67bc6b2a0273496b1656cf5f1c8e6ac3`  
		Last Modified: Tue, 05 May 2020 00:23:29 GMT  
		Size: 49.9 MB (49910303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e830d35be6457e6e536335a5903c5c2cadd1188b50a3d89192c15ea3402f15`  
		Last Modified: Tue, 05 May 2020 00:23:19 GMT  
		Size: 682.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
