# Music School

A modern, animated landing site for an online music school, built with Next.js. It showcases featured courses, instructors, testimonials, and upcoming webinars through a dark, motion-rich UI built on Aceternity-style components.

## Features

- **Hero section** with animated background effects (wavy background / spotlight)
- **Featured courses** sourced from a local JSON dataset, rendered as 3D / hover-effect cards
- **Why Choose Us** highlights section
- **Testimonials** via infinite moving cards
- **Upcoming webinars** listing
- **Instructors** showcase with animated tooltips
- Dedicated **Courses** and **Contact** pages
- Responsive navbar and footer

## Tech Stack

- [Next.js 16](https://nextjs.org) (App Router) + [React 19](https://react.dev)
- [TypeScript](https://www.typescriptlang.org/)
- [Tailwind CSS v4](https://tailwindcss.com/)
- [Framer Motion](https://www.framer.com/motion/) for animations
- [simplex-noise](https://github.com/jwagner/simplex-noise.js) for procedural background effects
- `clsx` + `tailwind-merge` (via `src/utils/cn.ts`) for class composition
- React Compiler (`babel-plugin-react-compiler`)

## Getting Started

Install dependencies and run the development server:

```bash
pnpm install
pnpm dev
# or: npm install && npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the site.

## Scripts

| Command      | Description                  |
| ------------ | --------------------------- |
| `pnpm dev`   | Start the development server |
| `pnpm build` | Build for production         |
| `pnpm start` | Run the production build     |
| `pnpm lint`  | Run ESLint                   |

## Project Structure

```
src/
├── app/                 # App Router pages
│   ├── page.tsx         # Home page (composes the sections below)
│   ├── layout.tsx       # Root layout + Navbar
│   ├── courses/         # Courses page
│   └── contact/         # Contact page
├── components/          # Page sections (HeroSection, FeaturedCourses, etc.)
│   └── ui/              # Reusable animated UI primitives
├── data/
│   └── music_courses.json   # Course catalog data
└── utils/
    └── cn.ts            # Tailwind class merge helper
```

Course content is defined in `src/data/music_courses.json`; edit that file to change the catalog.

## Deployment

The app deploys cleanly on [Vercel](https://vercel.com/new). See the [Next.js deployment docs](https://nextjs.org/docs/app/building-your-application/deploying) for other platforms.

## License

Released under the [MIT License](LICENSE).
