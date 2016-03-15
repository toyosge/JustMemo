# modern.IE

## 前提

brewで作業するので、
brewがインストールされていること。

## Vagrantのインストール

```Command
brew cask install vagrant
```

## VirtualBoxのインストール

```Command
brew cask install virtualbox
```

## Boxを追加する

```Command
vagrant box add boxName url
```

windowsXPのIE6をBOXに追加してみる

```サンプル
vagrant box add xp-ie6 http://aka.ms/vagrant-xp-ie6
```

他のIEが欲しい場合は、以下から選んでね！！

>
* XP with IE6:
http://aka.ms/vagrant-xp-ie6
* XP with IE8:
http://aka.ms/vagrant-xp-ie8
* Vista with IE7:
http://aka.ms/vagrant-vista-ie7
* Windows 7 with IE8:
http://aka.ms/vagrant-win7-ie8
* Windows 7 with IE9:
http://aka.ms/vagrant-win7-ie9
* Windows 7 with IE10:
http://aka.ms/vagrant-win7-ie10
* Windows 7 with IE11:
http://aka.ms/vagrant-win7-ie11
* Windows 8 with IE10:
http://aka.ms/vagrant-win8-ie10
* Windows 8.1 with IE11:
http://aka.ms/vagrant-win81-ie11

## 仮想環境の初期化

まずは、管理する場所をつくる
任意の場所にディレクトリを作成する

```Command
mkdir /hoge/hoge/xp-ie6
cd /hoge/hoge/xp-ie6
```

続いて初期化

```Command
vagrant init xp-ie6
```

## Vagrantfileの設定を変更する

sshで接続できないので、guiで起動するように変更する

```Command
vim vagrantfile
```

guiの設定がコメントアウトされているので、コメントアウトを外す。

```設定内容
config.vm.provider "virtualbox" do |vb|
  # Display the VirtualBox GUI when booting the machine
  vb.gui = true

  # Customize the amount of memory on the VM:
  vb.memory = "1024"
end
```

## 仮想環境を起動する

```Command
vagrant up
```

## 仮想環境を停止する

```Command
vagrant halt
```

## 参考URL

* modern.IE を Vagrant で使う
http://qiita.com/yteraoka/items/06fc91f37913c938d936
