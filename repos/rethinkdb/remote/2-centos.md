## `rethinkdb:2-centos`

```console
$ docker pull rethinkdb@sha256:97945571d761d1c6d13ed1c5b19c431829a165eae8979e95a43146244044296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:62b8895efb80423198ab0f72f481d21cbd46359abc1486702be4ba1d56a25a7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97244258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e1670ba60391d24a97d5a7b3e70a9c18ecb8683cd690ebe8ca6ec2898591b3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 17 Jun 2020 00:22:24 GMT
ADD file:84700c11fcc969ac08ef25f115513d76c7b72a4118c01fbc86ef0a6056fdebeb in / 
# Wed, 17 Jun 2020 00:22:25 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200611
# Wed, 17 Jun 2020 00:22:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 00:45:00 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0
# Wed, 17 Jun 2020 00:45:00 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Wed, 17 Jun 2020 00:45:12 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Wed, 17 Jun 2020 00:45:12 GMT
VOLUME [/data]
# Wed, 17 Jun 2020 00:45:12 GMT
WORKDIR /data
# Wed, 17 Jun 2020 00:45:12 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 17 Jun 2020 00:45:12 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6910e5a164f725142d77994b247ba20040477fbab49a721bdbe8d61cf855ac23`  
		Last Modified: Wed, 17 Jun 2020 00:23:52 GMT  
		Size: 74.9 MB (74866818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d202930a85138a93b068d1eccecb1b05af9be3ebf00c897408f75ca8e1d94d`  
		Last Modified: Wed, 17 Jun 2020 00:45:30 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c34589253a77f1123f119cd191e186943036825f376131178d3e138511acb0`  
		Last Modified: Wed, 17 Jun 2020 00:45:35 GMT  
		Size: 22.4 MB (22377081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc88e46cf376b3042a553f6853b4d0d091ef6fb76fef0d1d9d64ffec7da7a81`  
		Last Modified: Wed, 17 Jun 2020 00:45:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
