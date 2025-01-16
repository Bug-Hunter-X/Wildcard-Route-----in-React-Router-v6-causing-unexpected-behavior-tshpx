# React Router v6 Wildcard Route Issue

This repository demonstrates a common issue encountered when using the wildcard route `/*` in React Router v6.  The issue arises when this wildcard route is placed after more specific routes, causing unexpected behavior where the wildcard route always matches, even if a more specific route should have precedence.

## Problem

The provided example uses three routes: `/`, `/about`, and the wildcard route `/*`.  Intention is to have `/` and `/about` routes handle their respective paths, and the wildcard route to handle all other unmatched paths. However, the wildcard route always matches, effectively overriding the other routes.

## Solution

The solution involves correctly ordering the routes in the `Routes` component.  The wildcard route should always be placed last, ensuring that it only matches routes that haven't been matched by previous, more specific, routes.