


#### dependencies needed:

![[Pasted image 20260102161719.png]]



#### in the root directory run 
npx create-next-app@latest frontend



#### run these
run npm init -y
npm install concurrently --save-dev


#### add this to your scripts in package.json
"scripts": { "dev": "concurrently \"cd backend && ./mvnw spring-boot:run\" \"cd frontend && npm run dev\"" }


