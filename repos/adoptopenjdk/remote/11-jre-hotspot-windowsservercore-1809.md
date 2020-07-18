## `adoptopenjdk:11-jre-hotspot-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:0aa0dd1df9184f279b8ccf40375568d693f46ad0ecf6ef4ac73e7d4e5e582e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `adoptopenjdk:11-jre-hotspot-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull adoptopenjdk@sha256:0ae37187c5fa44a72ea1c12b4b566a91cceac6c054d0e2ddb93a509e2ca9f501
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2390719103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37b7adb919e769b51534c81366bc161fc607e6401bf42f5afe722da123cecb1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jul 2020 22:55:17 GMT
ENV JAVA_VERSION=jdk-11.0.8+10
# Fri, 17 Jul 2020 23:11:58 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.8_10.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.8_10.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (c94202eec5a406bf86352270cb0c9c17cb6c3ffc9c7d78c41e67b181e1d6f151) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c94202eec5a406bf86352270cb0c9c17cb6c3ffc9c7d78c41e67b181e1d6f151') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7b66bdcf6a1deae29e3dc95b56af1ccb3e91839b7945590251ac670c897a80`  
		Last Modified: Sat, 18 Jul 2020 01:14:47 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dbc7b9bf5f64d30b8589497d08d6296b1576783e5f0b87bfe39ee387c786f8`  
		Last Modified: Sat, 18 Jul 2020 01:15:44 GMT  
		Size: 80.5 MB (80524555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
