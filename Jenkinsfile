pipeline {
	agent any

	stages {
		stage("Compile") {
			steps {
                                sh "chmod +x gradlew"
				sh "./gradlew compileJava"
			}
		}
		stage("Unit test") {
			steps {
                                sh "chmod +x gradlew"
				sh "./gradlew test"
			}
		}
		stage("Build") {
			steps {
                        sh "chmod +x gradlew"
				sh "./gradlew build"
			}
		}
		stage("Commit") {
			steps {
				 "git add --all"
				 "git commit -m ."
				 "git branch -M master"
				 "git push -u origin master"
			}
		}

	}
}
