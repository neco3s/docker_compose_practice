# docker_compose_practice

### 学んだこと

- ps -ef で全てのプロセスを詳細に表示できる(uidなども表示される)
- docker-composeのつかい時,(docker runコマンドが長くなる時、複数のコンテナをまとめて起動するとき)
- docker run -v ${pwd}:/product-register -p 3000:3000 -it  4df56ae6aa44 bash
- docker build \<build context> <-> docker-compose build
- docker run \<image> <-> docker-compose up(imageがなければbuildしてからrunする)
- docker ps <-> docker-compose ps
- docker exec \<container> \<command> <-> docker-compose exec \<service> \<command> (serviceにはdocker-compose.ymlで書いたwebやdbなのでservice名を記入する,container idを指定する必要はない)
- docker-compose up -build (buildしてrun,Dockerfileを更新した場合はdocker-compose upで起動しても古いイメージがそのまま使われてしまうので再度buildしたいときは--buildを使う)
- docker-compose down (stopしてrm)
- docker-compose up -d(Dockerfileからイメージを作成し、そのイメージでコンテナを起動run(create+start)する)
- rails new . --force --database=postgresql --skip-bundle
- Gemfileが新しくなったら新しいイメージをbuildする(DockerfileでRUN bundle installすることでpackageをレイヤーとしてイメージに追加できる。コンテナが起動するたびにインストールする必要はない)
- docker-compose logs(ログを見れる、問題解決に役立つ)


### 参考にした動画

<https://www.udemy.com/course/aidocker/learn/lecture/20295745#content>
