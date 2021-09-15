## `openjdk:8u302-jre-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:00b25114119d54277d2137d28b2a2806b9c0a4d6b264e1dce176b03ef6c8a8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4651; amd64

### `openjdk:8u302-jre-windowsservercore-ltsc2016` - windows version 10.0.14393.4651; amd64

```console
$ docker pull openjdk@sha256:c4e285fb36121cc76928d7a414c207a7e42dfcd4d0f13f4bdd8e4a4469843df6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6310561125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6790fa214102ade7499f018478159204c9d97d2b9abefd630504cbe68272384e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 13 Sep 2021 01:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Sep 2021 00:34:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Sep 2021 00:35:51 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 15 Sep 2021 01:01:17 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Sep 2021 01:02:14 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 15 Sep 2021 01:02:14 GMT
ENV JAVA_VERSION=8u302
# Wed, 15 Sep 2021 01:05:38 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_windows_8u302b08.zip
# Wed, 15 Sep 2021 01:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9b8281bf21e46c781fb54e4f15f5728e2c44dea4219c9e6deeb732f1d909d3b`  
		Size: 2.2 GB (2201342322 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8721f004192f15fe71b8626ef3f3e34cbf2cfe1d15a63b6b544ab946162ef707`  
		Last Modified: Wed, 15 Sep 2021 01:10:18 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b794d0a07a41196dae8678e4ecbb9a5766d6db31f9729bfe3f1d83963af3e0`  
		Last Modified: Wed, 15 Sep 2021 01:10:18 GMT  
		Size: 339.2 KB (339172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c1f344e0222373968e87d0c3fbe3d9a5aed9d026ee90d28e8eab0fdf9a3144`  
		Last Modified: Wed, 15 Sep 2021 01:27:13 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae30094a4b1b2f3f76d86ef0aa8a23200a08d345879a9a5c5a7664b1d79a1e9`  
		Last Modified: Wed, 15 Sep 2021 01:27:13 GMT  
		Size: 328.7 KB (328675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995f2a34e252d4ec7fc3d8ded958122942d4d83b2e1e018821b5be28d9cda692`  
		Last Modified: Wed, 15 Sep 2021 01:27:13 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91577608c3de1594346d0f0c6cfb1239910e0629818406e884e8601dfd22b08`  
		Last Modified: Wed, 15 Sep 2021 01:28:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4743e953dd269817e80a1bb22819948ceca4d47111d4268895fc070ff7f7321a`  
		Last Modified: Wed, 15 Sep 2021 01:29:00 GMT  
		Size: 38.6 MB (38559610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
