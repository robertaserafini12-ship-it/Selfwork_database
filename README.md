# Selfwork Introduzione Database

Progettazione logica e concettuale dei database per i seguenti tre progetti.

---

## 1. E-Commerce (Libreria Online)

### Tabelle e Campi:
* **users**: `id` (PK), `full_name`, `email`, `password`, `birth_date`, `address`, `phone_number`
* **books**: `id` (PK), `title`, `author`, `publication_year`, `stock_quantity`
* **orders**: `id` (PK), `user_id` (FK), `order_date`, `is_paid`, `shipping_address`
* **order_items**: `id` (PK), `order_id` (FK), `book_id` (FK), `quantity`

### Relazioni:
* `users` (1) ─── (N) `orders`
* `orders` (1) ─── (N) `order_items`
* `books` (1) ─── (N) `order_items`

---

## 2. Social Network

### Tabelle e Campi:
* **users**: `id` (PK), `username`, `email`, `password`, `profile_picture_url`
* **posts**: `id` (PK), `user_id` (FK), `content`, `created_at`
* **likes**: `id` (PK), `user_id` (FK), `post_id` (FK), `created_at`

### Relazioni:
* `users` (1) ─── (N) `posts`
* `users` (1) ─── (N) `likes`
* `posts` (1) ─── (N) `likes`

---

## 3. Sito di Annunci

### Tabelle e Campi:
* **users**: `id` (PK), `full_name`, `email`, `password`, `birth_date`, `role`
* **categories**: `id` (PK), `name`
* **announcements**: `id` (PK), `title`, `description`, `category_id` (FK), `user_id` (FK), `created_at`, `is_accepted`

### Relazioni:
* `users` (1) ─── (N) `announcements`
* `categories` (1) ─── (N) `announcements`
