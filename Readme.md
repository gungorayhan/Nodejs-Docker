## dockefile 

FROM node:10 --node js indirdik
WORKDIR /home/node/app --projemizin çalışacağı dizini belirledik
COPY api /home/node/app --proje dosyamızı çalışacağı dizine aktardık
RUN npm install  --docker daha image halindeyken çalıştırılır. eğer yarn kullanıyor olsaydık öncelikle RUN yarn diyerek kurmamız gerekiyordu.Run npm i -save dotenv. çalışabilmesi için
CMD npm run start --oluşturuduğum image i docker ile çalıştır dediğim anca CMD kullanırız. çalışıtrılırken
EXPOSE 3000 --uygulamam hangi port üzerinden çalışacak


## terminal 
Dockerfile dosyamızın bulunduğu dizine gelerek
docker build -t node-rest-api .

docker images
docker run node-rest-api

docker run -p 1234:3000 node-rest-api --port mapping