Bu repoyu indirip terminalden reponun olduğu klasöre girin

## Docker Compose Yükleme

Mac kullanlar eğer makinelerinde docker yüklü ise docker compose da yüklü olacaktır<br/>
Eğer `sudo docker-compose up` çalışırsa `PgAdmin Hazırlığı` kısmından devam edebilirsiniz<br/>

[Mac Referans](https://docs.docker.com/docker-for-mac/install/)<br/>
Mac kullananlar [bu linkten](https://hub.docker.com/editions/community/docker-ce-desktop-mac/) uygulama olarak indirebilir<br/>
<br/>
[Linux Referans1](https://docs.docker.com/compose/install/)<br/>
[Linux Referans2](https://linuxhint.com/postgresql_docker/)<br/>

Linux kullananlar `history.txt` dosyasındaki komutları kullanarak kurabilir.<br/>

## PgAdmin Hazırlığı

Tarayıcıdan localhost:5051 'e gir <br/>
*email: pgadmin4@pgadmin.org <br/>
*şifre: root <br/>

### Add New Server'a tıkla

İstediğiniz bir ismi verip Connection kısmına geçin <br/>

*host: pgsql-server<br/>
*post: 5432<br/>
*maintanence database: postgres<br/>
*username: postgres<br/>
*password: postgres<br/>

<br/>
İleride şifre sormaması için save password'u seçebilirsiniz
<br/>

Bu bilgileri girip kaydedin<br/>
Server soldaki servers tabında çıkacaktır

### Çalıştırma

Docker dosyasının olduğu klasöre terminalden girip <br/>
`sudo docker-compose up` komutunu çalıştırın. <br/>
Tarayıcıdan localhost:5051 'e gir <br/>

### Terminalden Kmut girme
Öncelikle bir terminal açık 
```
sudo docker-compose up
```
komutu ile sunucuyu arkada çalıştırın.

Ardından başka bir terminalde aşağıdaki komut çalıştırmak sizi postgres kullanıcısı ile veritabanına bağlayacaktır.
```
sudo docker-compose run --rm db psql -h postgres -U postgres
```
Şifre: postgres

