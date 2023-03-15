include .env

all: back front start_project

back:
	@mkdir -p ${BACK_PATH}
	@if [ x$(shell find ${BACK_PATH} -prune -empty) = x${BACK_PATH} ]; then \
		if [ x${BACK_PROJECT_LINK} != x]; then \
			git clone ${BACK_PROJECT_LINK} ${BACK_PATH}; \
		fi; \
	else \
		echo "back is good"; \
	fi;
	@echo "back is done"

front:
	@mkdir -p ${FRONT_PATH}
	@if [ x$(shell find ${FRONT_PATH} -prune -empty) = x${BACK_PATH} ]; then \
		if [ x${FRONT_PROJECT_LINK} != x]; then \
			git clone ${FRONT_PROJECT_LINK} ${FRONT_PATH}; \
		else \
			echo "no rep"; \
		fi; \
	else \
		echo "front is good"; \
	fi;
	@echo "front is done"

start_project:
	@docker-compose up -d