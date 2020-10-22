Bu repoyu indirip terminalden reponun olduğu klasöre girin

## Docker Compose Yükleme

[Referans1](https://docs.docker.com/compose/install/)<br/>
[Referans2](https://linuxhint.com/postgresql_docker/)<br/>

`sudo curl -L -k "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-\$(uname -m)" -o /usr/local/bin/docker-compose` <br/>
`sudo chmod +x /usr/local/bin/docker-compose` <br/>
`sudo docker-compose up`<br/>
Çalışmazsa docker yüklü değil demektir<br/>

## Docker Yükleme

[Mac Referans](https://docs.docker.com/docker-for-mac/install/)<br/>
Mac kullananlar [bu linkten](https://hub.docker.com/editions/community/docker-ce-desktop-mac/) uygulama olarak indirebilir.<br/>
<br/>
[Linux Referans](https://docs.docker.com/engine/install/ubuntu/)<br/>
Linux kullananlar aşağıdaki komutlarla yükelyebilir<br/>

`sudo apt-get remove docker docker-engine docker.io containerd runc`<br/>
Not: bu kod hata verebilir sorun değil<br/>
`sudo apt-get update` <br/>
`sudo apt-get install apt-transport-https curl gnupg-agentsoftware-properties-common`<br/>
(Hata verirse: `sudo apt-get install --reinstall ca-certificates`) <br/>
`curl -fsSL -k https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -` <br/>
`sudo apt-key fingerprint 0EBFCD88` <br/>
`sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linuxubuntu $(lsb_release -cs) stable"`<br/>
(Çalışmaza: `sudo add-apt-repository "deb [arch=amd64] https://download.dockercom/linux/ubuntu bionic stable"`) <br/>
`sudo apt-get update` <br/>
`sudo apt-get install docker-ce docker-ce-cli containerd.io` <br/>
`sudo docker-compose up` <br/>

## PgAdmin Hazırlığı

Tarayıcıdan localhost:5051 'e gir <br/>
Email ve şifre docker-compose.yml dosyasında:<br/>
*email: pgadmin4@pgadmin.org <br/>
*şifre: root <br/>

### Add New Server'a tıkla

İstediğiniz bir ismi verip Connection kısmına geçin <br/>

*host: localhost (Çalışmazsa 127.0.0.1 veya 172.17.0.1)
<br/>
*post: 5432<br/>
*database username ve password docker-compose.yml dosyasında:<br/>
*maintanence database: postgres<br/>
*username: postgres<br/>
*password: postgres<br/>

<br/>
İleride şifre sormaması için save password'u seçebilirsiniz.
<br/>

Bu bilgileri girip kaydedin<br/>
Database soldaki servers tabında çıkacaktır