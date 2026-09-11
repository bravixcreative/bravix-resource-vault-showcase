# Bravix Resource Vault

A modern resource discovery and management platform built by **Bravix Creative**.

Bravix Resource Vault was designed to provide a clean, scalable experience for discovering, organizing and managing curated digital resources through a modern frontend and structured admin workflow.

> This repository is a public showcase of the project architecture, features and selected implementation patterns. The production source code remains private.

---

## Highlights

- Modern resource discovery experience
- Search and filtering
- Structured categories
- Resource detail views
- Authentication
- Admin dashboard
- Resource management
- Secure CRUD workflows
- Responsive interface
- SEO-ready architecture
- Scalable database structure

---

## Tech Stack

`Next.js` `React` `TypeScript` `Tailwind CSS`

`Supabase` `PostgreSQL` `Authentication` `Storage`

`Vercel` `SEO` `Responsive UI`

---

## Product Architecture

The application is separated into three primary layers:

### Public Experience

Focused on resource discovery, navigation and content consumption.

### Application Layer

Handles routing, filtering, server-side data access and reusable interface components.

### Admin Experience

Provides authenticated management workflows for maintaining resources and structured content.

For a more detailed overview:

[View Architecture →](./docs/architecture.md)

---

## Core Features

### Resource Discovery

Users can browse and discover curated resources through structured categories and an optimized browsing experience.

### Search & Filtering

Resources can be quickly narrowed down using search and filtering patterns designed for larger datasets.

### Resource Detail Pages

Individual resources have structured detail views containing the information required for evaluation and discovery.

### Admin Dashboard

Authenticated administrators can manage platform content without modifying application code.

### Structured Content

Resources are modeled consistently to support maintainability and future expansion.

[Explore Features →](./docs/features.md)

---

## Selected Implementation Patterns

This showcase includes simplified examples demonstrating parts of the architecture without exposing production code or credentials.

### Supabase Data Access

```ts
const {data, error} = await supabase
  .from('resources')
  .select('id, title, slug, category')
  .eq('published', true)
  .order('created_at', {ascending: false});
```

### Metadata

```ts
export function createResourceMetadata(resource: Resource) {
  return {
    title: resource.title,
    description: resource.description,
    alternates: {
      canonical: `/resources/${resource.slug}`
    }
  };
}
```

---

## Screenshots

Product screenshots and UI previews can be found in the [`screenshots`](./screenshots) directory.

---

## Security & Source Code

The production repository is private.

This showcase intentionally excludes:

- Environment variables
- API keys
- Authentication secrets
- Production database configuration
- Internal administration logic
- Private infrastructure details

The examples included here are simplified implementation patterns intended for portfolio and technical demonstration purposes.

---

## About Bravix Creative

We design and develop modern digital products for brands and growing businesses.

**Web Development · E-commerce · UI/UX · SEO & Performance**

[Visit Bravix Creative →](https://bravixcreative.com)

---

Built by **Bravix Creative**.