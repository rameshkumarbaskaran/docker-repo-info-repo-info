## `kong:centos`

```console
$ docker pull kong@sha256:cf0db57a429d75d14999631ca5ad7e8aba99074f35c8a2485c24ebccb4958904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:centos` - linux; amd64

```console
$ docker pull kong@sha256:043ee61b7269a392c48ed05afbda8657a732043e51555afe2ac555c5aa5b4476
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158442645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21f6b284f01143bf3d326e78ffc3531ea53f2a7e5fab166077537a57896dcc6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:32:03 GMT
LABEL maintainer=Kong Core Team <team-core@konghq.com>
# Wed, 08 Apr 2020 21:29:04 GMT
ENV KONG_VERSION=2.0.3
# Wed, 08 Apr 2020 21:29:10 GMT
RUN yum install -y -q unzip 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki
# Wed, 08 Apr 2020 21:29:26 GMT
RUN useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm 	&& yum clean all 	&& chown -R kong:0 /usr/local/kong 	&& chmod -R g=u /usr/local/kong
# Wed, 08 Apr 2020 21:29:27 GMT
USER kong
# Wed, 08 Apr 2020 21:29:27 GMT
COPY file:d4cc11e4d968fd7df92b7b157746b27dc40d08cd20ca769e15cffc687cea9b5c in /docker-entrypoint.sh 
# Wed, 08 Apr 2020 21:29:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Apr 2020 21:29:27 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 08 Apr 2020 21:29:28 GMT
STOPSIGNAL SIGQUIT
# Wed, 08 Apr 2020 21:29:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118a283d15f0b8d28c667ecaef11f9bcc20eb99542c2ac4f45189d8f715999df`  
		Last Modified: Wed, 08 Apr 2020 21:31:06 GMT  
		Size: 6.6 MB (6569066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ef44249d4c775f4d4c1c347cab01973bee052579c36db601bcbd7fa8eaba28`  
		Last Modified: Wed, 08 Apr 2020 21:31:19 GMT  
		Size: 76.1 MB (76092511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ebd767dcb9e711030da712324b59839e3602a4e6a4812d4dd4dfcf07f1ca4f`  
		Last Modified: Wed, 08 Apr 2020 21:31:04 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
