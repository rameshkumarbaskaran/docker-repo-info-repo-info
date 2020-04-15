## `hylang:0-windowsservercore-1809`

```console
$ docker pull hylang@sha256:d69449de88d23b9be7865813468db4a991051d3955eb8c0bcf5c2ad85e2b754a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `hylang:0-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull hylang@sha256:7b5ad1c9ebe70cd4f0569d34c1f3dd56226baa6a4cb70c46d2179ff7c06d7e2f
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329148567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc5a27f00385397601f33b9ea934d850f324bc2eafad391daeff4882277f2dd`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 17:09:34 GMT
ENV PYTHON_VERSION=3.8.2
# Wed, 15 Apr 2020 17:09:35 GMT
ENV PYTHON_RELEASE=3.8.2
# Wed, 15 Apr 2020 17:11:09 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 15 Apr 2020 17:11:10 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Wed, 15 Apr 2020 17:11:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Wed, 15 Apr 2020 17:11:12 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Wed, 15 Apr 2020 17:11:54 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 15 Apr 2020 17:11:55 GMT
CMD ["python"]
# Wed, 15 Apr 2020 21:21:54 GMT
ENV HY_VERSION=0.18.0
# Wed, 15 Apr 2020 21:22:29 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 15 Apr 2020 21:22:30 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4e7a2aa0041fb0d3fd445d94b23e74c4b82e87ff351bf7c7a0623bf86fbb6a`  
		Last Modified: Wed, 15 Apr 2020 17:27:43 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc455b671c7b32826cea9a056b9b63db72fc9930059fbd66323b9d9c35137d0`  
		Last Modified: Wed, 15 Apr 2020 17:27:43 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eaf71d1f72cf92fdb574a3146158813ebe0d4b1cd6995c8249ff10244491ad4`  
		Last Modified: Wed, 15 Apr 2020 17:27:50 GMT  
		Size: 51.9 MB (51935318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacff642707504c64da98f96c0a657fe0a36f26330c2eb3bd1bed7bbd6ccafde`  
		Last Modified: Wed, 15 Apr 2020 17:27:40 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c53d8554a2d0fdc1be46cdf4d7f572a9b5b8bddff635f964164d63ae59bc386`  
		Last Modified: Wed, 15 Apr 2020 17:27:41 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1a2a7c7ea0e978d570a03989d13ed344a8a8dee3dc2ec158f3e0ee4f77276d`  
		Last Modified: Wed, 15 Apr 2020 17:27:40 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8594da5592d408429c58bf21eed9d2e5c69ac4e6ae81dde9029d96e67ce776cd`  
		Last Modified: Wed, 15 Apr 2020 17:27:42 GMT  
		Size: 5.4 MB (5363639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae2ccad6deb41902c81fda06e9d471dc0ccdb5dad832ebaf32b03937c0e63c7`  
		Last Modified: Wed, 15 Apr 2020 17:27:41 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdbdc8b7d1adeb0da9169eec99703641930dfa3a526a8507c4dd381b1ef058e7`  
		Last Modified: Wed, 15 Apr 2020 21:26:42 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54794b040fb4b1604b48ecfeed790e0eb3d1375b6fd0e8ca4a6b2e694940e1e`  
		Last Modified: Wed, 15 Apr 2020 21:26:43 GMT  
		Size: 1.1 MB (1132227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432f590b35d89022a5f368b76508d5337553a0d57248204029b86b81776c146a`  
		Last Modified: Wed, 15 Apr 2020 21:26:43 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
