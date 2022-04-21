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
				sh "git add --all"
				sh "git commit -m ."
				sh "git branch -M master"
				sh "git push -u origin master"
			}
		}

	}
}
