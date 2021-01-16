## `openjdk:17-ea-5-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:b4dbcc3d756001a61ddc704536fb2207545fc5e1336e4bb2a7a8cfff7086f408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:17-ea-5-jdk-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:08d3a08b2270d37eb295c02a90cacff51e9436e0a3baef7775fe1dff5dbda038
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2631395878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83e9b2bba7cfd7f4b15230fc13ed3aaa7da087333cc870dc21d121fcd211458`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 19:49:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 13 Jan 2021 19:49:02 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 13 Jan 2021 19:49:25 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Fri, 15 Jan 2021 23:15:17 GMT
ENV JAVA_VERSION=17-ea+5
# Fri, 15 Jan 2021 23:15:18 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/5/GPL/openjdk-17-ea+5_windows-x64_bin.zip
# Fri, 15 Jan 2021 23:15:19 GMT
ENV JAVA_SHA256=93c1db93cef5471684276f5fc2870bdcc616d7aca274eab6737d8f133a5330af
# Fri, 15 Jan 2021 23:17:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 15 Jan 2021 23:17:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095bdf2ec48c97c5c3f23fd49bb117d66d72f8b46f5707f3c1b77227c6ca013e`  
		Last Modified: Wed, 13 Jan 2021 21:11:37 GMT  
		Size: 9.4 MB (9362296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec8ba32ad11b92749181d846d26ac913a25bbb39776d6faab16181b6f9a347`  
		Last Modified: Wed, 13 Jan 2021 21:11:32 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b643c361856e1ee8e404e05d6b434af548c27323c5c644e6f21820ba4f0d86`  
		Last Modified: Wed, 13 Jan 2021 21:11:32 GMT  
		Size: 297.9 KB (297887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc69e47e3a0e6d8bcd560fd49f0bab4d69b744b97b9bb9d692f27281d9d1a77`  
		Last Modified: Fri, 15 Jan 2021 23:34:52 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95998987c74bcc1433af9d7cf06d40b5f7b8324b52f3b757df6e2918ba4bbd33`  
		Last Modified: Fri, 15 Jan 2021 23:34:53 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d50027130a481d7c7a2b9fa8bf45832417fc9ca4bb1240a9890a6922c65d49c`  
		Last Modified: Fri, 15 Jan 2021 23:34:52 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f876b4c06c85367fdccf100e775f35dc310d2d74ca326c52e8d64f2657d2852`  
		Last Modified: Fri, 15 Jan 2021 23:35:13 GMT  
		Size: 186.0 MB (185955866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5554c91b2473c9395c0ca61868dc9d06800ef50a570b9ceba1de6c1df6b798c7`  
		Last Modified: Fri, 15 Jan 2021 23:34:52 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
