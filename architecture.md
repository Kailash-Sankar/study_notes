
# Architecture

### Patterns

#### Microservices

Instead of a single monolith application maintain a collection of small autonomous services based on product/business which interact with each other.
https://medium.com/@andrewvr/microservices-c8b5dbdd58b8

#### Micro Frontends

Instead of a large monolithic frontend, maintain smaller frontend repo's with their own vertical teams and independent deployment process and a container app to bring it all together.
https://martinfowler.com/articles/micro-frontends.html

#### Backends For Frontends (BFFs)

Practice of having backend for each front end application. An Android app would have it's own backend, the web application would also have it's own and then these would interact with common lower level services.
https://samnewman.io/patterns/architectural/bff/


### Concepts

#### Feature Flags/Toggles
Control system behaviour without modifying code, enable/disable features run time, based on requests or during releases.
https://martinfowler.com/articles/feature-toggles.html


#### Canary Release

#### Circuit Breaker


### Testing

#### Pyramid and Ice cream cones

The focus should be on writing more unit tests forming the base of the pyramid and going up to functional and intergration tests.
https://martinfowler.com/bliki/TestPyramid.html
https://watirmelon.blog/testing-pyramids/

#### A/B testing

