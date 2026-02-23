

## Authentication App with Supabase

### 1. Supabase Setup
- Connect the project to Supabase (via Lovable Cloud)
- Create a **profiles** table with fields: `id` (linked to auth.users), `display_name`, `avatar_url`, `created_at`, `updated_at`
- Set up RLS policies so users can only read/update their own profile
- Add a database trigger to auto-create a profile when a user signs up

### 2. Register Page (`/register`)
- Email and password signup form with validation
- Password confirmation field
- Optional display name field (saved to profiles)
- Link to login page
- Success feedback after registration

### 3. Login Page (`/login`)
- Email and password login form
- Link to register page
- Error handling for invalid credentials

### 4. Auth Protection
- Protected route wrapper that redirects unauthenticated users to `/login`
- Redirect authenticated users away from login/register pages

### 5. Dashboard (`/` — post-login)
- Welcome message with user's display name
- Show user email and profile info
- Logout button
- Clean, simple layout

### Design
- Clean, modern auth forms centered on the page
- Consistent with the existing shadcn/ui design system
- Form validation with clear error messages
- Loading states on submit buttons

