---
title: "EmailScraper"
description: "Scrapping third party emails"
pubDate: "Sep 22 2022"
heroImage: "/emailscrapper.png"
---

This app was created to assist a friend with his tour company by centralizing bookings from third-party systems. Here's what I developed:

* Set up an AWS WorkMail account to receive emails from third-party booking systems.
Linked the WorkMail account with an S3 bucket for backup.
* Configured S3 bucket events to trigger whenever a new element (email) was created, indicating a new booking.
* Implemented a GoLang Lambda to parse the received text email into HTML, extracting booking details using XPath/CSS selectors, and emitting an event with the formatted data.
* Developed another GoLang Lambda to listen to events with formatted data and insert it into an AWS DocumentDB.

I replicated the solution in both Node.js and GoLang to compare performance and optimize costs by considering execution time and memory usage.

Utilizing Lambdas and DocumentDB is advantageous; with no traffic, there are no associated costs, making it an ideal, cost-effective solution for proof of concept validation.

<a target="_blank" href="https://github.com/gtrrz-victor/email-scraper">Goto Github Project</a>