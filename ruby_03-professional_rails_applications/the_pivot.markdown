---
title: The Pivot
length: 3
tags:
type: project
---

## Goals

Your Dinner Dash application was *almost* great, but it turns out that we need
to *pivot* the business model.

In this project you'll build upon an existing implementation of
[Dinner Dash]({% page_url projects/dinner_dash %}), turning it from a
restaurant ordering site to something much bigger.

### Modeling

* Adapt the existing restaurant models to belong to individual businesses
* Mind security permissions such that each business does **not** have any knowledge of other businesses' data
* Push *all* logic down to the model layer so controllers and views remain simple

### Interface & Views

* Use and switch between multiple view templates to reduce view-layer logic
* Implement a clean, logical order flow that minimizes customer frustration

### Process

* Practice working with a "legacy" codebase to add substantial functionality
* Use outside-in TDD/BDD to drive all layers of Rails development
* Use frequent commits, issues, and branches to effectively organize your features
* Use a professional project management tool to pace and track progress

### Teams

The project will be completed by teams of three to four developers over the span of three weeks.

Like all projects, individual team members are expected to:

* Seek out features and responsibilities that are uncomfortable. The time to learn is *now*.
* Support your teammates so that everyone can collaborate and contribute.

## Setup

### Project Starting Point

You'll build upon an existing code base assigned by the instructors. You need to
work on adapting and improving this codebase, not building your own thing from
scratch. This is sometimes called "brownfield" development, and you'll soon know
why.

### Exploring the Dinner Dash App

As a group, dig into the code base and pay particular attention to:

* Test coverage and quality
* Architectural concerns
* Components that are particularly strong or weak
* General strengths and weaknesses

### Beginning The Pivot

Once you've explored the base project:

* Select one member of the group who will host the canonical repository for the project
* Create a new, blank repository on GitHub named `the_pivot`
* Clone the Dinner Dash project that you'll be working with to your local machine
* Go into that project directory and `git remote rm origin`
* Add the new repository as a remote `git remote add origin git://new_repo_url`
* Push the code `git push origin master`
* In GitHub, add the other team members as collaborators
* The other team members can then fork the new repo

### Tagging the Start Point

We want to be able to easily compare the change between the start of the project and the end. For that purpose, create a tag in the repo and push it to GitHub:

* $ git tag -a dinner_dash_v1
* $ git push --tags

### Restrictions & Outside Code

Your project should evolve, refactor, and clean up the code you inherit. This includes deleting redundant, broken, or obsolete code. However, you should **not** throw out the previous work wholesale.

Furthermore, there should be *no reduction in functionality* except when explicitly called for by new requirements.

### Setup the Project Management Tool

There are many popular project management tools out there. For this project
we'll use a lightweight tool that wraps GitHub issues: [Waffle.io](https://waffle.io/)

Setup a Waffle project for your new repo. Your team members and instructors should
be added to the project so they can create, edit, and comment on issues.

## Managing Requirements

The stories as written and prioritized in your project management tool will be
the authoritative project requirements. They may go against and likely go beyond
the general requirements in this project description.

### Workflow

Generally speaking, work for your project should go through this process:

* A story is written in the project management tool, in Waffle.io this creates a Github issue 
* A developer comments on the story that they're beginning work
* They create a feature branch
* They develop and test the feature
* They push the *feature* branch to the repository
* They submit a pull request asking to merge the branch into *master* and referencing the issue containing the user story
* A teammate reviews the code for quality and functionality
* The teammate merges the pull request and closes the story/issue
* Later, the customer will review the delivered features by browsing closed
pull requests

## Pivots

Your group will be assigned one of the following problem domains to pivot Dinner Dash:

### Keevahh

Micro-lending is a powerful tool for social progress. Let's rework Dinner Dash
into a micro-lending platform.

* Users register on the site as either a borrower (*the business*) or a lender
(*the customer*)
* Borrowers automatically have a borrower page (*the store*)
* Within that borrower page, they post one or more loan requests (*the products*)
* A loan request has a title, description, categories, photos, borrowing amount, requested-by
date, a repayments-begin date, and a repayment rate
* A lender can browse the site and view all open loan requests
* They can add multiple loan requests from multiple borrowers to their cart
* They can then checkout and the funds are allocated to the borrowers
* The borrowers are notified that funding has come through and their loan request
page is updated

