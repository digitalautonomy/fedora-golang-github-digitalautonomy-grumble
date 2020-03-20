To fix: To build you need to manually clone and generate the tar.gz expected by the spec file.
Spec files uploaded to Fedora's repo auto download the source code. I would fix this later.

```
git clone https://github.com/digitalautonomy/grumble.git
mv grumble/ grumble-c109af8d88b4b9cb77afe1f18572c66027cf8c0b
tar zcf grumble-c109af8d88b4b9cb77afe1f18572c66027cf8c0b.tar.gz grumble-c109af8d88b4b9cb77afe1f18572c66027cf8c0b/
```

To build this package you would need to install the `golang-x-crypto-devel, golang-github-protobuf-devel, golang-github-gorilla-websocket-devel
` packages.

Building the package:
```
fedpkg --release f31 local
```
