## `mongo:4-windowsservercore`

```console
$ docker pull mongo@sha256:6f2d25c1e6919c56d0aaf2d34225cb78e808ecc5f6db981682b76e0257710e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64
	-	windows version 10.0.17763.1518; amd64

### `mongo:4-windowsservercore` - windows version 10.0.14393.3986; amd64

```console
$ docker pull mongo@sha256:1dd546361f77eb8e7add09ad376572f138d4928b152fa33098262ccffbce9305
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6447235149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58751b43871a3ba3d8f4449821816c25fae30517db0323c0e497e1f50969d09d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 13:36:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Oct 2020 23:06:10 GMT
ENV MONGO_VERSION=4.4.1
# Wed, 14 Oct 2020 23:06:11 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.1-signed.msi
# Wed, 14 Oct 2020 23:06:11 GMT
ENV MONGO_DOWNLOAD_SHA256=acc93c7d8b8c3c8994940bdf2640215a5d3114ca7838be3cfc2d5887e170eaf7
# Wed, 14 Oct 2020 23:30:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 23:30:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Oct 2020 23:30:08 GMT
EXPOSE 27017
# Wed, 14 Oct 2020 23:30:08 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb0caa156c690c0274404e38041b8eb56dcd2c15edbc269fc4c619eb667cb7ff`  
		Last Modified: Wed, 14 Oct 2020 16:03:09 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d82d55566630be2206fc89c5a8a58abc8887a755bbe8a1f3cfca8b9b8790a62`  
		Last Modified: Thu, 15 Oct 2020 00:13:32 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c9a9026666eb071d35afe08062e002582b8ba37b0573078951837233df2fea`  
		Last Modified: Thu, 15 Oct 2020 00:13:32 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35e9d77f7f27428f29c5583bd1ec619369565b03fb8e071e6b2e2d94fe6278b`  
		Last Modified: Thu, 15 Oct 2020 00:13:29 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0447804488e15b2ba36c71bd59f88190e4960966ba7bd8012d1840b333c356`  
		Last Modified: Thu, 15 Oct 2020 00:15:55 GMT  
		Size: 705.9 MB (705875387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c5c2936a4b14e29c72129212ccc2b0389b86d1c702f47629ede9a2c7a04632`  
		Last Modified: Thu, 15 Oct 2020 00:13:28 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ff9ba19d615b3a9fe5ef346edd7be50810afd1794027387a44cc2d83fc8f91`  
		Last Modified: Thu, 15 Oct 2020 00:13:28 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b83b9e052228772e5c03f7579b5f6e6b5de87baeffd0643edfec9bf650db9c`  
		Last Modified: Thu, 15 Oct 2020 00:13:28 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-windowsservercore` - windows version 10.0.17763.1518; amd64

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
