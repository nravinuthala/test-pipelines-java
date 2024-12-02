pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }

    stages {
        stage('Test') {
            steps {
                // Get some code from a GitHub repository
                git url: 'https://github.com/nravinuthala/test-pipelines-java.git',
                    branch: 'main'

                // Run Maven on a Unix agent.
                sh "mvn clean test"

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

        }
    }
}
