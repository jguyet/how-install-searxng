# how-install-searxng

1. Install docker on your server.
2. docker pull searxng/searxng
3. docker run -d -p 8888:8080 --name searxng --restart always searxng/searxng
4. docker exec -it [containerID] sh
5. vi /etc/searxng/settings.yml
6. add `- json` after `- html`
7. Now you can use your searxng search engine on http://ip:8888/search?q=test&format=json

You can use searxng on you openwebui with the searchTool [https://openwebui.com/t/constliakos/web_search](https://openwebui.com/t/constliakos/web_search) by adding http://ip:8888/search on the tool setting.
