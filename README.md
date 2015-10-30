# Build

	docker build -t dgageot/ngxpagespeed .

# Run

	docker run --rm -ti --net host -v $(pwd)/sites-enabled:/etc/nginx/sites-enabled dgageot/ngxpagespeed
	
	
# Compose
	
	pagespeed:
      build: build/ngxpagespeed
      links:
        - 'nginx:WEB'
      ports:
        - '80'
