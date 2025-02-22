# Next.js 15: Unexpected Runtime Errors from Typo in Import Statement

This repository demonstrates a subtle bug in Next.js 15 where a simple typo in an `import` statement can lead to unexpected runtime errors. The error messages are not always helpful in identifying the root cause.

## Bug Description

The issue arises when there's a misspelling in an import statement, particularly when dealing with components from a library that has `react` as a dependency. Instead of a clear compiler error, Next.js 15 might throw an opaque runtime error, making debugging challenging.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm run dev` to start the development server.
4. Navigate to `/about` page; the app should crash with a runtime error.

## Solution

The solution is straightforward: Correct the typo in the `import` statement. In this case, changing `import {React} from 'react';` to `import React from 'react';` resolves the issue.