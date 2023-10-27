FROM node:20-alpine3.17
WORKDIR /app
COPY package.json .
RUN npm install
COPY /app/. /app
EXPOSE 8080
ENV USER=cami
ENV PASSWORD=cami0503
ENV DB=ECOMMERCE
ENV MONGO_URI="mongodb+srv://${USER}:${PASSWORD}@cluster0.17xc4.mongodb.net/${DB}retryWrites=true&w=majority"
CMD ["npm", "start"]



