FROM node

RUN mkdir -p /nuxt
COPY . /nuxt
WORKDIR /nuxt

RUN npm install -g yarn && \
    chmod u+x /usr/local/bin/yarn && \    
    yarn global add nuxt && \
    yarn global add vue-cli create-nuxt-app && \
    yarn install && yarn build

ENV HOST 0.0.0.0
EXPOSE 3000
CMD ["yarn", "run", "dev"]