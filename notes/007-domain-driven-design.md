# Domain-driven design (DDD)

Every software is based on a specific domain. Only by eliciting requirements, you can understand it. If well designed, the architecture reflects the domain.

That's when **Domain-driven Desing (DDD)** comes in handy!

What are the basics of DDD? 

First things first, we should not be alone in our job: among the different stakeholders, we need a **Domain Expert (DE)** that has expertise in that domain. The more we communicate with the Domain Expert, the more detailed our knowledge of the domain is.

But there's a problem: what if the DE uses some terms that are not shared with the dev team?

Like, for the DE, a video is a *Clip*, but for the devs, it is called *Video*.

The communication - and the docs - become a mess; that's why we need **Ubiquitous Language (UL)**. 

UL simplifies communication and improves the domain understanding among every team member. We should use it in docs, code, tests, diagrams... everywhere! Of course, it may evolve as we understand better the domain 🐒

## Entities, Value Objects, Aggregates

In DDD there are 3 fundamental blocks: 

🔸Entities
🔸Value objects
🔸Aggregates

What do they mean?

### Entities

Entities **are objects defined by their identity** and not their attributes

Think of the `User(id, username, age)` object.

`(1, Davide, 29)` and `(573, Davide, 29)` have the same attributes, but a different ID. Thus they are 2 different entities.

This means that **Entities are mutable**: you can update the second user as `(573, Davide, 45)`, but since the ID is the same, it represents the same object.

### Value Objects

They are the opposite of Entities: **objects are not defined by their attributes** rather than by an ID.

Think of a Cloudinary-like `Image(URL, width, height)`

It's the combination of its attributes that define the Object. If you change its height, the image will be another one.

### Aggregates

Aggregates are groupings of Entities and Value objects, **treated as a single object**.

Think of `UserProfile(User, Image)`.

Aggregates simplify how we manage complex objects!

### A recap

👨‍🏫 Domain Expert: who know everything about the domain
🗣 Ubiquitous language: shared terms to simplify communication

💳 Entities: Different IDs -> different objects
👯‍♂️ Value Objects: different Attributes -> different objects
🏗 Aggregates: Entities + Value Objects


Even with Entities, Value Object, and Aggregate, complex domains can be difficult to manage: we will need to split the domain into smaller parts!
