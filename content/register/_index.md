---
title: "Register"
description: "Join ROBU - Robotics Club of BRAC University"
date: 2024-01-01
type: "page"
layout: "simple"
---

# Join ROBU

Welcome to the registration page for the Robotics Club of BRAC University (ROBU)!

## How to Register

To become a member of ROBU, please follow these steps:

1. **Visit our registration portal**: <span id="registration-link"><a href="https://registration.bracurobu.com" target="_blank" rel="noopener noreferrer">https://registration.bracurobu.com</a></span>
2. **Complete the registration form** with your details
3. **Wait for interview call** - if your application is successful, you'll be contacted for an interview
4. **Attend mandatory free course (will require some tools, can be self-sourced or bought from us)** - "Basics of Robotics" (required for all new members)

<script>
  (function () {
    var linkWrapper = document.getElementById('registration-link');
    if (!linkWrapper) return;
    var closedText = '[Registration Server is currently Closed]';
    try {
      fetch('https://api.registration.bracurobu.com/health', { method: 'GET', cache: 'no-store' })
        .then(function (res) { return res.ok ? res.json() : Promise.reject(new Error('Bad status ' + res.status)); })
        .then(function (json) {
          if (!json || json.status !== 'ok') linkWrapper.textContent = closedText;
        })
        .catch(function () { linkWrapper.textContent = closedText; });
    } catch (e) {
      linkWrapper.textContent = closedText;
    }
  })();
</script>

## Membership Benefits

- Access to robotics workshops and training sessions
- Use of club equipment and resources
- Networking opportunities with fellow robotics enthusiasts
- Mentorship from senior members
- Form your own official crew

## Requirements

- Must be a current student of BRAC University
- Interest in robotics, programming, or engineering
- Commitment to participate in club activities

## Contact

For any questions about registration, please contact us through our social media channels or visit our club office.

*Registration is currently closed. Stay tuned till next club fair*
