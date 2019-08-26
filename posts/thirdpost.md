---
title: Sprint 3 Reflection
description: Reflecting on ELECTRA's progress this week.
date: 2019-08-23
tags:
  - electra
  - project-management
  - backend
  - cleanup
layout: layouts/post.njk
---
## Backend Cleanup
This week Dandy & I worked to cleanup the backend code. Specifically, we documented the controller and model functions, standardized naming conventions, and organized our backend architecture. While this may not seem productive, clean code helps future project work run smoothly. It makes the code readable and accessible, which helps developers, team members, and users alike.

Here's an example of function documentation:

``` js/2/4
/**
 * Gets all the users in the database
 * @param {object} response
 * @param {object} request
 * @param {object} next
 * @returns {object} A JSON object of all users
 */
exports.getUsers = async (request, response, next) => {
  try {
    const all_users = await Users.select();
    return response.send(all_users);
  } catch (err) {
    next(err);
  }
};
```
