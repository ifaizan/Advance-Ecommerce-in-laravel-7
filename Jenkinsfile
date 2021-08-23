pipeline {
 agent any
 stages {
        stage("Deployment") {
            steps {
                sh 'php --version'
                sh 'composer dump-autoload'
                sh 'php artisan clear-compiled'
                sh 'php artisan cache:clear'
                sh 'php artisan config:clear'
                sh 'php artisan config:cache'
                sh 'php artisan route:clear'
                sh 'php artisan view:clear'
                sh '/etc/init.d/supervisor restart'
            }
        }
    }
}
