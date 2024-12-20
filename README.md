# E-commerce Website
[![My Skills](https://skillicons.dev/icons?i=nuxt,tailwind,vue,pinia,typescript)](https://skillicons.dev)
## [🔗 Live Demo](https://nuxt-ecommerce-iota.vercel.app/) 
This is an e-commerce web application built using modern web technologies, focusing on creating a clean, responsive, and user-friendly interface. The project is entirely frontend-based and relies on a fake API for product and user data.

## Features

- **Home Page (`/`)**:
  - Displays top products from the fake API.
  <br />
  <img src="/public/preview/home-page.png"/>
  <hr />
  <img src="/public/preview/home-page-2.png"/>
- **Products Page (`/products`)**:

  - Displays all available products.
  - Includes a category filter to refine product searches.
  - <img src="/public/preview/products-page.png"/>
- **Product Details Page (`/products/:id`)**:

  - Displays detailed information about a specific product, including title, price, and other details.
   <img src="/public/preview/product-details.png"/>
- **Cart Page (`/cart`)**:

  - Displays products added to the cart.
  - Allows users to adjust product quantities.
  - Provides a summary for checkout.
  <img src="/public/preview/cart-page.png"/>
- **Authentication Page (`/auth`)**:

  - Enables user login using a fake API for testing purposes.
  <img src="/public/preview/login.png"/>
- **Profile Page (`/profile`)**:

  - Displays user information.

- **Checkout Page (`/checkout`)**:

  - Allows users to place orders for items in the cart.
  <img src="/public/preview/checkout-page.png"/>
- **Orders Page (`/orders`)**:

  - Displays a list of placed orders.
  <img src="/public/preview/orders-page.png"/>
- **Color Mode Switcher**:
  - Allows users to toggle between light and dark themes.

## Technologies Used
[![My Skills](https://skillicons.dev/icons?i=nuxt,vue,typescript,tailwind,pinia,vuetify,html,css,js&perline=5)](https://skillicons.dev)
- **Framework**: Nuxt 3
- **UI Framework**: TailwindCSS
- **Component Library**: Nuxt UI
- **JavaScript Framework**: Vue 3 Composition API
- **State Management**: Pinia
- **TypeScript**: Added types for all API results to enhance code quality.
- **API**:
  - Fake Store API for products data.
  - Fake authentication API for user login.

## Project Structure

The project is structured to ensure maintainability and scalability. Key architectural features include:

- **Factories Components**:

  - Reusable and dynamic components to reduce redundancy.

- **Composables**:

  - Encapsulated logic for reuse across components.

- **Middleware**:
  - Handles route guards for authentication and other functionalities.

## Setup and Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd <project-directory>
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Start the development server:
   ```bash
   npm run dev
   ```

## Usage

- Open the application in your browser at `http://localhost:3000`.
- Navigate through the various pages to explore the features.

## API Information

- **Products API**: [Fake Store API](https://fakestoreapi.com/)
- **Authentication API**: Mocked API for testing purposes.

## Notes

- This project is frontend-only and does not include a backend.
- The data is fetched dynamically from external APIs.

## Future Improvements

- Implement a backend for real data storage and processing.
- Add payment gateway integration for real transactions.
- Enhance the filtering functionality with more options.

## License

This project is open-source and available under the MIT License.

---

Feel free to contribute or reach out with feedback!