Lending like this is more fun together -- it'd be great if lenders could band
together into lending groups that make loans together on a weekly or monthly basis.

### EmployMe

Employment is key to quality of life. Let's rework our Dinner Dash into a platform
to help people find great jobs.

* Users register on the site as either a job poster (*the business*) or a job seeker (*the customer*)
* A business has a job listings page with all their job listings
* The business can create one or more job listing
* A listing has a title, description, categories, full-time/part-time indicator,
wage/salary range, number of positions open, and a closing date
* A job seeker can browse the site and view all open job listings
* They can add one or more job listings to their cart
* They can upload a PDF resume that's attached to their user account
* During the "checkout" process, they can add a brief introduction note to each job they're
applying for
* The job posters are notified that a new application has come in

The job posters will need a great dashboard where they can review the applicants
and either send them rejections or schedule interviews.

### Airlift

Technology has a huge role to play in disaster relief and recovery. Let's rework
Dinner Dash to help get relief supplies to the people and places that need them.

* Users register on the site as either suppliers (*the business*) or relief
providers (*the customer*)
* A supplier has a listings page with all their available supplies
* A listing has a title, description, categories, quantity available, unit size,
current location, shippable indicator, unit weight
* A relief provider can browse the site and view all available supplies
* They can add one or more supplies to their cart
* During checkout relief providers can choose to (a) pickup the supplies and request a
pickup day/time or (b) request delivery and set their current location using GPS coordinates
* The suppliers are notifed that a new request has come in

Disaster areas probably don't have desktops, electricity, and internet
access. This project needs to be built targeting *mobile web* and *SMS* where
appropriate.

### TravelHome

Experiencing other cultures is one of the strongest ways to build our understanding
of humanity. Let's make it easier for people to open their homes to travelers.

* Users register on the site and can be both hosts (*the business*) and travelers
(*the customer*)
* A host has a listings page where they list available accommodations and they
have a profile with their photo, name, and description
* A listing has a title, description, categories, quantity available, people-per-unit,
daily rate, photos, location, shared/private bathroom indicator, and available dates
* A traveler can browse the site and view all available listings
* They can add one or more listings along with requested dates to their cart
* Their profile has their name, photo, and previous bookings
* When they checkout, the hosts are notified of the requests
* The hosts can either confirm or deny the requests
* The traveler is notified when request status changes

A traveler will need a good way to roll up all their bookings into
an itinerary that helps them get from place to place with a map and pushes data
to their Google Calendar.

### FreshThreads

Off-the-rack clothes are so blah. Let's build a marketplace for buying custom clothing.

* Users register on the site as either sellers or buyers
* Sellers have a "store" page where they can post one or more items
* An item has a title, photos, a detailed description, and a time-to-produce
* Each item can also have one or more "options" defined by the seller such as: waist size,
color, fabric, sleeve length, etc. These must be chosen by the seller when creating/editing
the item and allow them to set specific values (like "S", "M", "L", etc or "Short", "Regular", "Long")
* Customers can browse all items on the platform or browse a specific seller's store
* When a customer adds an item to their cart they need to specify each of the options
* When the order is submitted the customer is emailed a receipt and the seller
is notified to begin production.

It's a pain to enter my options for EVERY purchase. Allow a user to store
their options in their account, so when they purchase an item the right values
are pre-selected (but can still be changed).

### Gallery

People hated our restaurant, but they loved our product photos. Let's pivot
the platform to sell photography, providing our customers a "whitelabel" experience:

* A photographer registers on the platform to create a new store
* A photographer posts photos for sale
* A photo has an image, dimensions, title, description,
shooting date, and photographed by attributes.
* A customer visits a store at a URL like example.com/stores/store_name
* The customer sees only the photos for this store
* The customer can browse photos and add them to the cart
* There is no aggregated shopping experience across stores, so a customer who
visits Store A and adds something to their cart, then visits Store B, will not
see the Store A item in the Store B cart
* The customer can checkout and receives an email receipt
* A photograph which is purchased is marked as purchased, can still be browsed,
but cannot be ordered by other users
* The photographer is notified via email about the purchase.

