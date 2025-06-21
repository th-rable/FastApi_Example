# FastApi_Example
FastAPI와 Docker, Action 시스템의 구현을 위한 예시 Repository
# 도커 로그인


# 도커 이미지 빌드
docker build --platform linux/arm64/v8 -t rable00/firstdocker .
ID와 repo 이름이 같아야 Hub에 Push 가능
도커 돌릴 platform을 써줘야함

# 도커 컨테이너 생성 및 실행
docker run -d --name mycontainer -p 8080:8080 rable00/firstdocker

# 컨테이너 상태 확인
docker ps -a
# 컨테이너 종료
docker stop mycontainer
# 컨테이너 삭제
docker rm mycontainer
# 컨테이너 종료 후 삭제
docker rm -f mycontainer

# 컨테이너 일시중지 및 재개
docker pause mycontainer
docker unpause mycontainer


# 이미지 확인
docker images
# 이미지 삭제
docker rmi [이미지id]

# 이미지 PULL
docker pull rable00/firstdocker:latest
# 이미지 PUSH
docker push rable00/firstdocker:latest