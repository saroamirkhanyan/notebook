# Խառը գրառումներ Go-ի մասին

## Աշխատանքային միջավայրի նախապատրաստումը

Ինչքան հիշում եմ, Go լեզվի առաջին իսկ հրապարակային թողարկումից սկսած ես իմ բոլոր համակարգիչների վրա՝ թե՛ անձնական օգտագործման, թե՛ աշխատանքային, միշտ ունեցել եմ Go-ի ամենաթարմ կոմպիլյատորը։

`$HOME` պանակում ստեղծում եմ `golang` անունով պանակ։

```bash
$ cd ~
$ mkdir golang
$ cd golang
```

[go.dev](https://go.dev/)-ից ներբեռնում եմ Go-ի իրականացման արխիվը, բացում եմ այն `golang`-ի մեջ ու ջնջում եմ արխիվը։

```bash
$ wget https://go.dev/dl/go1.17.6.linux-amd64.tar.gz
$ tar xf go1.17.6.linux-amd64.tar.gz
$ rm go1.17.6.linux-amd64.tar.gz
```

Արխիվից բացվում է `go` անունով պանակը, որի `bin` ենթապանակը պետք է ավելացնել միջավայրի `PATH` փոփոխականին՝ `go` գործիքները հասանելի դարձնելու համար։

```bash
$ echo 'PATH="$HOME/golang/go/bin:$PATH"' >> ~/.profile
```

Հետո նույն `golang`-ի մեջ ստեղծում եմ `gopath` պանակն ու `GOPATH` փոփոխականին վերագրում եմ դրա արժեքը։ Այս պանակն օգտագործվում է լրացուցիչ գործիքներ ու գրադարաններ տեղադրելու համար։

```bash
$ mkdir gopath
$ echo 'export GOPATH="$HOME/golang/gopath"' >> ~/.profile
```

Որպեսզի `PATH`-ի ու `GOPATH`-ի փոփոխություններն արտացոլվեն միջավայրում, կատարում եմ հետևյալ հրամանը.

```bash
$ source ~/.profile
```