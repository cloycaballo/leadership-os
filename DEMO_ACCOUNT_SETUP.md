# 🎭 Demo Account Setup Guide

## Account Credentials

**Email**: `test@leados.com`  
**Password**: `Test!2026`

---

## Step 1: Create User in Supabase

1. Go to: https://supabase.com/dashboard/project/gesxrlyplcotlubhuvri/auth/users
2. Click **"Add User"**
3. Enter:
   - Email: `test@leados.com`
   - Password: `Test!2026`
4. Click **"Create User"**

---

## Step 2: Load Demo Data

### Option A: Via LeadershipOS (Easiest)

1. Open your LeadershipOS app
2. Log in with `test@leados.com` / `Test!2026`
3. Go to **Settings** → **Data** tab
4. Click **"Restore File"**
5. Select `demo_account_backup.json`
6. Data will be loaded into the app
7. Click **"Push to Cloud"** to sync to Supabase

### Option B: Direct Cloud Upload

1. Log in with test account
2. Open browser console (F12)
3. Paste this code:

```javascript
// Load demo data directly
fetch('demo_account_backup.json')
  .then(r => r.json())
  .then(data => {
    localStorage.setItem('leadership_os_data', JSON.stringify(data));
    location.reload();
  });
```

---

## Demo Data Overview

### 👥 Team Members (6)
- Alex Rivera - Senior Developer (TechStart Solutions)
- Maria Santos - Project Manager (CloudNine Inc)
- James Wilson - Business Analyst (DataFlow Systems)
- Sarah Johnson - UX Designer (TechStart Solutions)
- Michael Lee - DevOps Engineer (CloudNine Inc)
- Emily Davis - QA Specialist (DataFlow Systems)

### 🎯 Projects (3)
1. **Mobile App Redesign** - TechStart Solutions (45% complete)
2. **Cloud Migration** - CloudNine Inc (60% complete)
3. **Data Analytics Dashboard** - DataFlow Systems (15% complete)

### ✅ Tasks
- 5 active tasks in various stages
- 2 completed tasks for history
- Mix of priorities (high, medium, low)

### 📊 Other Features
- 3 logbook entries
- 3 calendar events
- Quick links configured
- Braindump notes
- Settings configured

---

## Key Features to Demonstrate

### 1. Authentication
✅ Secure Supabase login  
✅ Session management  
✅ Lock/unlock functionality

### 2. Team Management
✅ View team members  
✅ Filter by account  
✅ EWS status indicators  
✅ No personal information (privacy-safe)

### 3. Project Tracking
✅ Multiple active projects  
✅ Progress tracking  
✅ Team assignments  
✅ Priority levels

### 4. Task Management (My Desk)
✅ Task creation and updates  
✅ Priority sorting  
✅ Status tracking  
✅ Project association

### 5. Cloud Sync
✅ Push to Cloud  
✅ Pull from Cloud  
✅ Sync status indicator  
✅ Cross-device capability

---

## Important Notes

### ✅ Safe to Share
- No real personal information
- Fictitious names and data
- No phone numbers or addresses
- Generic email addresses
- Demo projects and clients

### 🎯 Perfect For
- Product demonstrations
- Feature showcases
- Client previews
- Testing and QA
- Training purposes

### 🔒 Security
- Separate Supabase user
- Isolated RLS protection
- Can't access other accounts' data
- Easy to delete/recreate

---

## Resetting Demo Account

If you need to reset the demo data:

1. Log in as test@leados.com
2. Go to Settings → Data
3. Click "Restore File"
4. Select `demo_account_backup.json` again
5. Click "Push to Cloud" to update

Or delete and recreate the user in Supabase.

---

## Share with Confidence

You can now safely share these credentials with:
- Potential clients
- Stakeholders
- Demo audiences
- Beta testers
- Training participants

All data is fictitious and privacy-safe!

---

**Created**: January 28, 2026  
**File Location**: `demo_account_backup.json`  
**Account**: test@leados.com