And, one more thing: it takes awhile to save up for these amazing photographs.
It'd be awesome if a user could "favorite" photos to come back and easily
find/purchase them later.

### HubStub

Who wants to stand in line for tickets the day they come out? Nobody. Instead you
can just pay 50-500% more to buy them from someone else. HubStub helps you do
just that!

* Users register on the site and can both sell tickets (*the business*) or buy tickets
(*the customer*)
* Sellers automatically have a tickets-for-sale page (*the store*)
* Within that seller page, they post one or more available items (*the products*)
* An item has an event title, date, time, section, seat number(s), categories, photos, and a delivery method (download or mail)
* A buyer can browse the site and view all available tickets or browse them
grouped by event or seller
* They can add multiple tickets from multiple sellers to their cart
* They can then checkout and the tickets are either downloaded or the seller is
notified that they need to mail them

Shows and events are more fun together. Can you create a way to invite my friends
and have them RSVP?

## Expectations

You are to extend Dinner Dash so that it can handle multiple, simultaneous businesses. Each business has their own name, unique URL pattern, items, orders, and administrators.

<div class='note'>
<p>The requirements reference an <b>example.com</b>, but your URL will differ.</p>
</div>

### Functional Requirements

Individual restaurants can be accessed by specifying their restaurant name as the path prefix.

* Given a business named _Billy's BBQ_
* When I visit `http://example.com/billys-bbq`
* Then I expect to see all items defined for _Billy's BBQ_
* And I expect to see branding defined for _Billy's BBQ_
* When I visit `http://example.com/billys-bbq/categories`
* Then I expect to see all categories defined for _Billy's BBQ_

#### Public Visitor

As a public, unauthenticated visitor to a business I can:

* Maintain a **shared** shopping cart across all businesses I browse
* Add items to a shopping cart
* Log in to or create an account before completing checkout
   * When I create an account, then I expect to receive a welcome email
   * After login or creating an account, I will **immediately** resume the checkout process
* Request that my account become a business owner

#### Authenticated Customer

As an authenticated customer I can:

* Make purchases on any business I am browsing
  * Receive an email confirmation of my order with basic order details and a link to the order detail page
* Manage my account information shared by all businesses centrally on my account page
  * Shipping addresses
  * Billing addresses
  * Credit cards associated with my account
  * Basic account info like name and password, as managed previously in Dinner Dash v1
* View and manage my purchase history across all businesses

#### Creating a Business

* An account can request to create a new business that includes a name,
URL identifier ("slug"), and description
* The platform administrators are notified of the pending request
* If approved...
  * the requester is notified by email
  * the requester automatically becomes a business administrator for the business
* If denied...
  * the requester is notified by email

#### Authenticated Business Administrator

As an authenticated business admin, by using a dedicated admin area, I can:

* Add items, edit items, and retire listings in my business only
* Update the details of my business such as the: name, URL identifier, and description
* Add or remove other admins for the business
    * There can never be fewer than 1 admin for a business
* Perform the admin actions available to administrators in Dinner Dash as appropriate

#### Authenticated Platform Administrator

As an authenticated Platform Administrator, I can:

* Approve or decline the creation of new businesses
* Take a restaurant "offline" temporarily so that attempting to browse it redirects its root and displays a maintenance message
  * Bring an offline restaurant back online
* Override/assist restaurant admins in any functionality available to them via the admin portion of their restaurant pages

#### Validation and Error Messages

Any form in the application must:

* validate the submitted data appropriately
* reject invalid input
* display clear and helpful errors and corrective instructions
* allow the user to quickly fix and resubmit

### Non-Functional Requirements

#### Background Workers

Use background workers for any job that doesn't **have to** be completed before the response is sent to the user (ex: sending email, updating statistics, etc).

Use Resque or a similar library to support this functionality.

#### Security

