deploy: Dockerfile nginx.conf nginx.vh.default.conf
	$(eval DATE := $(shell date +%Y%m%d%H%M%s))
	docker build -t kter/nginx-vts-module:$(DATE) .
	docker tag kter/nginx-vts-module:$(DATE) kter/nginx-vts-module:latest
	docker push kter/nginx-vts-module:${DATE}
	docker push kter/nginx-vts-module:latest

.PHONY: deploy
