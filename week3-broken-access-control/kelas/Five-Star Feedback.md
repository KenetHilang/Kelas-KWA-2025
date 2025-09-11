# Five-Star Feedback Write-Up
> **Source:** https://juice-shop.herokuapp.com/#/score-board?categories=Broken%20Access%20Control

## Overview

**Title:** Five-Star Feedback

**Category:** Broken Access Control

The "Five-Star Feedback" challenge requires to manipulate the review system of a web application by deleting all five-star reviews.

## Solution

### 1. Accessing the Administration Page
> Log in into the admin account as usual, using `' OR True --`, and then access the admin page

![alt text](./assets/Five-Star%20Feedback/20250911_11h27m52s_grim.png)


### 2. Deleting the Five-Star Review
> Search for the five star review and then delete the five star review

![alt text](./assets/Five-Star%20Feedback/20250911_11h27m13s_grim.png)


### Solution Explanation

The challenge was completed by exploiting insufficient access control measures that should restrict the deletion of feedback to authorized personnel only, and even then, should not allow mass deletions without proper oversight.
