Bu repoyu indirip terminalden reponun olduğu klasöre girin

## Docker Compose Yükleme

Mac kullanlar eğer makinelerinde docker yüklü ise docker compose da yüklü olacaktır<br/>
eğer `sudo docker-compose up` çalışmazsa `Docker Yükleme` kısmından docker yükleyin<br/>

[Linux Referans1](https://docs.docker.com/compose/install/)<br/>
[Linux Referans2](https://linuxhint.com/postgresql_docker/)<br/>

`sudo curl -L -k "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-\$(uname -m)" -o /usr/local/bin/docker-compose` <br/>
`sudo chmod +x /usr/local/bin/docker-compose` <br/>
`sudo docker-compose up`<br/>
Çalışmazsa docker yüklü değil demektir<br/>

## Docker Yükleme

[Mac Referans](https://docs.docker.com/docker-for-mac/install/)<br/>
Mac kullananlar [bu linkten](https://hub.docker.com/editions/community/docker-ce-desktop-mac/) uygulama olarak indirebilir<br/>
<br/>
[Linux Referans](https://docs.docker.com/engine/install/ubuntu/)<br/>
Linux kullananlar `history.txt` dosyasındaki komutları kullanarak kurabilir.<br/>

## PgAdmin Hazırlığı

Tarayıcıdan localhost:5051 'e gir <br/>
Email ve şifre docker-compose.yml dosyasında:<br/>
*email: pgadmin4@pgadmin.org <br/>
*şifre: root <br/>

### Add New Server'a tıkla

İstediğiniz bir ismi verip Connection kısmına geçin <br/>

*host: pgsql-server
<br/>
*post: 5432<br/>
*maintanence database: postgres<br/>
*username: postgres<br/>
*password: postgres<br/>

<br/>
İleride şifre sormaması için save password'u seçebilirsiniz
<br/>

Bu bilgileri girip kaydedin<br/>
Server soldaki servers tabında çıkacaktır
