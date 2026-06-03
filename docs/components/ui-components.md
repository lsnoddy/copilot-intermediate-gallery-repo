# UI Components

This guide covers the components exported from `src/components/ui/index.ts`.

## Import pattern

```tsx
import {
  FeatureCard,
  Hero,
  SectionContainer,
  SectionTitle,
  StatsGrid,
} from "@/components/ui";
```

## Hero

Primary page introduction used on the home, gallery, upload, and admin pages.

**Props**

- `title: string`
- `description: string`

```tsx
<Hero
  title="Professional Photo Gallery & Portfolio"
  description="Upload, organize, and share your photography."
/>
```

## SectionContainer

Shared section wrapper that applies vertical spacing and an inner centered container.

**Props**

- `children: ReactNode`
- `className?: string`
- `bgColor?: string`

```tsx
<SectionContainer bgColor="bg-white/30 dark:bg-slate-800/30">
  <SectionTitle title="Quick Upload" />
</SectionContainer>
```

## SectionTitle

Section heading with optional supporting content and a "View All" link.

**Props**

- `title: string`
- `viewAllLink?: string`
- `className?: string`
- `children?: ReactNode`

```tsx
<SectionTitle title="Recent Uploads" viewAllLink="/gallery" />
```

## FeatureCard

Feature summary card used for marketing, quick actions, and upload capabilities.

**Props**

- `icon: LucideIcon`
- `title: string`
- `description: string`
- `iconColor: string`

```tsx
import { Upload } from "lucide-react";

<FeatureCard
  icon={Upload}
  title="Smart Upload"
  description="Drag and drop photos with guided processing."
  iconColor="text-blue-600"
/>
```

## StatsGrid

Responsive metric grid used by the admin dashboard.

**Props**

- `stats: Array<{ label; value; icon; color }>`
- `color` must be one of `blue`, `green`, `purple`, or `orange`

```tsx
import { Eye } from "lucide-react";

<StatsGrid
  stats={[
    { label: "Views", value: 1205, icon: Eye, color: "blue" },
  ]}
/>
```

## Usage notes

- Keep `Hero` content concise to preserve the existing centered layout.
- Use `SectionContainer` to maintain consistent spacing between page sections.
- Reuse `SectionTitle` instead of ad hoc headings for list and dashboard sections.
- Keep `FeatureCard` icon colors aligned with the existing utility class naming.
- Pass already formatted values to `StatsGrid` when display text should include separators or suffixes.
