FROM ubuntu:latest

# Set US English and UTF-8 Locale
RUN apt-get update && apt-get install -y locales && rm -rf /var/lib/apt/lists/* \
	&& localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
ENV LANG=en_US.utf8

# Remove 'ubuntu' user if it exists
RUN if id "ubuntu" &>/dev/null; then \
		echo "Deleting user 'ubuntu'"; \
		deluser --remove-home ubuntu || echo "Failed to delete ubuntu user"; \
	else \
		echo "User 'ubuntu' does not exist"; \
	fi
