# Ravebrite

![Ravebrite screenshot](https://user-images.githubusercontent.com/63977819/125955348-0469447a-2bbe-4a55-a5ae-4a975039712b.png)

Ravebrite is an Eventbrite clone focused on EDM events. Users can browse events, filter by genre, sign up, purchase tickets, bookmark events, and create and manage their own events.

## Technologies

* React / Redux
* Ruby on Rails 6.1
* PostgreSQL
* Webpack
* Active Storage (local disk in development)

## Prerequisites

* **Ruby** 3.2.10 (see `.ruby-version`)
* **Node.js** 18+ and npm
* **PostgreSQL** 15+

Recommended: [rbenv](https://github.com/rbenv/rbenv) for Ruby version management.

## Local setup

### 1. Install Ruby

```bash
rbenv install 3.2.10
cd Ravebrite-main
rbenv local 3.2.10
```

### 2. Install dependencies

```bash
bundle install
npm install
npm run build
```

### 3. Start PostgreSQL

```bash
# macOS with Homebrew
brew services start postgresql@15
```

### 4. Set up the database

```bash
bundle exec rails db:create db:schema:load db:seed
```

### 5. Start the server

```bash
bundle exec rails server
```

Open **http://localhost:3000** in your browser.

## Demo account

After seeding, you can log in with:

| Email | Password |
|-------|----------|
| `demo@user.com` | `demouser` |

Other seeded users (e.g. `raph@ex.com`) use password `123456`.

## Development

Rebuild the frontend after changing React code:

```bash
npm run webpack
```

Or for a one-off production build:

```bash
npm run build
```

Event images are stored on local disk in development (`storage/`). No AWS credentials are required to run locally.

## Features

* Browse all events with genre filtering
* Sign up and log in
* View event detail pages
* Purchase tickets (1–4 per order) and view owned tickets
* Bookmark events ("Likes")
* Create, edit, and delete hosted events
* Upload event photos via Active Storage

![Features overview](https://user-images.githubusercontent.com/63977819/125955647-761b9b0d-0236-4e5c-96d6-cede7362b957.png)
# ravebrite-restored
