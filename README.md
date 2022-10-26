# Intro to Identity and Access Management

## Learning Goals

- Create an application that requires users to authenticate with Flask-Login.
- Retrieve data from cookies to allow users to access data from previous
  sessions.
- Authorize users to access different sets of resources based on their
  attributes.
- Establish database rules through SQLAlchemy to encrypt passwords and protect
  users' private information.

***

## Key Vocab

- **Identity and Access Management (IAM)**: a subfield of software engineering that
  focuses on users, their attributes, their login information, and the resources
  that they are allowed to access.
- **Authentication**: proving one's identity to an application in order to
  access protected information; logging in.
- **Authorization**: allowing or disallowing access to resources based on a
  user's attributes.
- **Session**: the time between a user logging in and logging out of a web
  application.
- **Cookie**: data from a web application that is stored by the browser. The
  application can retrieve this data during subsequent sessions.

***

## Introduction

In our lessons up to this point, we have made websites that provide equal
experiences to all users. This is perfect for certain types of websites, but
most today aim to provide a tailored experience to the user. This requires
a web application to keep track of the user through a **digital identity**.

Some companies like Meta are striving to make digital identities into close
analogues for real identities, but most digital identities are fairly simple:
a collection of traits that, when combined, uniquely identify a user of the
application. If this sounds an awful lot like a database record, you're on
the right track.

Digital identities can be stored in databases as records or in special
**directory services** using a protocol called Lightweight Directory
Access Protocol (or LDAP). For simplicity's sake, we will just be using SQLite
in this module.

"Access Management" describes how we determine which identities have the rights
to create, retrieve, update, or delete specific information. You've already seen
this in the "Chatterbox" lab from this Phase- you could retrieve any message,
but you could only create, update, or delete your own. Applications carry out
access management through a combination of identity information and
**authorization** policies that state which users can access what. These
policies are usually designed for roles or groups (e.g. Teacher, Science
Teachers) rather than identity-by-identity.

Identity and Access Management (IAM) is a broad and rapidly evolving field
underneath the software umbrella, and is thus typically carried out by a team of
specialists rather than full-stack generalists. That being said, an
understanding and appreciation of the field's basic concepts will allow you to
start building identity-tailored applications in your career and on your own.

***

## Resources

- [Introduction to Identity and Access Management (IAM) - auth0](https://auth0.com/docs/get-started/identity-fundamentals/identity-and-access-management)
- [Flask-Login](https://flask-login.readthedocs.io/en/latest/)
