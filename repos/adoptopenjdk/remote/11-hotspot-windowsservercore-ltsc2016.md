## `adoptopenjdk:11-hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:805649fa0c869cf6233ba8f2baa5ac21a94a45917c7d0c67fb176577a9d46ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `adoptopenjdk:11-hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull adoptopenjdk@sha256:ff11d1f9015485b8105db78bc8d6ee9cab5654b77fe19ae6608e04e8faaba1fa
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6102974790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402eab0782e75ec98a481771f0a4be14ecc9bc6a772897f714bd4df7c838836c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 00:35:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 20:33:36 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Wed, 11 Dec 2019 20:36:58 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_x64_windows_hotspot_11.0.5_10.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_x64_windows_hotspot_11.0.5_10.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (692b95374e860daac705ae6c1c351d07a6f5105a1909de68680d556db4f4f426) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '692b95374e860daac705ae6c1c351d07a6f5105a1909de68680d556db4f4f426') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 11 Dec 2019 20:37:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:530e4240d4261ce165890648d1df6230dc4f9ce5df2e6cf9f0d5876694c3d4f0`  
		Last Modified: Wed, 11 Dec 2019 01:14:39 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cdabb8bd4292a6e5eb846dd0b34a08d0aff7cc337d6e216c2c49086b684b52`  
		Last Modified: Wed, 11 Dec 2019 22:15:22 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fb2d928990baa4398fa734ec3c2c56860ec3aa23d7dafeba677350fc46aa9e`  
		Last Modified: Wed, 11 Dec 2019 22:16:05 GMT  
		Size: 380.3 MB (380267301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f3b52c107d198cd7d6211abb79a95fed1f78f6d9b7f8924c217734103af06b`  
		Last Modified: Wed, 11 Dec 2019 22:15:21 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
