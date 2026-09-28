# Foodi

> **Showcase page.** This repository is a public showcase of a **private repository**:
> it contains a description of the work only, with **no source code**.

An **Uber Eats-style food-delivery platform**: four native mobile apps on a single shared backend, with AI features for restaurant onboarding.

## The four apps, one backend

| App | Who it serves |
|---|---|
| Customer | Diners browse, order and track |
| Restaurant | Restaurants manage menu and orders |
| Rider | Riders accept jobs, collect with a pickup PIN, deliver with an OTP |
| Admin | Operations approve restaurants and riders, and view orders |

## Order flow

```
place order -> restaurant accepts -> preparing -> ready
  -> rider enters PICKUP PIN at the restaurant -> picked up
  -> rider enters DELIVERY OTP at the door -> delivered
```

The PIN and OTP handoffs make each change of custody provable, which is what stops disputes between restaurant, rider and customer.

## What I built

- Monorepo with a shared package holding types, the order state machine and formatting, imported by every app
- Customer app in Expo with routing, browsing, ordering and live tracking
- Postgres schema, migrations and seed data
- AI features: one-click menu builder, theme suggestions and smart search

## Stack

Expo (SDK 56), React Native, React 19, expo-router, TypeScript, Supabase (Postgres, auth, realtime, storage, edge functions), Claude API

---

*Source code is private. This page documents the work; code can be shared on request.*
