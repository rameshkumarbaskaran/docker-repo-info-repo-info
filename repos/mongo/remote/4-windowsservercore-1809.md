## `mongo:4-windowsservercore-1809`

```console
$ docker pull mongo@sha256:3760b4636a1facf31ee5a8cf73757c81f15d0d15d3c3530dc168d267e5dc45c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `mongo:4-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull mongo@sha256:d0a998df8bd714db63dcd38e12bba37eb4d6e281d5e7f16e89aac6ad25c57d26
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3079228812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951bf43f87235d72989d8fd3ddc80817c3b1b691a42533ec1c69f0d932b9c903`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Oct 2020 23:30:18 GMT
ENV MONGO_VERSION=4.4.1
# Wed, 14 Oct 2020 23:30:19 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.1-signed.msi
# Wed, 14 Oct 2020 23:30:19 GMT
ENV MONGO_DOWNLOAD_SHA256=acc93c7d8b8c3c8994940bdf2640215a5d3114ca7838be3cfc2d5887e170eaf7
# Wed, 14 Oct 2020 23:54:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 23:54:44 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Oct 2020 23:54:45 GMT
EXPOSE 27017
# Wed, 14 Oct 2020 23:54:46 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d839ec6fa74e5e869036dfd823e95452a7afcde18ac997af483c88c21b92ad8c`  
		Last Modified: Wed, 14 Oct 2020 16:02:33 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0b4737f5628d77546cd22e42fff6102588058d57db3b8f71e4e4157f05b9d7`  
		Last Modified: Thu, 15 Oct 2020 00:16:22 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbb2fe0a5f6df487cb4bcf6c7edafebbb216e4ff41bd7f8eac4ce0361dac300`  
		Last Modified: Thu, 15 Oct 2020 00:16:22 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf695c22f4dd601a38456e9a527e4296f6e9fe7c3618a3d0f0da34aa115fb0d`  
		Last Modified: Thu, 15 Oct 2020 00:16:19 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550fffcfd01f6bebe3f3eda02990390cd3e4814280eac84678c3c339c267f864`  
		Last Modified: Thu, 15 Oct 2020 00:17:52 GMT  
		Size: 705.1 MB (705130619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aecaa26887a358f05e28f52c3781de5fbd461e697f839ccd89dc1c4d1921ae1e`  
		Last Modified: Thu, 15 Oct 2020 00:16:19 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69325529ffc44c2568687ff278eae0b4286afd7eddd66d74807bf70b0ab6c1d6`  
		Last Modified: Thu, 15 Oct 2020 00:16:18 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf56ed5c8e00d8b2c16053c180898e549cea8ff477434539ea7366da23ffbfd7`  
		Last Modified: Thu, 15 Oct 2020 00:16:18 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
