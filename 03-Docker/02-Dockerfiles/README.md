```
 1168  mkdir 02-Dockerfiles/apache/v1 -p
 1169  ls
 1170  cd 02-Dockerfiles/
 1171  ls
 1172  cd apache/
 1173  ls
 1174  cd v1/
 1175  ls
 1176  vim Dockerfile
 1177  cat Dockerfile
 1178  docker run -it ubuntu:16.04
 1179  docker ps
 1180  curl 172.17.0.2
 1181  ls
 1182  docker ps
 1183  ls
 1184  cat Dockerfile
 1185  docker build -t myapache:v1 .
 1186  docker images
 1187  docker run -d myapache:v1
 1188  docker ps
 1189  cd
 1190  docker inspect 2121ca788dc5
 1191  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' 2121ca788dc5
 1192  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' ${docker ps -q}
 1193  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -q)
 1194  curl -v 172.17.0.3
 1195  docker ps
 1196  curl -v 172.17.0.3:80
 1197  docker ps
 1198  docker run -d -p 8081:80 myapache:v1
 1199  docker ps
 1200  ls
 1201  cd -
 1202  ls
 1203  cd ..
 1204  ls
 1205  cp -rf v1 v2
 1206  ls
 1207  cd v2/
 1208  ls
 1209  vim Dockerfile
 1210  docker build -t myapache:v2 .
 1211  docker images
 1212  docker run -d myapache:v2
 1213  docker ps
 1214  ls
 1215  cd ..
 1216  ls
 1217  cp -rf v2 v3
 1218  ls
 1219  cd v3/
 1220  ls
 1221  vim index.html
 1222  ls
 1223  vim Dockerfile
 1224  ls
 1225  docker build -t myapache:v3 .
 1226  docker run -d myapache:v3
 1227  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -q)
 1228  curl 172.17.0.6
 1229  ls
 1230  docker ps
 1231  docker run -d -P myapache:v3
 1232  docker ps
 1233  ls
 1234  cd ..
 1235  ls
 1236  cd ..
 1237  ls
 1238  cd ..
 1239  ls
 1240  cd 02-Dockerfiles/
 1241  ls
 1242  cd apache/
 1243  ls
 1244  cp -rf v3 v4
 1245  ls
 1246  cd v4/
 1247  ls
 1248  mv Dockerfile mydockerfile
 1249  ls
 1250  vim index.html
 1251  ls
 1252  docker build -t myapache:v4 .
 1253  docker build -t myapache:v4 -f mydockerfile .
 1254  docker run -d -P myapache:v4

```

