# FastApi_Example
FastAPI와 Docker, Action 시스템의 구현을 위한 예시 Repository

# 시작하기
pip install -r requirements.txt

# 서버실행
uvicorn main:app --reload
   OR   
python3 -m uvicorn main:app --reload

# 도커 로그인
docker login

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
# 빌드 플랫폼 추가하기
docker run --privileged --rm tonistiigi/binfmt --install all

# 도커 실시간 로그 확인하기
docker logs -f --tail 10 mycontainer
