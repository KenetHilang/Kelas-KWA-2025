# Forged Review Write-Up
> **Source:** https://juice-shop.herokuapp.com/#/score-board?categories=Broken%20Access%20Control

## Overview

**Title:** Forged Review

**Category:** Broken Access Control

This challenge involves manipulating the review submission process in a web application to post reviews as another user, exploiting weak access control mechanisms.

## Solution

## Solution

### 1. Understanding the Web's Review Mechanism
> Initially, submit a generic review through the application's interface to understand how the review submission process works.

![alt text](20250911_12h24m55s_grim.png) 

> Using Burp Suite, capture the HTTP request sent when review is submitted. Analyze the request to understand its structure and the parameters it includes.

![alt text](20250911_12h25m37s_grim.png) 

### 2. Exploiting the Vulnerability
> Modify the "user_id" parameter in the intercepted request to the ID of another user, preferably a user with higher privileges like an admin, to test if the application enforces proper authorization checks.

![alt text](20250911_12h26m02s_grim.png) 

> Resend the modified request to see if the review gets posted under the changed user ID.

![alt text](20250911_12h26m11s_grim.png) 

> Verify the review in the web app

![alt text](20250911_12h26m41s_grim.png)

### Solution Explanation

The challenge highlighted significant security flaws related to input validation and session management, such as the server failed to validate if the logged-in user matched the "author" of the review. The application did not properly secure review IDs, allowing an attacker to modify any review by simply knowing its ID.
