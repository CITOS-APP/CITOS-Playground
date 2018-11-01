# CITOS-Playground
<pre>
$ git clone https://github.com/CITOS-App/CITOS-Playground.git
$ cd CITOS-Playground
$ pip install virtualenv
$ virtualenv -p python3 citos_env
 // or  virtualenv -p python2.7 citos_env
$ source citos_env/bin/activate

$ pip install -r requirements.txt
 
$ ansible-galaxy install -r requirements.yml -p roles/

$ make setup

/// 해당 프로젝트 경로에서 실행
$ vagrant ssh local
$ vagrant ssh db
</pre>