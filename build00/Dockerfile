FROM nginx:1.23

# 같은 디렉토리에 있는 index.html 파일을 /usr/share/nginx/html/index.html로 덮어쓴다
COPY index.html /usr/share/nginx/html/index.html

CMD ["nginx", "-g", "daemon off;"]
