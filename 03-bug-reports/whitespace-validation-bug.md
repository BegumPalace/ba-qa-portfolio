# Bug Report - Whitespace Validation on Mandatory Field

## Bug ID
BUG-VAL-001

## Module
Request Creation Form

## Severity
Medium

## Priority
High

## Description
The system incorrectly accepts whitespace-only input in a mandatory text field.

## Preconditions
- User is on request creation screen
- Mandatory text field is visible

## Steps to Reproduce
1. Open the request creation form
2. Enter a single whitespace character into the mandatory text field
3. Click **Save**

## Actual Result
The record is saved successfully.

## Expected Result
The system must treat whitespace-only input as empty and block the save action.

## Suggested Validation Logic
Input should be trimmed before validation.

Example:
trim().isEmpty() → validation error
