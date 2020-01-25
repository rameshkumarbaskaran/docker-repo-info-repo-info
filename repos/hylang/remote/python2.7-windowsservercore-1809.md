## `hylang:python2.7-windowsservercore-1809`

```console
$ docker pull hylang@sha256:2cb6d067480d48a2f6cbc923b9a73eb82212e54eb67120fedcef569fa9ed95e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `hylang:python2.7-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull hylang@sha256:c0bbe5de2c4e0b6473aacb762a6854bff826f94776edb4b3baa83462acb9b5ec
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2266212392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7b8f725cd746b783327307121f8d9ecf21b7fbeae29e39df9a1c949f6cc5ca`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 18:31:45 GMT
ENV PYTHON_VERSION=2.7.17
# Wed, 15 Jan 2020 18:31:46 GMT
ENV PYTHON_RELEASE=2.7.17
# Wed, 15 Jan 2020 18:33:53 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.msi'; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		Write-Host 'Complete.'
# Sat, 25 Jan 2020 02:37:32 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Sat, 25 Jan 2020 02:37:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/42ad3426cb1ef05863521d7988d5f7fec0c99560/get-pip.py
# Sat, 25 Jan 2020 02:37:34 GMT
ENV PYTHON_GET_PIP_SHA256=da288fc002d0bb2b90f6fbabc91048c1fa18d567ad067ee713c6e331d3a32b45
# Sat, 25 Jan 2020 02:38:41 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Sat, 25 Jan 2020 03:09:25 GMT
RUN pip install --no-cache-dir virtualenv
# Sat, 25 Jan 2020 03:09:26 GMT
CMD ["python"]
# Sat, 25 Jan 2020 05:08:35 GMT
ENV HY_VERSION=0.17.0
# Sat, 25 Jan 2020 05:09:13 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Sat, 25 Jan 2020 05:09:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991e8bf1fe43fb6d1b926596157fec820f98e6bf95f7d87c5037c6a9d454ee94`  
		Last Modified: Wed, 15 Jan 2020 18:44:46 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3061269fafccc2b8dbc758f49ebd8556e388f724ca6c14b7274e2c96eeb5b9`  
		Last Modified: Wed, 15 Jan 2020 18:44:44 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8b29109525c4a2b28a2790a4cf8dcf3e323f9aabee0ae266fe15eef2b42f3`  
		Last Modified: Wed, 15 Jan 2020 18:45:09 GMT  
		Size: 38.9 MB (38905595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0e5fda0c747525ba40ec1c573ec1e5934fff585ed19dfc67ce12dbcf92052b`  
		Last Modified: Sat, 25 Jan 2020 03:15:13 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bbb854dec21f961df73f2402085f5bea98ed0e3cdcec5ac44687f7cc7c2ee7`  
		Last Modified: Sat, 25 Jan 2020 03:15:10 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f23d1e3d3795183b8141f5cd28cb356e068526bf22c8380c85c040b033bfe9`  
		Last Modified: Sat, 25 Jan 2020 03:15:10 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fae694a7c55b8173fdd0e4d1a924e70a24569784203e75509a40fb7368cf60c`  
		Last Modified: Sat, 25 Jan 2020 03:15:19 GMT  
		Size: 5.0 MB (5027134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a87fd11bf2629990c053534f2d718d0e21a2f3aa4dedf04d394db32b5cdf5ed`  
		Last Modified: Sat, 25 Jan 2020 03:15:12 GMT  
		Size: 3.8 MB (3777129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48a219c2b4da5e4d514c8a35456a50f174f86c682d139ea4b3a54b9b4b875d2`  
		Last Modified: Sat, 25 Jan 2020 03:15:10 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af74aa7646556f0f81bbf985a57d29b43380720aa8f7811ff81031609d9b4de`  
		Last Modified: Sat, 25 Jan 2020 05:14:24 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01480112fa5b459600906f5a326e910e736d965f38cc31dc965474c6ff5703b`  
		Last Modified: Sat, 25 Jan 2020 05:14:25 GMT  
		Size: 1.1 MB (1080621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881383fb05ded092f593698e232c979018e0fe45506be9bf0630aa9b36fd0731`  
		Last Modified: Sat, 25 Jan 2020 05:14:24 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
