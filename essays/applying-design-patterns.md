---
layout: essay
type: essay
title: "Applying Design Patterns"
# All dates must be YYYY-MM-DD format!
date: 2023-11-28
published: true
labels:
  - Software Engineering
  - Javascript
  - Design Patterns
---

## Defining design patterns
The whole reason we write code in the first place is to make our lives as human beings easier. We gain immense productivity from automating non-trivial tasks that humans cannot complete consistently and timely through technology. Through technology,
we 
can message anyone on the globe practically instantaneously whereas without technology we would have to rely on something like mailing letters to communicate. We
can purchase virtually any physical item from the internet with the click of a button whereas trying to do so without technology would be quite non-trivial. If there's some *common problem* that we need to solve, we can usually automate it.

In regards to programming, if we didn't have things like libraries, frameworks, packages, etc., we would have to rewrite a lot of code that already exists somewhere on the internet and, realistically speaking, probably works better too. 

### Design patterns as problem-solving
Design patterns have come about because programmers have realized that there are a lot of *common problems* that need to be solved. That means that in theory, we can automate those problems too.

In practice, however, there are always problems that are not so trivial that we can automate it with code. These vague, yet recurring *patterns* of problems are hard to automate, but can be solved by similar approaches. When programming applications in 
particular, we call these reusable approaches "design patterns."

In the real world, basic problem-solving skills involve recognizing patterns and knowing how to apply them to solve different problems. If you think about it, that is precisely what design patterns are: solutions to drastically different problems 
that can be reapplied to variations of such problems. Design patterns are simply a problem-solving method. When programming, we use the same approaches to solving problems in different situations because they are proven to be effective.

## Design patterns in Lendor-Vendors
Lendor-Vendors is the name of the organization and web application my team and I developed for our final project in ICS 314, Software Engineering I. It is an application that allows users to loan out their items to other users, or loan other users' items.

The app was developed with Meteor, a full-stack framework that uses React for the UI and MongoDB 
for the database. Throughout the development process, we discovered and took advantage of many design patterns provided by the Meteor stack.

### React
React is a frond-end framework that includes many features that allows you to, instead of writing tedious HTML logic, write clean and reusable components that you use flexibly and comfortably throughout your development process.

#### Reusable components
The biggest feature that React promotes is the idea of modular, reusable components. In React, everything is a component, defined as a .JSX file. Every page you see is a component. Each page is also made up of many components.

The Lendor-Vendors app has a "Gallery" page, which displays every item that is currently available for loaning. There is also a page called "Your Items" which only displays the items the current user owns. An example of reusable components lie in 
these two pages. They both display a component we defined- the Item Card.
```
const ItemCard = ({ item }) => (
  <Link id="cards-link" to={`/view_item/${item._id}`}>
    <Card className="h-100 item-card">
      <Card.Header>
        <Card.Img src={item.image} alt={`${item.title} image`} style={{ width: '100%', height: '150px', objectFit: 'cover' }} />
      </Card.Header>
      <Card.Body>
        <Card.Title>{item.title}</Card.Title>
      </Card.Body>
      {Roles.userIsInRole(Meteor.user(), 'admin') ? (
        <Container className="d-flex justify-content-start">
          <Row>
            <Col>
              <DeleteItemButton item={item} />
            </Col>
          </Row>
        </Container>
      ) : ''}
    </Card>
  </Link>
);
```
In both Gallery and Your Items, the follow piece of code displays all items: 
```
<Row xs={1} md={2} lg={3} xl={4} xxl={5} className="d-flex flex-wrap justify-content-center g-4 px-5">
  {searchPattern === '' ? (
    items.map((item, index) => <Col style={{ maxWidth: '250px' }} key={index}><ItemCard item={item} /></Col>)
  ) : (
    fuseSearch.map((searchedObj, index) => <Col style={{ maxWidth: '250px' }} key={index}><ItemCard item={searchedObj.item} /></Col>)
  )}
</Row>
```

### Model-view-controller
The model-view-controller is best explained as a system that has three components- the data model, the view that the user sees, and the controller that the user uses. 

#### Model
The data model. In the Meteor stack, this refers to MongoDB, which is the program Meteor uses for database management. On the server side of the Lendor-Vendors app is the MongoDB database that all clients access. It stores all the data the app 
needs.

MongoDB allows you to organizze your database in "collections," which are basically groups of data documents. In Lendor-Vendors, we have a variety of collections, but the key collections are:
- Items
- Requests
- ForumRequests
- Profiles

Before we even began writing code, we needed to think about how we were going to design our database. These four were the main components we came up with when brainstorming our data model. By using MongoDB, we were able to implement these four 
components seamlessly into our application by using collections.

#### View
This refers to the UI that the user interacts with. Our application is ***heavily*** styled using React-Bootstrap. Common features of React-Bootstrap we used are:
- Grid layout
- Cards
- Modals

Using the grid system Bootstrap provides, we were able to format our pages exactly the way we wanted.

#### Controller
A typical React component JSX file in our project is structured like this:

```
const JSXComponent = () => {
    // functions
    someFunction
    ...
    return (
        <ComponentThatUsesTheAboveFunctions function={someFunction} />
    );
};
```

We define whatever functions we need separately from the UI section. This way, back-end logic is *mostly* separated from the front-end HTML. This separation was a major factor in our productivity. Had we mixed and nested our logic within our 
front-end code like this:
```
const JSXComponent = () => {
    return (
        <ComponentThatUsesTheAboveFunctions function={someFunction() {
            doSomething;
        }} />
    );
};
```
it would have been a nightmare to work with. This looks fine right now, but our logic was typically complicated and required multiple lines per function:
```
const JSXComponent = () => {
    return (
        <ComponentThatUsesTheAboveFunctions function={someFunction() {
            doSomething;
            doSomethingElse;
            const something = getSomething();
            if (something.hasSomething) {
                something.modifySomething;
            }
            return something;
        }} />
    );
};
```
Hopefully it is clear how this approach can quickly become way too complex to manage.
