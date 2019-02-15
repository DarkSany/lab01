# lab01

$ export GITHUB_USERNAME=<имя_пользователя> - задаём значение переменной, echo - для получения
$ export GIST_TOKEN=<сохраненный_токен> 
$ alias edit=<nano|vi|vim|subl> - выбираем редактор, любой из трёх

$ mkdir -p ${GITHUB_USERNAME}/workspace - создание католога
$ cd ${GITHUB_USERNAME}/workspace - переход к каталогу
$ pwd - получение абсолютного пути текущего каталога
$ cd .. - 
$ pwd - 

$ls - показывает содержимое
  
$ mkdir -p workspace/tasks/ - создаём ещё каталоги
$ mkdir -p workspace/projects/
$ mkdir -p workspace/reports/
$ cd workspace
  
$cd .. -  подъём на уровень вверх

# Debian
$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz - загружаем файлы
$ tar -xf node-v6.11.5-linux-x64.tar.xz - обращаемся к архиватору
$ rm -rf node-v6.11.5-linux-x64.tar.xz - удаление файла
$ mv node-v6.11.5-linux-x64 node - перемещение и переименование файла (если вместо node имя поставить)

$ ls node/bin
$ echo ${PATH} - PATH содержит основные доступные пути
$ export PATH=${PATH}:`pwd`/node/bin - переинициализируем переменную, как результат работы pwd
$ echo ${PATH}
$ mkdir scripts
$ cat > scripts/activate<<EOF - cat - выводит содержимое файла, << перенаправление. Создаём файл в памти, она псотупает в cat оттуда через std::out выводим
export PATH=\${PATH}:`pwd`/node/bin
EOF
$ source scripts/activate - перенаправляем в файл active. Если его нет,то создастся

$ npm install -g gistup
$ ls node/bin

$ cat > ~/.gistup.json <<EOF
{
  "token": "${GIST_TOKEN}"
}
EOF
