FROM ruby
RUN gem install sinatra
RUN gem install thin

#RUN printenv > env.out

FROM scratch
COPY --from=0 / /

#RUN source env.out

# Harcoding default values
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
ENV LANG=C.UTF-8
ENV GEM_HOME=/usr/local/bundle
ENV BUNDLE_SILENCE_ROOT_WARNING=1
ENV BUNDLE_APP_CONFIG=/usr/local/bundle
