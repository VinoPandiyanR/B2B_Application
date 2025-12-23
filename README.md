# A2B Hotel - B2B Catering Application

A comprehensive B2B Catering Management System built with Java Spring Boot, MySQL, and modern HTML/CSS/JS frontend.

![A2B Hotel Logo](https://via.placeholder.com/150x150/DAA520/1a1a2e?text=A2B)

## 🌟 Features

### Customer Management
- Add, edit, and delete customers
- Store contact details, company info, and GST numbers
- View customer order history

### Order/Booking Management
- Create catering bookings with complete event details
- Track order status (Pending, Confirmed, In Progress, Completed, Cancelled)
- Manage event details: date, time, venue, guests count
- Menu preferences and special requirements
- Decoration options with color schemes and themes

### Payment Processing
- Multiple payment methods (GPay, PhonePe, Paytm, UPI, Cash, Card, Bank Transfer)
- Payment tracking and receipts
- Payment status management

### Dashboard
- Overview of total customers, orders, and revenue
- Recent orders display
- Upcoming events calendar
- Quick action buttons

## 🛠️ Technology Stack

- **Backend:** Java 17, Spring Boot 3.2.0
- **Database:** MySQL 8.0
- **ORM:** Spring Data JPA / Hibernate
- **Security:** Spring Security
- **Frontend:** Thymeleaf, HTML5, CSS3, JavaScript
- **Build Tool:** Maven

## 📋 Prerequisites

Before running the application, ensure you have:

1. **Java 17** or higher installed
2. **MySQL 8.0** or higher installed and running
3. **Maven** installed (or use the included Maven wrapper)

## 🚀 Quick Start

### 1. Clone/Setup the Project

```bash
cd B2B_Application
```

### 2. Configure Database

The application will automatically create the database. Just ensure MySQL is running with:
- **Host:** localhost
- **Port:** 3306
- **Username:** root
- **Password:** root

To use different credentials, update `src/main/resources/application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/a2b_b2b_catering?createDatabaseIfNotExist=true
spring.datasource.username=your_username
spring.datasource.password=your_password
```

### 3. Build the Application

```bash
# Windows
mvnw.cmd clean install

# Linux/Mac
./mvnw clean install
```

### 4. Run the Application

```bash
# Windows
mvnw.cmd spring-boot:run

# Linux/Mac
./mvnw spring-boot:run
```

### 5. Access the Application

Open your browser and navigate to:
```
http://localhost:8080
```

## 🔐 Default Login Credentials

| Role | Username | Password |
|------|----------|----------|
| Admin | admin | admin123 |
| Manager | manager | manager123 |
| Staff | staff | staff123 |

## 📁 Project Structure

```
B2B_Application/
├── src/
│   ├── main/
│   │   ├── java/com/example/B2B_Application/
│   │   │   ├── config/           # Security & Data config
│   │   │   ├── controller/       # Web & REST controllers
│   │   │   ├── entity/           # JPA entities
│   │   │   ├── repository/       # Data repositories
│   │   │   └── service/          # Business logic
│   │   └── resources/
│   │       ├── static/
│   │       │   ├── css/          # Stylesheets
│   │       │   └── js/           # JavaScript files
│   │       ├── templates/        # Thymeleaf templates
│   │       │   ├── customers/    # Customer views
│   │       │   ├── orders/       # Order views
│   │       │   ├── payments/     # Payment views
│   │       │   └── fragments/    # Reusable components
│   │       └── application.properties
│   └── test/
├── pom.xml
└── README.md
```

## 📊 Database Schema

### Tables Created:
- `customers` - Customer information
- `catering_orders` - Order/booking details
- `payments` - Payment transactions
- `users` - System users
- `menu_items` - Menu catalog

## 🎨 UI Features

- Modern dark theme with gold accents
- Responsive design for all devices
- Interactive dashboard with statistics
- Clean data tables with sorting
- Form validation with error messages
- Toast notifications for actions
- Print-ready payment receipts

## 🔧 Configuration Options

### Change Server Port
```properties
server.port=8081
```

### Enable SQL Logging
```properties
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```

## 📝 API Endpoints

### REST API (for future mobile/integration)

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/orders` | GET | List all orders |
| `/api/orders/{id}` | GET | Get order details |
| `/api/orders/upcoming` | GET | Get upcoming orders |
| `/api/orders/stats` | GET | Get dashboard stats |
| `/api/customers` | GET | List all customers |
| `/api/customers/search` | GET | Search customers |

## 🔒 Security Features

- Form-based authentication
- Role-based access control
- Session management
- CSRF protection (can be enabled)
- Password encryption (BCrypt)

## 📈 Future Enhancements

- [ ] Email notifications for bookings
- [ ] SMS alerts for payment confirmations
- [ ] Report generation (PDF/Excel)
- [ ] Menu management module
- [ ] Invoice generation
- [ ] Calendar view for events
- [ ] Mobile responsive PWA

## 🐛 Troubleshooting

### MySQL Connection Issues
```bash
# Check if MySQL is running
mysql -u root -p

# Create database manually if needed
CREATE DATABASE a2b_b2b_catering;
```

### Port Already in Use
```properties
# Change port in application.properties
server.port=8081
```

### Build Errors
```bash
# Clean and rebuild
mvnw clean install -DskipTests
```

## 📄 License

This project is licensed under the MIT License.

## 👥 Support

For support, email: support@a2bhotel.com

---

**A2B Hotel** - Premium B2B Catering Services

