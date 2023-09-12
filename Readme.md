## dockerfile 

FROM node:10 --node js indirdik<br/>
WORKDIR /home/node/app --projemizin çalışacağı dizini belirledik<br/>
COPY api /home/node/app --proje dosyamızı çalışacağı dizine aktardık<br/>
RUN npm install  --docker daha image halindeyken çalıştırılır. eğer yarn kullanıyor olsaydık öncelikle RUN yarn diyerek kurmamız gerekiyordu.Run npm i -save dotenv. çalışabilmesi için<br/>
CMD npm run start --oluşturuduğum image i docker ile çalıştır dediğim anca CMD kullanırız. çalışıtrılırken<br/>
EXPOSE 3000 --uygulamam hangi port üzerinden çalışacak<br/>


## terminal 
Dockerfile dosyamızın bulunduğu dizine gelerek<br/>
docker build -t node-rest-api .<br/>

docker images<br/>
docker run node-rest-api<br/>

docker run -p 1234:3000 node-rest-api --port mapping<br/>