SimShop Api 

Postman documantation link : https://documenter.getpostman.com/view/27227009/2s93z6cP6Q

Code first veritabanlarının olusturulması için powershell arayüzüne asagıdaki kod girilmelidir :

dotnet ef database update --project "./SimShop” --startup-project "./SimShop"

Project database diagram :
![diagram](https://github.com/enesaym/SimpraBootcampFinalProject/assets/89969736/33d0610f-694a-424a-bd2a-36ed2119b21c)


Adım 1:
![login](https://github.com/enesaym/SimpraBootcampFinalProject/assets/89969736/a1e72661-5485-4c62-9c91-b84b00a49267)

Sistem senaryosu admin yetkisine sahip kullanıcının admin,admin kullanıcı adı ve şifresini girerek login olması ile başlar. 
Get : Giriş yapmış kullanıcının bilgilerini getirir.
Post(SingIn): Kullanıcının giriş yaparak accessToken almasını sağlar.
Post(SıgnUp): Kullanıcının sisteme customer yetkisiyle kayıt olmasını sağlar.

Adım 2:
![category](https://github.com/enesaym/SimpraBootcampFinalProject/assets/89969736/9a9da49f-5f97-4faf-9d06-e4fdf1514f65)

Admin yetkisi ile giriş yapıldıktan sonra ürün eklenebilmesi için categoryler eklenir. Categoryler id ye göre güncellenebilir veya silinebilir. 

Adım 3:
![product](https://github.com/enesaym/SimpraBootcampFinalProject/assets/89969736/b8cc6099-3a72-496d-a40b-b42c607a688c)

Categoryler eklendikten sonra ürünler eklenir. Her ürünün bir kategoriye ait olması gereklidir. 
Ürünler category id ye göre listelenebilir. Ürün id ye göre güncellenebilir veya silinebilir.

Adım 4:
![Untitled](https://github.com/enesaym/SimpraBootcampFinalProject/assets/89969736/a7bf3f5d-b99e-4194-a36b-217c3fee979b)


Admin yetkisine sahip kullanıcılar sistemdeki kullanıcılara Post metodu ile kupon tanımlayabilir. Get metodu ile sistemdeki aktif kullanıcı kendisine tanımlanan kuponları görüntüleyebilir.

Adım 5:
![basket](https://github.com/enesaym/SimpraBootcampFinalProject/assets/89969736/01d0c424-8c7d-4861-a395-d78ef4a1a8f7)

Bu adımdan sonra customer rölüne sahip kullanıcılar sepetlerine ürün ekleyip cıkarabilir ve sepet içerisindeki ürünleri görüntüleyebilir.

Adım 6:
![order](https://github.com/enesaym/SimpraBootcampFinalProject/assets/89969736/125942de-b986-47a1-84a8-ddb3702189a1)

Kullanıcı sepetindeki ürünleri order post ile sipariş verebilir. Sipariş verildikten sonra kullanıcıya ait siparişler get apisi ile görüntülenebilir. Sipariş verildikten sonra kullanıcı sepeti temizlenir. Sipariş sırasında kupon kodu girilirse kupon kodu ve cüzdan bakiyesi kadar indirim yapılır. Kullanılan puanlara ve kupon kodlarına göre puan kazanımı cüzdan hesabına aktarilir.

Extra : 
![Untitsdled](https://github.com/enesaym/SimpraBootcampFinalProject/assets/89969736/dee0d507-8345-48e1-99d6-bcd7a35b0da8)

Admin yetkisine sahip kullanıcı sisteme admin yetkisine sahip kullanıcı ekleyebilir veya tüm kullanıcılar üzerinde silme guncelleme ve getirme işlemlerini yapabilir.

