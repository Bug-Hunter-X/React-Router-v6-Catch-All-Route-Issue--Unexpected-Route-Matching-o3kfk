# React Router v6 Catch-All Route Bug

This repository demonstrates a subtle bug in React Router v6 related to the catch-all route (`/*`).  The issue occurs when the catch-all route unexpectedly overrides more specific routes, even if a more specific route should match first. This appears to be linked to route nesting or the presence of dynamic segments.

## Bug Reproduction

The `bug.js` file contains a minimal reproducible example.  Navigate to `/` and `/about`.  The issue manifests when the catch-all route `/` unexpectedly takes precedence over the others causing improper route matching.

## Solution

The `bugSolution.js` file provides a corrected version. The solution involves carefully considering the order of routes and utilizing more specific catch-all routes only after all other route matches are exhausted.