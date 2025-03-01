# Faker Examples

A collection of useful examples demonstrating how to use the [Faker](https://fakerjs.dev/) library to generate realistic fake data for testing and development purposes.

## 📌 Features
- Generate random names, addresses, phone numbers, emails, and more.
- Useful for testing, database seeding, and prototyping.
- Various examples showcasing different use cases.

## 🔧 Installation

To use Faker in your JavaScript project, install it via npm:

```bash
npm install @faker-js/faker
```

or using yarn:

```bash
yarn add @faker-js/faker
```

## 🚀 Usage Examples

### 1. Basic Usage
```javascript
import { faker } from '@faker-js/faker';

console.log(faker.person.fullName()); // Random full name
console.log(faker.internet.email());  // Random email
console.log(faker.location.streetAddress()); // Random address
```

### 2. Generating Fake User Data
```javascript
const generateUser = () => {
  return {
    id: faker.string.uuid(),
    name: faker.person.fullName(),
    email: faker.internet.email(),
    phone: faker.phone.number(),
    address: faker.location.streetAddress(),
  };
};

console.log(generateUser());
```

### 3. Generating Multiple Fake Users
```javascript
const generateUsers = (count = 5) => {
  return Array.from({ length: count }, generateUser);
};

console.log(generateUsers(10)); // Generates an array of 10 fake users
```

### 4. Fake Product Data (E-Commerce Example)
```javascript
const generateProduct = () => {
  return {
    id: faker.string.uuid(),
    name: faker.commerce.productName(),
    price: faker.commerce.price(),
    description: faker.commerce.productDescription(),
    category: faker.commerce.department(),
  };
};

console.log(generateProduct());
```

### 5. Bulk Data Generation
```javascript
const generateBulkData = (count = 100) => {
  return Array.from({ length: count }, () => generateUser());
};

console.log(generateBulkData(100)); // Generates an array of 100 fake users
```


