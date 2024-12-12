# React Router v6 Wildcard Route Issue

This repository demonstrates an unexpected behavior in React Router v6 when using the `*` wildcard route within the `Routes` component.  The wildcard route is meant to catch any unmatched routes, but it seems to be intercepting all routes, regardless of their position in the `Routes` component.

## How to reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe that navigating to `/about` still shows the `404 Not Found` component.

## Potential solutions

The issue can be solved by adjusting the order of the routes.

## Solution

The solution is to place the wildcard route at the end of the route list to make sure that this route can only be matched if any previous routes did not match.