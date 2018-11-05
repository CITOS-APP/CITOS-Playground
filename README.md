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

// Vagrantfile에 명시된 vm 생성
$ vagrant up

$ make setup

/// 해당 프로젝트 경로에서 실행, ssh 접속
$ vagrant ssh local
$ vagrant ssh db



// Vagrantfile에 명시된 vm 멈춤, 재부팅, 삭제
$ vagrant halt
$ vagrant reload
$ vagrant destroy

</pre>