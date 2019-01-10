---
id: best-practices
title: Production Best Practices (Security)
sidebar_label: Production Best Practices (Security)
---

### Uses safe version of Express

Since, Express 2.x and 3.x are no longer maintained, we use 4.1.0 which is not vulnerable to security attacks

### Uses Helmet

Helmet can help protect your app from some well-known web vulnerabilities by setting HTTP headers appropriately.

Helmet is actually just a collection of smaller middleware functions that set security-related HTTP response headers.

### Uses cookies securely

To ensure cookies don’t open your app to exploits, we don’t use the default session cookie name and set cookie security options appropriately.
