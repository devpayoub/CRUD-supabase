# 🗄️ CRUD Test with Supabase

A simple CRUD (Create, Read, Update, Delete) application built with Next.js 15, TypeScript, Tailwind CSS, and Supabase. This project demonstrates basic database operations with a clean, modern interface.

## ✨ Features

- **Create Records** - Add new users to the database
- **Read Records** - Display all users in a responsive table
- **Update Records** - Edit existing user information
- **Delete Records** - Remove users with confirmation
- **Real-time Updates** - Automatic table refresh after operations
- **Responsive Design** - Works on all devices
- **Dark Mode Support** - Built-in dark/light theme
- **Error Handling** - Comprehensive error messages
- **TypeScript** - Full type safety throughout the application

## 🚀 Tech Stack

- **Frontend**: Next.js 15, React 19, TypeScript
- **Styling**: Tailwind CSS 4
- **Database**: Supabase PostgreSQL
- **Deployment**: Vercel-ready

## 📋 Prerequisites

Before running this project, make sure you have:

- Node.js 18+ installed
- A Supabase account and project
- Git installed

## 🛠️ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/devpayoub/CRUD-supabase.git
   cd crud-supabase-test
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   
   Create a `.env.local` file in the root directory:
   ```env
   NEXT_PUBLIC_SUPABASE_URL=your_supabase_project_url
   NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

   To get these values:
   - Go to your Supabase project dashboard
   - Navigate to Settings → API
   - Copy the "Project URL" and "anon public" key

4. **Set up the database**

   In your Supabase dashboard, create a `Users` table with the following SQL:
   ```sql
   CREATE TABLE Users (
     id UUID DEFAULT gen_random_uuid() PRIMARY KEY,
     email TEXT UNIQUE NOT NULL,
     username TEXT UNIQUE NOT NULL,
     created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
   );
   ```

5. **Run the development server**
   ```bash
   npm run dev
   ```

6. **Open your browser**
   
   Navigate to [http://localhost:3000](http://localhost:3000)

## 📁 Project Structure

```
src/
├── app/                    # Next.js App Router
│   ├── layout.tsx         # Root layout
│   ├── page.tsx           # CRUD interface
│   └── globals.css        # Global styles
└── lib/
    └── supabase.ts        # Supabase client configuration
```

## 🔄 CRUD Operations

### Create
- Fill out the form with email and username
- Click "Create User" to add a new record
- The table automatically refreshes to show the new user

### Read
- All users are displayed in a responsive table
- Shows email, username, and creation date
- Table updates automatically after any operation

### Update
- Click "Edit" on any user row
- Form populates with current data
- Modify fields and click "Update User"
- Click "Cancel" to discard changes

### Delete
- Click "Delete" on any user row
- Confirmation dialog appears
- Confirm to permanently remove the user

## 🎨 UI Components

- **Modern Design**: Clean, responsive interface
- **Loading States**: Spinner animations during operations
- **Error Handling**: Clear error messages for validation
- **Dark Mode**: Automatic theme switching
- **Responsive**: Works on mobile, tablet, and desktop

## 🔧 Customization

### Styling
The project uses Tailwind CSS. You can customize the design by modifying:
- `src/app/globals.css` - Global styles
- Component classes in `src/app/page.tsx`

### Database Schema
Update the database schema in Supabase and modify the CRUD operations in `src/app/page.tsx` to match your new schema.

## 🚀 Deployment

### Vercel (Recommended)
1. Push your code to GitHub
2. Connect your repository to Vercel
3. Add environment variables in Vercel dashboard
4. Deploy!

### Other Platforms
The project can be deployed to any platform that supports Next.js:
- Netlify
- Railway
- DigitalOcean App Platform
- AWS Amplify

## 🔒 Security Features

- **Input Validation**: Email format and required field checking
- **Error Handling**: Comprehensive error messages without exposing sensitive data
- **Confirmation Dialogs**: Prevent accidental deletions
- **Type Safety**: TypeScript ensures data integrity

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) - The React framework
- [Supabase](https://supabase.com/) - The open source Firebase alternative
- [Tailwind CSS](https://tailwindcss.com/) - A utility-first CSS framework
- [Vercel](https://vercel.com/) - The platform for frontend developers

## 📞 Support

If you have any questions or need help with this project:

1. Check the [Issues](https://github.com/devpayoub/CRUD-supabase/issues) page
2. Create a new issue with a detailed description
3. Include your environment details and error messages

---

**Made with ❤️ using Next.js and Supabase**
