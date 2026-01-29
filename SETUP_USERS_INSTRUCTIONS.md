# Supabase User Setup Instructions

## Users to Create

You need to create these 4 users in your Supabase project:

1. **admin@leados.com** - Password: `Admin!123`
2. **cloy.caballo@leados.com** - Password: `Admin!123`
3. **chill.aledo@leados.com** - Password: `Prolevel#2026`
4. **reyma.pesigan@leados.com** - Password: `Prolevel#2026`

## Option 1: Using Supabase Dashboard (Recommended)

1. Go to your Supabase project dashboard: https://supabase.com/dashboard/project/gesxrlyplcotlubhuvri
2. Navigate to **Authentication** → **Users**
3. Click **Add User** button
4. For each user:
   - Enter the email address
   - Enter the password
   - Click **Create User**
5. Repeat for all 4 users

## Option 2: Using the Sign-Up Page (Alternative)

If you want to allow users to sign up themselves:

1. Open your LeadershipOS HTML file in a browser
2. You'll need to temporarily add a sign-up option to the login screen
3. Each user can create their own account with their email and password

## Option 3: Using SQL (Admin API)

You can also use the Supabase SQL editor to create users, but this requires the service role key and is more complex.

## Verification

After creating the users, you can verify they exist by:
1. Going to Authentication → Users in your Supabase dashboard
2. You should see all 4 email addresses listed

## Next Steps

Once the users are created:
1. Open the LeadershipOS HTML file
2. Try logging in with one of the email/password combinations
3. Test the Cloud Sync feature by:
   - Clicking "Push to Cloud" to upload your data
   - Clicking "Pull from Cloud" to download it back

## Important Notes

- Passwords are securely hashed in Supabase (not stored in plain text)
- Each user's data is isolated via Row-Level Security (RLS)
- Users can only access their own cloud backups
- The old Google Sheets authentication has been completely replaced
