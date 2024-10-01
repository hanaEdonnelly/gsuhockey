FROM jekyll/jekyll:latest
LABEL maintainer="sylhare"
LABEL image="sylhare/type-on-strap"

# Set the working directory
WORKDIR /srv/jekyll

# Copy the Gemfile and Gemfile.lock
COPY Gemfile Gemfile.lock ./

# Install the gems
RUN bundle install

# Copy the rest of your site
COPY . .

# Build the site
RUN jekyll build

# Expose the port that the site will be served on
EXPOSE 4000

# Run the Jekyll server
CMD ["jekyll", "serve", "--watch", "--incremental"]
