---
title: "EventsManager"
description: "App to manage all your event's guests"
pubDate: "Sep 22 2023"
heroImage: "/post_img.webp"
---

This app was created to manage all the people that I invited to a personal event. 
With this app you could:

* Manage all event invitations with an Admin portal.
* Send SMS from the admin portal, allowing updates on attendance and prompting guests to upload event photos.
* Post-event, the app generates a gallery featuring all photos uploaded by invited attendees.

Infraestructure:
* Monorepo using turborepo
* Admin portal: Next.js with Nextui, deployed on Vercel and domain hosted on AWS Route53
* Supabase as a Auth provider
* DynamoDB as a guest DB
* React.js app as a Gallery (Vite), deployed on Vercel and domain on AWS
* React.js app to allow a person to update the assistance. Deployed on S3 Bucket linked with CloudFront as a cache.
* API-Rest deployed on AWS API Gateway + lambda to either:
    * upload event photos
    * update assistance


<a target="_blank" href="https://github.com/gtrrz-victor/eman">Goto Github Project</a>