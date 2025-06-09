pipeline{
agent any
stages {
stage('Build Application') {
steps {
bat 'mvn clean install'
}
}
stage('Deploy CloudHubs') {
environment {
ANYPOINT_CREDENTIALS = credentials('d1c9e494-3a7a-449e-be79-153ce7aa7c00')
}
steps {
echo 'Deploying mule project due to the latest code commit…'
echo 'Deploying to the configured environment….'
bat 'mvn clean deploy -DmuleDeploy -Dmule.app.name=cicdproject-Dusername=gebrehiwott-Dpassword=Abcdpin131790'
}
}
}
}