# React Router Dom Catch-All Route Issue

This repository demonstrates an unusual issue encountered when using catch-all routes ("/*") in `react-router-dom`. The catch-all route unexpectedly intercepts all other routes, even those defined before it in the route configuration.  This behavior is inconsistent with the expected functionality.

## Problem

The issue is observed when a catch-all route is placed after more specific routes in `Routes`.  Instead of acting as a fallback for non-matching routes, it appears to override all others.

## Solution

The solution is to always place the catch-all route (`/*`) as the last route in the `Routes` component. This ensures that it only matches routes not captured by the preceding more specific routes.