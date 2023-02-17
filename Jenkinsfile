node {
stage("Git Clone"){

git branch: 'main', url: 'https://github.com/chanakyad/Customer.git'
}
stage("Docker build"){
sh 'docker build -t customer .'
sh 'docker images'
stage("Deploy"){
sh 'docker rm -f customer||true'
sh ' docker run -d -p 9002:9002 --name customer customer'
}
}
}
