# React Router Catch-All Route Issue

This repository demonstrates a common issue in React Router v6 where a catch-all route (`/*`) unintentionally intercepts all other routes, preventing them from ever being matched.  This typically occurs when the catch-all route is defined after more specific routes.

## Problem

The provided `App.js` demonstrates the problem. Even though routes like `/about` are defined, the catch-all route `/*` always matches first, leading to the `NotFound` component being rendered regardless of the URL.

## Solution

The `AppSolution.js` file provides a solution. By placing the catch-all route (`/*`) *before* all other routes, React Router correctly handles route matching. Specific routes are matched first, and only if no other route matches does the catch-all route take effect.