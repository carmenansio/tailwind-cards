# **Tailwind CSS Pricing Cards Example**

This project demonstrates how to build a responsive pricing card section using **Tailwind CSS**.

## **Getting Started**

Follow these steps to set up the project and build the example step by step.

---

### **1. Initialize the Project**

1. Create a new folder and initialize the project:
   ```bash
   mkdir tailwind-pricing-cards
   cd tailwind-pricing-cards
   npm init -y
   ```

2. Install the required dependencies:
   ```bash
   npm install tailwindcss postcss autoprefixer
   npx tailwindcss init
   ```

3. Generate a basic Tailwind CSS configuration in `tailwind.config.js`.

---

### **2. Create the HTML and CSS Structure**

1. Create the project folders:
   ```bash
   mkdir css dist
   touch index.html css/styles.css
   ```

2. Add the following to your `css/styles.css` file:
   ```css
   @tailwind base;
   @tailwind components;
   @tailwind utilities;
   ```

3. Compile the Tailwind CSS file:
   ```bash
   npx tailwindcss -i ./css/styles.css -o ./dist/styles.css --watch
   ```

---

### **3. Build the HTML Layout**

Start by creating the basic structure of the HTML file:

#### **`index.html`**
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tailwind CSS Pricing Cards</title>
    <link rel="stylesheet" href="dist/styles.css">
</head>

<body class="bg-gray-900 text-gray-100">
    <!-- Hero Section -->
    <section class="bg-gradient-to-r from-purple-900 to-indigo-900 py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-4xl font-extrabold sm:text-5xl">Tailwind Pricing Cards</h2>
                <p class="mt-4 text-xl text-purple-200">Beautiful and responsive cards using Tailwind CSS</p>
            </div>
        </div>
    </section>

    <!-- Pricing Cards Section -->
    <section>
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 gap-8 sm:grid-cols-2 lg:grid-cols-3">
                <!-- Individual cards will go here -->
            </div>
        </div>
    </section>
</body>

</html>
```

---

### **4. Add Individual Cards**

1. Start by adding the first pricing card inside the `.grid` container:

```html
<!-- Basic Plan -->
<div class="bg-white bg-opacity-10 rounded-lg shadow-lg p-6 relative overflow-hidden">
    <div class="absolute top-0 right-0 m-4">
        <span class="inline-flex items-center px-3 py-1 rounded-full text-sm font-medium bg-purple-100 text-purple-800">
            Basic
        </span>
    </div>
    <div class="mb-8">
        <h3 class="text-2xl font-semibold text-white">Starter Pack</h3>
        <p class="mt-4 text-purple-200">Perfect for individuals and small teams.</p>
    </div>
    <div class="mb-8">
        <span class="text-5xl font-extrabold text-white">$49</span>
        <span class="text-xl font-medium text-purple-200">/mo</span>
    </div>
    <ul class="mb-8 space-y-4 text-purple-200">
        <li class="flex items-center">
            <svg class="h-6 w-6 text-green-400 mr-2" xmlns="http://www.w3.org/2000/svg" fill="none"
                viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M5 13l4 4L19 7" />
            </svg>
            <span>10 user accounts</span>
        </li>
        <li class="flex items-center">
            <svg class="h-6 w-6 text-green-400 mr-2" xmlns="http://www.w3.org/2000/svg" fill="none"
                viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M5 13l4 4L19 7" />
            </svg>
            <span>100 transactions per month</span>
        </li>
        <li class="flex items-center">
            <svg class="h-6 w-6 text-green-400 mr-2" xmlns="http://www.w3.org/2000/svg" fill="none"
                viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M5 13l4 4L19 7" />
            </svg>
            <span>Basic reporting</span>
        </li>
    </ul>
    <a href="#"
        class="block w-full py-3 px-6 text-center rounded-md text-white font-medium bg-gradient-to-r from-purple-600 to-indigo-600 hover:from-purple-700 hover:to-indigo-700">
        Get Started
    </a>
</div>
```

2. Add additional cards for the **Pro Plan** and **Enterprise Plan** by copying and customizing the first card. Replace content like the title, price, and features.

---

### **5. Customize with Tailwind Configuration (Optional)**

If you want to personalize colors, fonts, or breakpoints, edit the `tailwind.config.js` file:

```javascript
module.exports = {
  content: ["./*.html"],
  theme: {
    extend: {
      colors: {
        purple: {
          900: "#4c1d95",
        },
      },
    },
  },
  plugins: [],
};
```

---

### **6. Deploy the Project**

Deploy your project using GitHub Pages, Vercel, or Netlify:

1. Initialize a git repository:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   ```

2. Push the repository to GitHub:
   ```bash
   git remote add origin <repository-url>
   git push -u origin main
   ```

3. Deploy using your preferred platform.

---

### **Final Output**

Your page will display a fully responsive pricing card section with gradient backgrounds and hover effects.
