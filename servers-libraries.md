---
title: Servers & Libraries
---

<!-- =========================================================
VODUM Docs - Servers & Libraries
Dark themed markdown with subtle badges & callouts
========================================================= -->

<div align="left">

# 🖥️ Servers & Libraries

<span style="display:inline-block;padding:6px 10px;border-radius:999px;background:#0b1220;border:1px solid #1f2a44;color:#9fb2d8;font-size:12px;">
Plex • Jellyfin • Libraries • Access
</span>

<br><br>

The **Servers & Libraries** section is where you configure and monitor all
**Plex** and **Jellyfin** servers connected to VODUM, as well as their
associated **libraries** and user access.

This section is divided into two main tabs:
- **Servers**
- **Libraries**

<hr style="border:0;border-top:1px solid #1f2a44;margin:18px 0;" />

</div>

## 🗂️ Servers tab

The **Servers** tab allows you to:
- add new Plex or Jellyfin servers
- monitor server availability
- edit server configuration
- inspect libraries and user access per server

---

## ➕ Add server

On the left side of the page, you can add a new server.

### Fields explained

#### Server type
Select the server type:
- **Plex**
- **Jellyfin**

This choice determines:
- which API is used
- how libraries and users are synchronized

---

#### URL
The base URL of your server, for example:
http://192.168.1.10:32400


This URL is used by VODUM to communicate with the server API.

---

#### Token
The API token used to authenticate VODUM.

- For **Plex**, this is a Plex token
- For **Jellyfin**, this is an API key

> ⚠️ Tokens are sensitive information.  
> Make sure they remain private.

---

#### Add server
Click **Add server** to register the server in VODUM.

Once added:
- the server is checked automatically
- libraries are fetched
- the server appears in the server list

<hr style="border:0;border-top:1px solid #1f2a44;margin:18px 0;" />

## 🧱 Server cards (overview)

On the right side, each server is displayed as a card.

Each card shows:
- **Server name**
- **Server type** (Plex / Jellyfin badge)
- **URL**
- **Online / Offline status**
- **Number of libraries**
- **Number of users with access**

> ✅ **Online** means the server responds correctly to API checks.  
> ❌ **Offline** means the server could not be reached during the last check.

Clicking on a server card opens the **Server details** page.

<hr style="border:0;border-top:1px solid #1f2a44;margin:18px 0;" />

## 🧩 Server details page

The server details page provides a complete view of a single server.

---

### ℹ️ Server information

This panel displays editable server configuration fields:

- **Name**: internal display name in VODUM
- **Server type**: Plex or Jellyfin
- **Status**: current connectivity status
- **URL**: API endpoint
- **Local URL**: optional local/internal address
- **Public URL**: optional public address
- **Token**: API token used by VODUM

### Actions
- **Save**: apply configuration changes
- **Delete**: remove the server from VODUM

> ⚠️ Deleting a server removes:
> - the server configuration
> - associated libraries
> - access mappings  
> It does **not** delete users on Plex or Jellyfin directly.

<hr style="border:0;border-top:1px solid #1f2a44;margin:18px 0;" />

## 📚 Libraries (per server)

Below the server information, the **Libraries** table lists all libraries
detected on the selected server.

### Columns explained

- **Name**: library name as defined on the server
- **Type**: Movies / Shows / TV Shows
- **section_id / ID**: internal server identifier
- **Users**: number of users currently having access to this library

This view helps you:
- verify library synchronization
- understand access distribution
- detect inconsistencies between servers

---

## 👥 Users with access to this server

This section lists all users who currently have access to the selected server.

Each entry shows:
- username
- email address (if available)
- quick access to the user details page

> 💡 This list reflects the **current applied access**, not future or pending subscriptions.

<hr style="border:0;border-top:1px solid #1f2a44;margin:18px 0;" />

## 🗂️ Libraries tab (global view)

The **Libraries** tab provides a **global view** of all libraries across all servers.

This page is useful to:
- audit access at scale
- compare libraries across servers
- identify heavily shared libraries

---

### 📋 All libraries table

Each row represents one library on one server.

#### Columns explained

- **Server**: server hosting the library
- **Name**: library name
- **Type**: Movies / Shows
- **ID**: server-specific library identifier
- **Users**: number of users with access

Checkboxes allow future batch operations or selection-based actions.

> 💡 A library appearing multiple times means it exists on multiple servers.

<hr style="border:0;border-top:1px solid #1f2a44;margin:18px 0;" />

## 🔄 How access works (important)

<span style="display:inline-block;padding:10px 12px;border-radius:12px;background:#0b1220;border:1px solid #1f2a44;color:#9fb2d8;">
<b>Key concept</b><br>
Libraries are not assigned manually per user in this section.<br>
Access is driven by <b>subscriptions</b> and applied by automated tasks.
</span>

- Servers define **what can be shared**
- Libraries define **what exists**
- Subscriptions define **who should have access**
- Tasks apply access changes to Plex/Jellyfin

This separation ensures consistency and automation.

<hr style="border:0;border-top:1px solid #1f2a44;margin:18px 0;" />

## ✅ Typical workflow

1. Add a Plex or Jellyfin server
2. Verify server status (Online)
3. Check detected libraries
4. Create subscriptions that reference servers/libraries
5. Let automated tasks apply access

<hr style="border:0;border-top:1px solid #1f2a44;margin:18px 0;" />

## 🧯 Troubleshooting

### Server appears Offline
- verify URL and token
- check network connectivity
- inspect **Logs** for API errors

### Libraries missing
- ensure the server is reachable
- trigger a synchronization task
- check permissions of the API token

### User count incorrect
- verify subscriptions
- check if access update tasks ran
- inspect Logs for skipped updates

<hr style="border:0;border-top:1px solid #1f2a44;margin:18px 0;" />

## 📌 Notes

- This section defines the **infrastructure layer** of VODUM.
- Direct manual changes on servers may be overwritten by automated tasks.
- Always use VODUM as the source of truth for access management.

<br>

<div align="center">
<span style="display:inline-block;padding:6px 10px;border-radius:999px;background:#0b1220;border:1px solid #1f2a44;color:#9fb2d8;font-size:12px;">
VODUM • Servers & Libraries documentation
</span>
</div>

