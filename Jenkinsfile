pipeline {
 agent any
 stages {
        stage("Deployment") {
            steps {
                sh 'git fetch --all'
                sh 'git checkout ${custom_var}'
                sh 'php --version'
		        sh 'composer install'
                sh 'composer dump-autoload'
                sh 'php artisan clear-compiled'
                sh 'php artisan cache:clear'
                sh 'php artisan config:clear'
                sh 'php artisan config:cache'
                sh 'php artisan route:clear'
                sh 'php artisan view:clear'
            }
        }
    }
}
