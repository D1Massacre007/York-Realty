# 🏠 York Realty

**Find Your Campus Home, Fast.**  
York Realty is a student-focused housing platform built to help York University students easily find and post **on-campus properties** — safely, affordably, and efficiently.

> ⚠ **Note:** This website is **still under development**, and exciting new features are on the way!

---

## 🚀 Live Like You Belong

Welcome to York Realty, the modern platform for students who are ready to settle in — or move on. Whether you're looking to **rent a space**, **post your property**, or just **explore verified listings**, we’ve got your back.

---

## 🧭 Website Overview

### 🔸 Home (`index.html`)
- Hero banner with call-to-action.
- Swiper carousel showcasing **why students choose York Realty**.
- Dynamic **Featured Listings** pulled from the backend.

### 🔸 Listings (`listings.html`)
- View all available properties.
- Powerful **real-time filters**:
  - 🔍 Search by title, address, postal code
  - 🛏 Beds & 🛁 Baths dropdowns
  - 🏘️ Housing type, 🏫 Campus proximity
- Secure “View Details” action (login required).

### 🔸 Create Listing (`create-listing.html`)
- **Authenticated users only** can:
  - Upload images
  - Input property details (address, price, beds, baths, etc.)
  - Post new listings via **backend API**
- Built-in validation with glowing error highlights.

### 🔸 Login/Register
- Modern form UI with gradient glow and validation.
- Registration includes:
  - Full name, email, password (with confirmation)
- Login securely checks credentials and handles sessions.
- Session persistence via `sessionStorage`.

### 🔸 FAQ (`faq.html`)
- Common student questions answered.
- Helps build trust, especially for first-time users or landlords.

---

## 🛠️ Built With

| Tech        | Description                                  |
|-------------|----------------------------------------------|
| 🟢 Node.js   | Backend runtime for serving HTTP requests    |
| ⚙️ Express   | Lightweight framework for API routes         |
| 🐬 MySQL     | Relational database for user & listing data |
| 🎨 Bootstrap | Responsive and modern UI styling             |
| 🖼️ Swiper.js | Carousel for homepage and testimonials       |
| 🧠 JavaScript | Vanilla JS for dynamic UI & form logic      |
| 🌐 REST API | JSON-based endpoints for real-time data       |

🎨 **Design Theme:**  
York Realty uses a **Red & White color palette**, proudly inspired by **York University’s official branding** — clean, confident, and student-first.

---

## 🌐 Backend Integration

### 📂 `app.js`
- Express server setup
- Middleware:
  - `express.json()`
  - `cors`
  - `multer` for file uploads (listing images)
- Routes:
  - `POST /register`
  - `POST /login`
  - `POST /listings` (with `multipart/form-data`)
  - `GET /listings` (all)
  - `GET /listings/:id` (detail)

### 🧩 `Database.js`
- MySQL connection pooling
- Environment variables for DB credentials
- Secure queries using prepared statements

---

## 🔄 Real-Time API Features

- 📥 **User registration/login**: Instant feedback and error handling.
- 🏡 **Listings fetch**: Live property data rendered directly to the UI.
- 🔍 **Filters**: Update results dynamically without page reload.
- 🖼️ **Image upload**: Real-time upload via `FormData` and `multer`.

---

## 🔐 Secure Features

- Session-based auth using `sessionStorage`
- Protected pages (e.g., `create-listing`, `view-details`)
- Client-side form validation
- Password mismatch and format checks
- Custom alerts with fade-in/out transitions

---

## 🎨 CSS Details

**Click here to view all elements of CSS used:**  

<details>
<summary>📂 Show All CSS Elements</summary>

### ✅ Global Styles & Variables
- Theme color variables using `:root`
- Smooth scrolling and clean typography
- Layout with `flex` and `min-height: 100vh`

---

### ✅ Navbar Styling
- Fixed navbar with **York Red background**
- Brand hover animation (`scale + rotate`)
- Navigation links with **animated underline** using `::after`

---

### ✅ Hero Section
- Full-screen **background image** with dark overlay
- Large **hero heading** with text-shadow
- Animated **call-to-action button** with hover scaling

---

### ✅ Cards (Listings)
- Rounded corners (`border-radius: 1rem`)
- **Hover effects:** `transform: scale(1.02) translateY(-12px)`
- Image **zoom on hover** (`object-fit: cover; transform: scale(1.1)`)

---

### ✅ Forms & Validation
- Input focus with **red glow** using `box-shadow`
- Validation glow with `.form-red-gradient-glow`
- Styled submit buttons with hover lift

---

### ✅ Filter Section
- Styled search bar and dropdowns with focus glow
- Search button hover animation

---

### ✅ Animations
- `.fade-in` and `.fade-in-up` for section reveals
- Keyframes: `@keyframes fadeIn`, `fadeInUp`, `pulseBadge`

---

### ✅ Modals
- Custom modal with **red header and scale-in animation**
- Buttons with hover transformations

---

### ✅ FAQ Section
- White strip with shadow and **bold red FAQ link hover effects**

---

### ✅ Swiper Carousel
- Customized navigation buttons with **gold hover effects**
- Circular buttons and pagination styling

---

### ✅ Footer
- Red background with **white links**
- Social icons with hover scaling

---

### ✅ Back-to-Top Button
- Circular button with **hover lift effect** and shadow

---

### ✅ Responsive Design
- Media queries for:
  - **Tablets** (`max-width: 992px`)
  - **Mobiles** (`max-width: 768px`)
- Adjusted typography, card size, hero section padding

---

### ✅ Transitions
- Smooth hover transitions (`transition: all 0.3s ease`)
- Bouncy animations using `cubic-bezier`

</details>

---

## 🛠 Future Reworks & Features (Under Development)

- 🌐 **Language Translation Button**  
  - Translate **English → French** for all pages dynamically.
- 🤖 **Machine Learning Recommendations**  
  - Implement **Cosine Similarity** to suggest **similar listings** based on user searches.
- 🗺 **Live Location Map**  
  - Display property locations on an **interactive map** for better navigation.
- 🔮 **Other Planned Enhancements**  
  - **Dark Mode toggle**
  - **Advanced filtering options** (Price range slider, property type tags)
  - **Enhanced image gallery with zoom-in modal**
  - **User profile dashboard** for managing listings

---

## ▶️ How to Run Locally

```bash
# Clone the repository
git clone https://github.com/yourusername/YorkRealty-App.git
cd YorkRealty-App

# Install dependencies
npm install

# Start development server
npm run dev

