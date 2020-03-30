# Ujian Tengah Semester Teknologi Cloud Computing Teori
-------------------------------------------------------------------------------------
##### A. Pembuatan Akun Dokerhub
* Untuk pembuatan akun Dockerhub dengan mengunjungi [Docker Hub](https://hub.docker.com/), jika sudah mempunyai akun Docker Hub bisa langsung untuk melakukan [Login](https://id.docker.com/login/?next=%2Fid%2Foauth%2Fauthorize%2F%3Fclient_id%3D43f17c5f-9ba4-4f13-853d-9d0074e349a7%26next%3D%252F%253Fref%253Dlogin%26nonce%3DeyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiI0M2YxN2M1Zi05YmE0LTRmMTMtODUzZC05ZDAwNzRlMzQ5YTciLCJleHAiOjE1ODU1MTQ1NzUsImlhdCI6MTU4NTUxNDI3NSwicmZwIjoidVd2UDNXQ04taEJCYzBfYy1wRUVYZz09IiwidGFyZ2V0X2xpbmtfdXJpIjoiLz9yZWY9bG9naW4ifQ.7xqSCH9ncCNtvK2U-1wlRBvCxeLmViw9rpQ6w6mglLo%26redirect_uri%3Dhttps%253A%252F%252Fhub.docker.com%252Fsso%252Fcallback%26response_type%3Dcode%26scope%3Dopenid%26state%3DeyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiI0M2YxN2M1Zi05YmE0LTRmMTMtODUzZC05ZDAwNzRlMzQ5YTciLCJleHAiOjE1ODU1MTQ1NzUsImlhdCI6MTU4NTUxNDI3NSwicmZwIjoidVd2UDNXQ04taEJCYzBfYy1wRUVYZz09IiwidGFyZ2V0X2xpbmtfdXJpIjoiLz9yZWY9bG9naW4ifQ.7xqSCH9ncCNtvK2U-1wlRBvCxeLmViw9rpQ6w6mglLo), untuk hasil pembuatan akun Docker Hub dapat dilihat pada gambar dibawah
![Gambar Akun Dockerhub](https://github.com/didaap/uts-tekn-cloud-computing/blob/master/akun%20Docker.PNG)
> Hasil pembuatan akun Dockerhub

##### B. Pull image dan menjalankan
* Setelah melakukan pembuatan akun Docker Hub, dilanjutkan dengan menjalankan image dan menjalankan pada komputer. Untuk image yang saya gunakan adalah images drupal.

* Selanjutnya mengetikkan perintah `pull docker drupal` untuk melakukan pull image drupal, untuk proses seperti gambar dibawah
![Proses pull images drupal](https://github.com/didaap/uts-tekn-cloud-computing/blob/master/pull%20drupal.jpg)

* Setelah pull images drupal berhasil, selanjutnya dilakukan run images dengan mengetikkan perintah `docker run -d -p 8080:80 drupal`. 
![Run images drupal](https://github.com/didaap/uts-tekn-cloud-computing/blob/master/run%20drupal%202.jpg)

* Kemudian setelah dirun maka akan menampilkan hasil seperti gambar dibawah :
![Hasil](https://github.com/didaap/uts-tekn-cloud-computing/blob/master/hasil.jpg)


##### C. Membuat Dockerfile dan Push ke Repository Docker Hub
* Untuk membuat image yang pertama yaitu membuat file Dockerfile terlebih dahulu, untuk Dockerfile yang saya buat yaitu
```
#image base
FROM nginx:alpine
#copy aplication file
COPY html /usr/share/nginx/html
```