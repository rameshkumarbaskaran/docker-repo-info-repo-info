## `openjdk:22-ea-1-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:d4dbc98e9566d3759e9c376f86fa21aa46ad4d7e8ea0dd0e9049b310c47b0134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `openjdk:22-ea-1-windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull openjdk@sha256:a24aae6e3af81ef86fbeef4d55177e4dddb7fc66f3d42d0a925c6eb55c8f6fa7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1850286177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18288c2bfff12e1d9ecbd4a1d7bbcfcf17ae121461b9deef1818d3947a4d7f23`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 17:39:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jun 2023 20:26:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Jun 2023 20:26:18 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 14 Jun 2023 20:26:44 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 14 Jun 2023 20:26:44 GMT
ENV JAVA_VERSION=22-ea+1
# Wed, 14 Jun 2023 20:26:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_windows-x64_bin.zip
# Wed, 14 Jun 2023 20:26:46 GMT
ENV JAVA_SHA256=9348aa2fc8344b25baad9b614627983b4e900ab0293ecfa3ec7f9b5d911a90a7
# Wed, 14 Jun 2023 20:27:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 Jun 2023 20:27:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b712a9a082fd391beaa9ca7c8e6c3fda37b0ad8d29cc4663173ed973b961d342`  
		Last Modified: Wed, 14 Jun 2023 18:21:55 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1119c9dd4674cbb889b8cd01bbadf4652797b89d882f89be398f7da1beb24c70`  
		Last Modified: Wed, 14 Jun 2023 20:34:37 GMT  
		Size: 305.5 KB (305458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9ed58112430e156afd8c7eed20069147a2b5ecdb1b8da57264db5ea41dd214`  
		Last Modified: Wed, 14 Jun 2023 20:34:37 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e32d8326ab7a8f29c3209f83dfd8c39f6746f5de5efc42d984740194104030`  
		Last Modified: Wed, 14 Jun 2023 20:34:37 GMT  
		Size: 257.0 KB (257037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc1374ca12e0f000e82e2c894369b4e5e40f31d10eaa40bb2a3d8446328acbb`  
		Last Modified: Wed, 14 Jun 2023 20:34:35 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6fbe1cd76c2f5dd51ebc428cc6b545e292acb0da970dc61e818251ad4597af`  
		Last Modified: Wed, 14 Jun 2023 20:34:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acd07a56ff8bc06dd0656094b648e16a36377c6b575ac138a348390321d43f7`  
		Last Modified: Wed, 14 Jun 2023 20:34:35 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8a0ecc3119375481c9b19f2fc68f892dbbdb642f07f5a96a644b838f83dacb`  
		Last Modified: Wed, 14 Jun 2023 20:34:54 GMT  
		Size: 199.1 MB (199095484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac6df817569d846654eac06b7496a3be7a51b5c988f0d971780e6cd73b77c82`  
		Last Modified: Wed, 14 Jun 2023 20:34:35 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
