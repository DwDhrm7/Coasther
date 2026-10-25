# Coasther

**A boarding-house (kost) mobile app: browse rooms, manage a tenancy, and track electricity, water, and payments from one place.**

Coasther is the tenant-facing React Native app of **COASTHER**, a smart boarding-house system. In the full system, ESP32 meters (PZEM-004T for power, YF-S201 for water flow) report usage over MQTT/HiveMQ. This repository contains the mobile app, which currently runs on **dummy data** for demonstration.

## Features

- **Login and profile**: sign-in screen, profile card, and edit-profile form.
- **Home**: banner, recommended rooms, facilities, location info, and resident reviews.
- **Rooms**: room list with a filter bar, and a detail page with images, facilities, description, reviews, and a booking button.
- **Tenant dashboard**: usage summary (electricity and water), payment history and detail, announcements, and quick actions.
- **Maps**: Google Maps integration for the property location.

## Tech stack

React Native 0.82, TypeScript, React Navigation (native stack), `react-native-maps`, `react-native-vector-icons`.

## Getting started

Requires Node.js, Android Studio (or Xcode on macOS), and a Google Maps API key for the map screen.

```bash
git clone https://github.com/DwDhrm7/Coasther.git
cd Coasther
npm install
```

Android setup:

1. In `android/app/src/main`, rename `AndroidManifest1.xml` to `AndroidManifest.xml`.
2. Add your own Google Maps API key to that file. Do not commit the key.

Run the app:

```bash
npm start            # start Metro
npm run android      # run on Android
```

## Project structure

```
src/
  components/   Home, Room, RoomDetail, Dashboard, Profile, Login, shared Header/Navbar
  App.tsx       Navigation setup
  assets/       Images
```

## Status

A team project built with [@GungNanda](https://github.com/zeppyx13). The app uses dummy data; wiring it to the live MQTT/IoT backend and a real payment flow is future work.
