@title[Prerequisites]

@snap[north span-100]
@size[1.5em](Prerequisites)
@snapend

@snap[center span-100]
@ul
- AWS Account
- [eksctl](https://eksctl.io/)
- [AWS IAM Authenticator](https://github.com/kubernetes-sigs/aws-iam-authenticator)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
@snapend

---
@title[Prerequisites - MacOS]

@snap[north span-100]
@size[1.5em](MacOS)
@snapend

@snap[center span-100]
Using [Homebrew](https://brew.sh/) is the easiest option. The following will install eksctk, kubetl and AWS IAM Authenticator
@snapend

```
brew install weaveworks/tap/eksctl
```

@snap[south template-note]
*[eksctl](https://eksctl.io/)* is looking for contributors to help make it great
@snapend

---
@title[Prerequisites - Linux]

@snap[north span-100]
@size[1.5em](Linux)
@snapend

@snap[center span-100]
You will need to install everything separately according to the instructions.
@snapend
<br>

```bash
curl --silent --location "https://github.com/weaveworks/eksctl/releases/download/latest_release/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
sudo mv /tmp/eksctl /usr/local/bin
```

** To finish **




