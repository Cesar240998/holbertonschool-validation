#make file - Development Lifecycle with Makefile
build:  ## create a rule to build the webpage and create the file /dist
	hugo
clean:  ## create a rule clean to clenup all directory /dist
	@rm -rf dist/*
post:   ## Create a new blog post using enviroment variable
	@hugo new posts/$(POST_NAME).md
	@sed -i 's/title:.*/title: $(POST_TITLE)/' content/posts/$(POST_NAME).md
	@sed -i -r 's/draft:.*/draft:"false"/' content/posts/$(POST_NAME).md
help:   ## command help
	@fgrep -h "##" $(MAKEFILE_LIST) | fgrep -v fgrep | sed -e 's/\\$$//' | sed -e 's/##//'
