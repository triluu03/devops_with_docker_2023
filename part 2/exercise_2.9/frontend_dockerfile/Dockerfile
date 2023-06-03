FROM node:16-alpine

WORKDIR /usr/src/app

COPY . .

RUN npm install

ENV REACT_APP_BACKEND_URL=http://localhost/api/

RUN npm run build

RUN npm install -g serve

# I'm using port 4000 because my laptop is using MacOS Monterey.
EXPOSE 4000

CMD ["serve", "-s", "-p", "4000", "build"]
