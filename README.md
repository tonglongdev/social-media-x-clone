# Social Media X Clone

A full-stack social media platform inspired by Twitter/X, built with modern web technologies. Features real-time updates, user authentication, and a responsive design.

## Features

- **User Authentication**: Secure authentication with Clerk
- **Create & Share Posts**: Write and publish posts with the community
- **Comments & Interactions**: Engage with posts through comments, likes, and shares
- **User Profiles**: View user profiles with follower information
- **Follow System**: Follow/unfollow other users
- **Real-time Updates**: WebSocket support for live updates
- **Image & Video Support**: Upload and display media in posts
- **Search Functionality**: Discover posts and users
- **Trending Tags**: See popular hashtags
- **Responsive Design**: Mobile-friendly interface
- **Infinite Feed**: Seamless scrolling with pagination

## Tech Stack

- **Frontend**: Next.js 15, React, TypeScript
- **Styling**: Tailwind CSS, PostCSS
- **Database**: PostgreSQL with Prisma ORM
- **Authentication**: Clerk
- **Real-time**: WebSocket
- **State Management**: React Query (TanStack Query)
- **Deployment**: Node.js server

## Getting Started

### Prerequisites

- Node.js 18+
- npm, yarn, pnpm, or bun
- PostgreSQL database
- Clerk account for authentication

### Installation

1. Clone the repository
2. Install dependencies:

```bash
npm install
# or
yarn install
# or
pnpm install
# or
bun install
```

3. Set up environment variables:

```bash
# Create a .env.local file with:
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_key
CLERK_SECRET_KEY=your_key
DATABASE_URL=your_database_url
```

4. Set up the database:

```bash
npx prisma migrate dev
npx prisma db seed
```

### Running the Development Server

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser.

## Project Structure

```
src/
├── app/              # Next.js app directory
│   ├── api/          # API routes
│   ├── (board)/      # Main feed layout
│   └── sign-in/      # Authentication pages
├── components/       # Reusable React components
├── providers/        # Context providers (QueryProvider)
└── utils/            # Utility functions

prisma/
├── schema.prisma     # Database schema
└── migrations/       # Database migrations
```

## Key Components

- **Feed**: Main feed displaying posts
- **Post**: Individual post component
- **Comments**: Post comments section
- **FollowButton**: User follow/unfollow functionality
- **LeftBar**: Navigation sidebar
- **RightBar**: Recommendations and trending tags
- **Search**: Search functionality

## Building for Production

```bash
npm run build
npm start
```

## License

This project is open source and available for educational purposes.