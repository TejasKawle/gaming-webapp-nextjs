🎮 Gaming Website – Next.js (Catch-All Routes Demo)

This project is a Next.js gaming website built to demonstrate the power of dynamic and catch-all routing in real-world applications.
Users can browse games, view detailed pages, and explore content driven by dynamic URL structures such as:

/games/[slug]
/games/[...slug]

 Features
 Next.js Catch-All Routes

This project highlights how to use:

Dynamic Routes
/games/[slug]


Used for individual game pages like:

/games/elden-ring
/games/hades

Catch-All Routes
/games/categories/[...slug]


Used to demonstrate multi-level routing, enabling URLs such as:

/games/categories/action-rpg
/games/categories/action-rpg/open-world
/games/categories/action-rpg/open-world/soulslike


Catch-all routes allow the app to handle unlimited nested paths without manually creating each route.

🧱 Tech Stack

Next.js 14+ (App Router or Pages Router)

TypeScript

React

CSS / Tailwind (if used)

Steam CDN WebP images for real game covers

Static JSON-based game data

📁 Project Structure

Example structure (Pages Router version):

/pages
  /games
    [slug].tsx
    [...slug].tsx   // catch-all route
/components
/data
  games.ts         // Game objects and metadata

🧩 How Catch-All Routes Work

In Next.js, a catch-all route uses:

/pages/games/[...slug].tsx


Meaning:

It matches any URL like /games/a, /games/a/b, /games/a/b/c, etc.

All segments are passed as an array:

router.query.slug   // ["a", "b", "c"]


This project uses it for:

Category filtering

Multi-step navigation

Nested content exploration

🎮 Game Data Example

Each game uses a shared TypeScript interface:

export type Game = {
  id: string;
  slug: string;
  title: string;
  image: string;
  description: string;
  category: string;
  rating: number;
  platforms: string[];
  // more fields...
};


Images use real Steam CDN WebP links like:

image: "https://cdn.akamai.steamstatic.com/steam/apps/1145360/header.jpg?format=webp"

▶️ Getting Started
1. Install Dependencies
npm install

2. Run Development Server
npm run dev

3. Visit in Browser
http://localhost:3000

📚 What You Learn

This project teaches you:

✓ How to create dynamic routes
✓ How to use catch-all and optional catch-all routing
✓ How to structure data-driven navigation
✓ How to map URL segments to page content
✓ How to build scalable Next.js websites
📦 Production Build
npm run build
npm start

📝 License

This project is open-source and free to modify for learning purposes.