Your app needs to be secure enough that a malicious user with complete knowledge
of the source code cannot exploit the system (ie: change other users' data, view
other users' data, elevate their own privlege level, etc).

### Base Data

Before final delivery, and ideally before customer check-ins, you should have the following data pre-loaded in your marketplace:

* At least 500 total businesses
* At least 25 categories
* At least 1,000 listings per category
* At least 500 known customers
* At least 10 orders per customer
* 1 business admin per business (jmejia@turing.io)
* 1 platform administrators (jorge@turing.io)

It creates a much stronger impression of your site if the data is plausible. We recommend creating a few "template" businesses that have real listings, then replicating those as needed. It's better to have "Taste of India 26" and "Taste of India 27" than "Lorem Ipsum" and "Tellus Domit".

### Extensions

In this project you as developers are expected to take a more active role in shaping the project. Although there are a few potential extensions proposed at the outset, you are encouraged to propose additional extensions, in the form of new features and user stories describing them, to your project manager.

If you have an idea for a killer feature for your application, pitch it to your stakeholders for refinement. If they are convinced of its value, they'll work with your team to create one or more user stories in your project management software and prioritize those stories in the context of the rest of the requirements. You may be able to convince them to prioritize your feature ahead of current base requirements if it is sufficiently compelling or necessary.

**However**, your application should not implement features which have not been approved
by your customer.

#### Dashboard

As a business admin, you should have access to a business dashboard that will give you actionable data to make business decisions. This dashboard should include:

* Top 10 customers by revenue
* Top 10 customers by units purchased
* Top 20 products by revenue
* Top 20 products by units sold
* Top 10 orders by revenue
* Top 10 orders by units sold
* Top 10 days by revenue

#### Custom CSS per Business

Provide a mechanism so that business administrators may provide custom a CSS sheet to change the appearance of their listing page. This custom styling should not affect any other business's appearance.

Have four pre-built themes they can select from and the ability to upload their own.

#### Use Sub-Domains To Distinguish Businesses

In order to give greater precedence and more SEO-juice to each individual business, as well as pave the way for businesses to use custom domains, change your application so that, instead of using a path prefix per request to identify individual businesses in the system, use unique sub-domains instead.

So instead of `http://www.example.com/billys-bbq/items` pointing to the items belonging to the business _Billy's BBQ_, allow `http://billys-bbq.example.com/items` to be used instead.

## Evaluations

### Feedback / Evaluation Schedule

Rapid and frequent feedback about the work we produce is a central tenet of agile software development. As such, we'll have frequent meetings to discuss the state of your project and correct course as necessary.

These meetings are intended to model interactions with a *real customer*, they are not support sessions. As the stories clearly define the customer's expectations, your application needs to **exactly** follow the stories as they've been developed with your customer. A 95% implementation is wrong.

If you want to deviate from the story as it's written, you need to discuss that with your customer and get approval to change the story *first*.

### Evaluation Rubric

The following criteria will be used for your project's evaluation:

#### Feature Delivery

You'll be graded on each of the criteria below with a score of (1) well below
expectations, (2) below expectations, (3) as expected, (4) better than expected.

**1. Completion**

* 4: Team completed all the user stories and requirements set by the client in timely manner.
* 3: Team completed all the user stories and requirements set by the client.
* 2: Team completed most of all the user stories and requirements set by the client.
* 1: Team completed the user stories and requirements partially.

**2. Organization**

* 4: Team used a project management tool and updated their progress in real-time.
* 3: Team used a project management tool to keep their project organized.
* 2: Team used a project management tool but didn't update the progress frequently.
* 1: Team failed to use a project management tool to track its progress.

**3. Progress**

* 4: Team delivered all the requested features on all iterations.
* 3: Team delivered all the requested features on all but one iteration.
* 2: Team delivered all the requested features on all but two iterations.
* 1: Team failed to delivered requested features on three or more iterations.

#### Technical Quality

**1. Test-Driven Development**

* 4: Project shows exceptional use of testing at different layers (above 95% coverage).
* 3: Project shows adequate testing (90% - 95% coverage).
* 2: Project shows gaps in test usage/coverage/design (85 - 90% coverage).
* 1: Project lacks sufficient testing (under 85% coverage).

**2. Code Quality**

* 4: Project demonstrates exceptionally well factored code.
* 3: Project demonstrates solid code quality and MVC principles.
* 2: Project demonstrates some gaps in code quality and/or application of MVC principles.
* 1: Project demonstrates poor factoring and/or understanding of MVC.

**3. User Experience**

* 4: Project exhibits a production-ready and polished UX.
* 3: Project exhibits a production-ready user experience.
* 2: Project exhibits some gaps in the UX.
* 1: Project exhibits inattention to the user experience.
