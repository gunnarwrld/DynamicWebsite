# PostHub 🚀

A modern, dynamic web application built with vanilla JavaScript that showcases posts, user profiles, and comments using the DummyJSON API. This project demonstrates clean code architecture, responsive design, and interactive user experiences without relying on frameworks.

![PostHub Demo](https://img.shields.io/badge/Status-Active-success) ![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-yellow) ![HTML5](https://img.shields.io/badge/HTML5-Semantic-orange) ![CSS3](https://img.shields.io/badge/CSS3-Responsive-blue)

## 📋 Table of Contents

- [Features](#features)
- [Demo](#demo)
- [Technologies](#technologies)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [API Reference](#api-reference)
- [Key Learnings](#key-learnings)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)

## ✨ Features

### Core Functionality
- **Dynamic Post Loading**: Fetches and displays posts from DummyJSON API with pagination
- **User Profiles**: View detailed user information including contact details, physical stats, and blood type
- **Interactive Comments**: Read and explore comments for each post
- **Smart Caching**: User data is cached to minimize API calls and improve performance
- **Lazy Loading**: Posts only load when needed, optimizing initial page load time

### User Experience
- **Single Page Application (SPA)**: Seamless navigation without page reloads using hash-based routing
- **Modal System**: Clean, animated modal overlays for viewing user profiles
- **Loading States**: Smooth loading animations with CSS keyframes
- **Error Handling**: Comprehensive error messages for network failures and empty states
- **Responsive Design**: Mobile-first approach with media queries for all screen sizes
- **Active Navigation**: Visual feedback showing the current page

### Contact Form
- **HTML5 Validation**: Native browser validation for name, email, and required fields
- **Pattern Matching**: Custom validation patterns for name input
- **Success Messages**: User-friendly confirmation after form submission

## 🎯 Demo

### Screenshots

**Home Page**
- Welcome message with app instructions
- Clean, semantic HTML structure
- Expandable "How to use" section

**Posts Page**
- Grid of post cards with tags, reactions, and views
- "Load More" button for pagination
- Clickable post titles and author names

**Post Detail View**
- Full post content with complete metadata
- Comments section with user feedback
- Back navigation to posts list

**User Profile Modal**
- Profile image and user details
- Comprehensive information display
- Smooth animations and backdrop

## 🛠 Technologies

- **HTML5**: Semantic markup with `<article>`, `<details>`, `<summary>` elements
- **CSS3**: Flexbox layouts, animations, transitions, media queries
- **JavaScript (ES6+)**: Async/await, Fetch API, DOM manipulation, event handling
- **DummyJSON API**: RESTful API for posts, users, and comments data

## 📦 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/gunnarwrld/DynamicWebsite.git
   cd DynamicWebsite
   ```

2. **Open in your browser**
   
   Simply open `index.html` in your preferred web browser:
   ```bash
   # Using Python's built-in server (recommended)
   python -m http.server 8000
   
   # Or using Node.js http-server
   npx http-server
   
   # Or just open the file directly
   open index.html  # macOS
   start index.html # Windows
   ```

3. **Access the app**
   
   Navigate to `http://localhost:8000` (if using a server) or the file path in your browser.

## 🚀 Usage

### Navigation
- Click **Home** to view the welcome message and instructions
- Click **Posts** to browse all available posts
- Click **Contact** to access the contact form

### Interacting with Posts
1. Click on any **post title** to view full details and comments
2. Click on any **author name** to open their profile in a modal
3. Click **Load More** to fetch additional posts (10 at a time)

### Viewing Profiles
- User profiles display in a modal overlay
- Close the modal by:
  - Clicking the **X** button
  - Clicking **outside the modal**
  - Pressing the **ESC** key

### Contact Form
1. Fill in your name (letters only, minimum 2 characters)
2. Enter a valid email address
3. Write your message (optional)
4. Check the confirmation checkbox
5. Click **Send Message**

## 📁 Project Structure

```
DynamicWebsite/
│
├── index.html          # Main HTML structure with semantic markup
├── style.css           # Complete styling including animations and responsive design
├── app.js              # All JavaScript logic (600+ lines)
└── README.md           # Project documentation
```

### Key Files Explained

**index.html**
- Semantic HTML5 structure
- Multiple view sections (Home, Posts, Post Detail, Profile, Contact)
- Modal overlay for user profiles
- Form with HTML5 validation attributes

**style.css**
- Organized sections for each component
- CSS animations (@keyframes for fadeIn, slideIn, spin)
- Responsive design with mobile-first approach
- Error and empty state styling

**app.js**
- Global state management (`appData` object)
- Modular functions for data fetching, caching, and display
- Event handlers for navigation, modal, and form
- Comprehensive error handling with try-catch blocks

## 🔌 API Reference

This project uses the [DummyJSON API](https://dummyjson.com):

| Endpoint | Purpose | Parameters |
|----------|---------|------------|
| `/posts?limit={n}&skip={n}` | Fetch posts with pagination | `limit`, `skip` |
| `/posts/{id}` | Get single post by ID | `id` |
| `/users/{id}` | Get user details by ID | `id` |
| `/comments/post/{id}` | Get comments for a post | `id` |
| `/posts/user/{id}` | Get all posts by a user | `id` |

### Data Caching Strategy
- **Users**: Cached in `appData.users` object for O(1) lookup
- **Posts**: Stored in `appData.posts` array
- **Pagination**: Tracked with `currentSkip` and `totalPosts`

## 📚 Key Learnings

### Development Journey

1. **Semantic HTML Structure**
   - Learned to use `<article>`, `<details>`, `<summary>` for better accessibility
   - Implemented proper heading hierarchy

2. **API Integration**
   - Async/await patterns for cleaner asynchronous code
   - Error handling with try-catch and response.ok validation
   - Data caching to reduce unnecessary API calls

3. **State Management**
   - Global `appData` object for centralized state
   - Efficient data structures (object for users, array for posts)

4. **UI/UX Improvements**
   - Loading states with CSS animations
   - Error and empty state messages
   - Modal system with multiple close methods
   - Active navigation highlighting

5. **Code Simplification**
   - Replaced complex custom validation with HTML5 native validation
   - Simplified navigation logic using `classList.toggle`
   - Removed unnecessary features (auto-scroll, CTA button)

6. **Performance Optimization**
   - Lazy loading posts only when needed
   - User data caching
   - Efficient DOM manipulation

## 🔮 Future Enhancements

- [ ] Add search functionality for posts and users
- [ ] Implement local storage for offline viewing
- [ ] Add dark mode toggle
- [ ] Create user authentication simulation
- [ ] Add post filtering by tags
- [ ] Implement infinite scroll option
- [ ] Add animations for page transitions
- [ ] Create a "favorites" feature
- [ ] Add share functionality for posts
- [ ] Implement accessibility improvements (ARIA labels)

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## 👨‍💻 Author

**Gunnar**
- GitHub: [@gunnarwrld](https://github.com/gunnarwrld)

## 🙏 Acknowledgments

- [DummyJSON](https://dummyjson.com) for providing the free API
- Högskolan Kristianstad - Frontend Development course
- The JavaScript community for inspiration and best practices

---

**Built with ❤️ using Vanilla JavaScript**

*No frameworks were harmed in the making of this project* 😄
