# React Router Dom v6 Catch-all Route Issue

This repository demonstrates a bug in React Router Dom v6 where the catch-all route (`/*`) is triggered even when a valid route exists.  This leads to unexpected behavior and breaks navigation.

## Bug Description
The provided code creates a simple React application with three routes: a home route (`/`), an about route (`/about`), and a catch-all route (`/*`).  However, the catch-all route is always triggered, regardless of whether a valid route exists.

## Solution
The issue is caused by the placement of the catch-all route.  It needs to be placed at the end of the `Routes` component to correctly handle unmatched routes. This fix ensures that other routes are checked first, and the catch-all route is only used if no other route matches.

## How to reproduce
1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe that the catch-all route is triggered for all navigation, even when navigating to `/` or `/about`.
