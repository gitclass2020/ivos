pipeline{
agent {node {label 'S1'}}

stages {
	stage(checkout) {
	steps {
checkout([$class: 'GitSCM', branches: [[name: 'master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'eec141d1-ea8c-43f9-801a-cab104ec4365', url: 'https://github.com/gitclass2020/ivos.git']]])
	
	
	script {
		DATE_TAG = java.time.LocalDte.now()
		DATETIME_TAG = java.time.LocalDateTime.now()
	   }
     echo ${DATETIME_TAG}
	 }
   }
   stage(print) {
	steps {
		echo 'TESTING PIPELINE - HOTFIX'
		echo ${DATETIME_TAG}
	
	script {
		def now = new Date()
		println now.format("yyMMdd.HHmm", TimeZone.getTimeZone('UTC'))
	}
   }
 }
}
}