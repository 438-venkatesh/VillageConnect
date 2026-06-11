# VillageConnect

Rural community app for village residents and panchayat (Sarpanch) — announcements, directory, marketplace, grievances, groups, and more.

## Stack

- **Frontend:** Expo 51 / React Native (iOS, Android, Web)
- **Backend:** Node.js, Express, MongoDB Atlas
- **Auth:** Phone OTP (demo OTP: `1234`)

## Quick start

### API

```bash
cd server
cp .env.example .env   # add MongoDB URI + JWT_SECRET
npm install
npm run seed
npm run dev
```

Local API runs at `http://192.168.1.8:4000` (development only). Update the IP in `src/config/api.js` if your Wi-Fi address differs.

### App (uses LAN API)

The app calls **`http://192.168.1.8:4000/api`** (see `src/config/api.js`). Start the API server first on the host machine.

```bash
npm install
npx expo start
```

### Build APK

```bash
npx eas build -p android --profile preview
```

Or local APK: `npx expo run:android`

## Demo logins (after seed)

| Role | Phone | OTP |
|------|-------|-----|
| Resident | `9876543210` | `1234` |
| Sarpanch | `9876599887` | `1234` |

Sarpanch can post announcements and manage village grievances under **Help → Village Complaints**.
