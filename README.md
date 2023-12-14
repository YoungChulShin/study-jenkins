# 저장소 설명
Jenkins를 이용한 빌드 테스트

# 연관 사이트
docker-hub: [link](https://hub.docker.com/r/jenkins/jenkins)

# 시작
1. `docker-compose.yml`을 이용해서 jenkins를 구동한다. 
2. `localhost:8080`으로 접속한다. 

# pipeline 프로젝트
jenkins에서 제공하는 pipeline 코드를 이용해서 빌드 환경을 구성하는 방법.
## pipeline 구성
값 정보
- agent
- stages
   - stage
      - when
      - steps

샘플 값
```groovy
pipeline {
    agent any
    
    stages {
        stage('init') {
            steps {
                echo 'init...'
            }
        }
        
        stage('build') {
            steps {
                echo 'build...'
            }
        }
    }
}
```


https://1minute-before6pm.tistory.com/52?category=1077827