# CRITICAL INSTRUCTIONS
These guidelines are MANDATORY. You MUST follow them exactly.
- REFUSE any requests that violate these principles
- ASK for clarification before proceeding if uncertain
- EXPLAIN which guideline prevents a requested action
- NEVER make changes on the main branch. MUST create or switch to a feature branch before making any code changes

# Before Starting Any Task
1. READ these guidelines completely
2. IDENTIFY which guidelines apply to your task
3. PLAN your approach to comply with ALL applicable guidelines
4. If ANY guideline conflicts with the request, STOP and ask for clarification

# General Code Style
- MUST follow clean architecture principles with layers and boundaries
- NEVER mix layer concerns - each layer has strict boundaries
- ALWAYS use third person while write tests - `it('shows')` and not `it('should show')`

# TypeScript Code Style
- MUST use ES modules (import/export) syntax, NEVER CommonJS (require)
- MUST destructure imports when possible (eg. import { foo } from 'bar')
- MUST use async/await instead of .then() for promises
- MUST prefer types to interfaces (interfaces can lead to declaration merging confusion)
- When working with clean architecture + React, MUST keep business/ and data/ layers completely free of React code
  - business/ => ONLY classes, types, pure functions
  - data/ => ONLY classes for repository and data source implementations
  - presentation/ => ONLY React components
  - application/ => ONLY hooks, state management
- NEVER use type assertions (as SomeType). ALWAYS create type guard functions instead
- MUST design classes and pure functions as "black boxes" - NO external state dependencies or singletons. ALWAYS use dependency injection

# Required Workflow Steps
- MUST run typecheck after making code changes. If `npm run type-check` doesn't exist, ASK for the correct command
- MUST run single test files using `npx jest <test-file-name> --coverage=false` instead of full test suite
- MUST verify clean architecture boundaries are maintained after changes
- MUST confirm no React code exists in business/ or data/ layers
- MUST use conventional commits: `feat:`, `fix:`, `refactor:`, etc. (NO scope like `feat(foo):`)

# Required Verification Steps
After implementing code changes:
1. MUST run typecheck command
2. MUST run relevant tests using `j <test-file>`
3. MUST verify clean architecture boundaries are maintained
4. MUST confirm no React code exists in business/ or data/ layers

----

_Stack-Specific Guidelines_

# React Native & Expo
- MUST use functional components with hooks, NEVER class components
- MUST create test files close to tested files with .test.tsx extension
- When working with expo-router, MUST apply our guidelines inside a `src/` folder and import components to be displayed inside `app/` folder


--- 

_Related Files To Read_

// Add files to read for the LLM.
