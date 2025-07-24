# 📣 WackyFlip-Push

**Push Notification Services for the [Wacky Flip](https://wackyflip.com) Universe**

Timely alerts. Engaged players. Better retention.

`WackyFlip-Push` handles all push notifications across platforms — from tournament updates and reward reminders to feature announcements and engagement campaigns. Designed for scalability, personalization, and precision delivery.

---

## 🚀 Key Features

* 🔔 **Cross-Platform Push** (Web, iOS, Android, Desktop)
* 🎯 **Targeted Campaigns** (user segments, region, behavior-based)
* 🏆 **Tournament Alerts** (leaderboard shifts, countdowns, winner announcements)
* 🎁 **Reward & Event Reminders** (daily login, bonus ready, new challenges)
* 📬 **In-App Message Sync** (pairs with inbox systems for fallback visibility)
* 📊 **Delivery & Engagement Metrics** via [`WackyFlip-Stats`](https://github.com/wackyflipgame/WackyFlip-Stats)

---

## 📦 Repository Structure

```
WackyFlip-Push/
├── services/              # Push delivery logic per platform (FCM, APNs, WebPush)
├── scheduler/             # CRONs for campaign dispatch & retries
├── templates/             # Localized message templates
├── triggers/              # Hooks from other systems (tournaments, rewards)
├── config/                # TTLs, frequency caps, quiet hours, opt-in settings
├── integrations/          # Connectors (Auth, Stats, Leaderboards)
├── tests/                 # Unit + integration tests
└── README.md
```

---

## 🔗 System Integrations

| Source System               | Triggered Push Type                  |
| --------------------------- | ------------------------------------ |
| `WackyFlip-Tournaments`     | Match reminders, countdowns, results |
| `WackyFlip-Rewards`         | Daily bonus ready, milestone reached |
| `WackyFlip-ContentPipeline` | New game drops, updates available    |
| `WackyFlip-Auth`            | Welcome series, re-engagement        |
| `WackyFlip-Stats`           | Behavior-based targeting & frequency |

---

## ✍️ Example Notification Template

```json
{
  "title": "🏆 Final Hours!",
  "body": "Only 2 hours left in the Flip Royale Tournament! Get flipping!",
  "deeplink": "wackyflip://tournament/royale",
  "segments": ["active_last_3d", "joined_tournament"],
  "ttl": 7200
}
```

---

## 🔐 Permissions & Opt-In

* ✅ GDPR/CCPA compliant opt-in tracking
* 🔒 Secure token handling for FCM & APNs
* 🌐 Web push registration tied to user sessions

---

## 📈 Analytics

Push metrics automatically sent to `WackyFlip-Stats`:

* Delivery Success/Fail
* Open Rate & CTR
* Conversion Triggers (e.g. returned to app, started match)

---

## 🛠️ Developer Notes

* [docs/setup.md](docs/setup.md): Local setup & mock push server
* [docs/platform-support.md](docs/platform-support.md): FCM, APNs, WebPush config
* [docs/events.md](docs/events.md): Event hooks and trigger map

---

## 📌 Future Plans

* 🧠 ML-based send-time optimization
* 🌍 Time zone-aware scheduling
* 🧪 A/B testing framework for message effectiveness
* 📬 Unified message inbox + push sync

---

## ⚠️ License

**Internal Use Only**
Not intended for public deployment or external integration.
