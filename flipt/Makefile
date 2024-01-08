url := http://localhost:9090

up:
	docker compose up -d
	docker compose ps

down:
	docker compose down

restart: down up

logs:
	docker compose logs --follow

feature_flag := demotoggle
test:
	curl $(url)/api/v1/flags/$(feature_flag)

ui:
	open $(url)
