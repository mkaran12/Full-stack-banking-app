## Mkaran School lms platform

This repository contains a faithful copy and enhancement of the LMS platform.

**Deployment:**

To deploy the application to production, you will need to sign up for accounts on the following services:

Vercel https://vercel.com - for server-less hosting.

Mux https://mux.com - for Videos storage. 

Clerk https://clerk.com authetication

MongoDB Atlas https://mongodb.com This project  uses MongoDb.com. I've 
found it to be much more flexible for budding NextJS developers. I've created 7 free databases there
so far and it is perfect for my needs. I had no problems modifying the schema for use with MongoDB and 
if you are looking for a project already adapted for Mongo - honestly the only changes were in the 
Schema! And Copilot did all the heavy lifting.  

UploadThing https://uploadthing.com/ for serverless upload storage.

**Key Features:**

* Browse and filter courses
* Purchase courses using Stripe
* Mark chapters as completed or uncompleted
* Progress calculation of each course
* Student dashboard
* Teacher mode
* Create new courses
* Create new chapters
* Easily reorder chapter position with drag and drop
* Upload thumbnails, attachments, and videos using UploadThing
* Video processing using Mux
* HLS Video player using Mux
* Rich text editor for chapter description
* Authentication using Clerk
* ORM using Prisma
* MySQL database using Planetscale

**Enhancements:**

* Added a search function to the courses page
* Improved the user interface of the student and teacher dashboards

**Planned Enhancement:**
Integrate Elliot Chong's Quizmify into this.

**Usage:**

To use this repository, you will need to have Node.js and NPM installed on your machine. Once you have installed the necessary dependencies, you can clone the repository and run the following commands:


To reset the database, run 

    npx prisma migrate reset
    npx prisma db push

Note that when I ran npx prisma migrate reset against mongodb.com I ran
into errors in the terminal stating I lacked permission. However, aftersn
running the command I did reinitialize the database. 

Note also if reinitializing the datbase you also need to run:node scripts/seed.ts
This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

