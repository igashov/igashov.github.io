FROM ruby:latest

# Install required packages
RUN apt-get update && apt-get install -y \
    build-essential \
    nodejs \
    git \
&& rm -rf /var/lib/apt/lists/*

# Set the working directory
WORKDIR /app

# Copy Gemfile and Gemfile.lock into the container
COPY Gemfile ./

# Install gems
RUN bundle install

# Expose port 4000 for Jekyll
EXPOSE 4000
