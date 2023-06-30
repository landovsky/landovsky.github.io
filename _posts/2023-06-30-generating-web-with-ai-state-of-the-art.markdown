---
layout: post
title:  "Generating web with AI - state of the art?"
date:   2023-06-29 21:15:34 +0100
categories: en
---

# Objectives

---

**I would like to speed-up UI prototyping so that I can go from a prompt to code real fast.**

Specifically I wanted to design a webpage given this specification:

**TLDR** *(full brief in the appendix)*

Search engine simplifying the process of finding pharmacies with specific medicines. Page 1: Search by medicine name and view results with in-stock indicators. Sort results by distance. Page 2: Medicine detail showing which pharmacies have it in stock, with info about each pharmacy (address, opening hours.)

**I’ve briefly explored several approaches**

- specialized tools
- ChatGPT
- Figma plugins

# Specialized tools

---

From 4 random articles titled "10 best tools for AI design" I've picked solutions matching my problem.

**Verdict**

- overall failure in helping my use-case
- most tools have preconceived idea of web structure
- tools are probably designed for people who could not otherwise build a web and so their needs don’t match mine (missing exports, etc)

## [Snappy.appypie.com](http://snappy.appypie.com/)

- Platform purpose: "Create powerful web and mobile applications and automate workflows easily and quickly without any coding."
- Generates a site based on prompt (without word limit).
- The output is more of a wireframe, purposed for a phone resolution.

![snappy.appypie.com result.png](/assets/images/generating-web-with-ai/snappy.appypie.com_result.png)

## [Uizard.io](http://uizard.io/) 👍

- First real generator (28 USD per month).
- Takes a 300-character description prompt and 150-character design requirements.
- Pros: generates several screens with components, creates a prototype with pages linked together. Users generative model to create images. The result is editable (Figma-like).
- Cons: most of UX is hallucinations, none of it is actually usable as a finished product; components are recycled (across completely different prompts), does not adhere to constraints (i.e. design 2 pages). Can only be exported as PDF, PNG, and JPEG.

![uizard-pharmacy-Landing-f4c78.png](/assets/images/generating-web-with-ai/uizard-pharmacy-Landing-f4c78.png)

![uizard-pharmacy-SearchResults-ba8de.png](/assets/images/generating-web-with-ai/uizard-pharmacy-SearchResults-ba8de.png)

⬇️ Result for prompt asking for completely something different, spot 10 similarities..

![Landing-79686.png](/assets/images/generating-web-with-ai/Landing-79686.png)

## [Durable.co](http://durable.co/)

- AI website builder with tons of other services (marketing, CRM, invoicing) placing it outside my use-case
- Generates a site based on industry and name (can suggest one) - can be hacked by sending description prompt in the industry field.
- No prompt customization.
- Produces average quality visuals, but structure seems the same - hero, image, service cards, testimonial, gallery, contact info and form.

![app.durable.co result.png](/assets/images/generating-web-with-ai/app.durable.co_result.png)

## [Wix.com](http://wix.com/)

- Claims "AI technology that creates a site for you."
- Could not find AI designer.

## Debuild.app

- Joined waiting list.

## [10Web.io](http://10web.io/)

- AI web design.
- Input: describe business and 3 key services.
- Generates OK design (responsive), but does not adhere to the prompt (no search input, etc.).
- Seems more like the layout and structure is preconceived (home, service, about and contact pages) and AI only generates texts and images.
- Output > [https://10web-site.ai/52/working-troll/](https://10web-site.ai/52/working-troll/)

![10web.io result.png](/assets/images/generating-web-with-ai/10web.io_result.png)

## Sketch2Code (Microsoft)

- Site not available [https://sketch2code.azurewebsites.net/](https://sketch2code.azurewebsites.net/).

Overall, none of these tools can help me achieve my goal of designing a simple site based on my prompt.

# ChatGPT

---

Approach

- get GPT to generate code using Bootstrap

The result is closer to what I need, but it obviously needs more work to be useful.

![gpt-search.png](/assets/images/generating-web-with-ai/gpt-search.png)

![gpt-detail.png](/assets/images/generating-web-with-ai/gpt-detail.png)

# Figma plugin

---

Using figma to code plugins, one can achieve interesting results. The downside is that you need the Figma design…

Input:

![Screenshot 2023-06-30 at 8.41.47.png](/assets/images/generating-web-with-ai/Screenshot_2023-06-30_at_8.41.47.png)

Output:

![Screenshot 2023-06-30 at 8.44.47.png](/assets/images/generating-web-with-ai/Screenshot_2023-06-30_at_8.44.47.png)

# Appendix

---

## Full spec

*The MediSearch platform serves as a user-friendly medicine search engine that simplifies the process of finding pharmacies with specific medicines in stock. The website is theme is predominantly violet and features exquisite use of color gradients.*

***Homepage(Search and Result List):** On the homepage, we offer users the ability to search for medicines based on their names. Typing in the search bar, results begin to appear in a list where each row distinctively displays a combination of the medicine name and form (e.g., Coldrex Sacks, Coldrex Tablets 50mg). A keen eye would notice an in-stock indicator icon next to each medicine to swiftly inform of its availability status. Results can be further honed based on users' convenience as they have the option to sort these results by distance from their pre-estimated location.*

***Medicine Detail Page:** Post choosing a medicine from the list, users are redirected to a medicine detail page containing an array of pharmacy cards. Each card leaves no stone unturned in providing all necessary information about a pharmacy – its name, address, phone number, and operation hours. Further, a compactly fitting map ensures users do not have to scour the internet for directions.*

***Email Subscription Page:** In unfortunate circumstances where a user's required medicine is out of stock in all pharmacies, we offer a silver lining - an option to subscribe for email notifications about the medicine's availability status.*

## GPT prompt

You are a web developer with design capabilities. You will take a description (see below), enhance it by inserting details written in between the lines and based on the enhanced description build the html code split to individual pages.

Website description:
{{website description}}

Design requirements:
{{design requirements}}

Here are a few rules to observe:

- output complete HTML using Slim lang syntax
- use Bootstrap as the CSS framework, its components and utility classes
- make sure you properly place elements (by adding padding / margin as necessary)
- when relevant use icons (for example state indicators, input field icons (email, phone, location, etc.)
- use (but don't overuse) primary color for main actions and secondary color for other actions
- when designing sub-pages, include bread crumbs
- include aria roles and attributes for accessibility

## [uizard.io](http://uizard.io) prompt

Search engine simplifying the process of finding pharmacies with specific medicines. Page 1: Search by medicine name and view results with in-stock indicators. Sort results by distance. Page 2: Medicine detail showing which pharmacies have it in stock, with info about each pharmacy (address, opening hours.)

*There was another one I was trying but was lost in time..*