# Hướng dẫn tạo bot Telegram download mp3 từ youtube

![Build Status](https://img.shields.io/github/actions/workflow/status/d3473r/youtube-mp3-bot/docker-image.yml)
![Latest Version](https://ghcr-badge.egpl.dev/d3473r/youtube-mp3-bot/latest_tag?trim=major&label=latest)
![Docker Image Size (tag)](https://ghcr-badge.egpl.dev/d3473r/youtube-mp3-bot/size?tag=main)

## Tạo trên vps Ubuntu hoặc aacpnel
01. Cài đặt docker lên máy chủ vps
```
curl -fsSL https://get.docker.com | bash -s docker
```
```
curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose && chmod +x /usr/local/bin/docker-compose
```
02. Tạo bản sao git về may chủ
```
git clone https://github.com/nqthaivl/youtube-mp3-bot.git
```
3. Chuyển đến thư mục youtube-mp3
```
cd youtube-mp3-bot
```
4. Đổi tên file .env.example thành .env
```
cp .env.example .env
```
5. Chỉnh sửa file `.env` thêm token telegram vào
6. Khởi chạy docker (nhớ chuyển vào thư mục youtube-mp3-bot rồi chạy)
```
docker-compose up -d
```
- Bot chấp nhận các loại link `www.youtube.com`, `m.youtube.com` hoặc `youtu.be` 

## Chú ý

- [Chỉ chấp nhận các file nhỏ hơn 50MB](https://core.telegram.org/bots/faq#how-do-i-upload-a-large-file)
