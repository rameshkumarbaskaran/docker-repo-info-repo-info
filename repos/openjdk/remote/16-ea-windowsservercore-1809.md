## `openjdk:16-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:f16523932ede84db0b189fa77c9d152b43cb5b10279b7e65be9a87225ec29909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `openjdk:16-ea-windowsservercore-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull openjdk@sha256:06b1384bd9673413ebfa427149e508adc1a1086f1327549353c9f8a7c1ac8ded
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2542264509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fda89b21c7e48129ea4dd0f14ecd5007c8b77a7d44d2f7741dbb94d8bc3d58`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Tue, 11 Aug 2020 20:36:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 15:20:31 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 12 Aug 2020 15:20:32 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 12 Aug 2020 15:20:53 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 27 Aug 2020 22:14:17 GMT
ENV JAVA_VERSION=16-ea+13
# Thu, 27 Aug 2020 22:14:18 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/13/GPL/openjdk-16-ea+13_windows-x64_bin.zip
# Thu, 27 Aug 2020 22:14:19 GMT
ENV JAVA_SHA256=054db7127dd6aaf511122fb635ed2d0c77aab20ce9cfe6c6c0b0a89910d354bc
# Thu, 27 Aug 2020 22:15:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 27 Aug 2020 22:15:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43065500f09f35124a5d71517aa493fd23ad75660682600f7f6b40aa7629ac78`  
		Last Modified: Tue, 11 Aug 2020 20:54:54 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61325951c8c59861a712789969f747b1171e1a463d838cc58ec539e09209ac0e`  
		Last Modified: Wed, 12 Aug 2020 16:08:33 GMT  
		Size: 9.1 MB (9149173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b85fd778f4a6d3cd93553accf4bfc8b282ee060683d4289cdb4def2dd78a15`  
		Last Modified: Wed, 12 Aug 2020 16:08:31 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ec4e041da1cd72477b2a3db3cfa7c178f24e8fda9bd70cee26c9db8c5e5cd7`  
		Last Modified: Wed, 12 Aug 2020 16:08:29 GMT  
		Size: 300.5 KB (300490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ab39b50296f58bf4d829b4c51c498599a8ab6312beeb93c1e082dbae1ee7c5`  
		Last Modified: Thu, 27 Aug 2020 22:24:00 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5406eb0e76d114ed5e79048dc087531f3931c65912d8f6b8768ded94fc5e002`  
		Last Modified: Thu, 27 Aug 2020 22:24:00 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29557148806a3d1c322dcfcdc394256da4c43c0fa01d71fd121e8925f308ce38`  
		Last Modified: Thu, 27 Aug 2020 22:24:00 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fd8188d22655972f3cc19191501a89796bbb1d50389638a550e4eaf1506977`  
		Last Modified: Thu, 27 Aug 2020 22:24:20 GMT  
		Size: 196.9 MB (196941085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ea2ede2e8fcc77fc2f82b5e31557c45837a784acaf144dbf165dc303a25805`  
		Last Modified: Thu, 27 Aug 2020 22:24:00 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
