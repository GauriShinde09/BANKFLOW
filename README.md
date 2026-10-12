# BANKFLOW — Full-Stack Banking Application

A full-stack banking demo built to practise real-world Java backend development, React UI development, authentication, database design, and deployment.

**Live application:** https://bankflow-frontend.vercel.app/  
**Backend API:** https://bankflow-backend-mhnx.onrender.com/

> **Educational demo only:** BANKFLOW is a learning/portfolio project, not a real banking service. Do not enter real financial or sensitive personal information.

## Repositories

This project is maintained in separate frontend and backend repositories so each application can be developed and deployed independently.

- **Frontend — React + Tailwind CSS:** [BANKFLOW-frontend](https://github.com/GauriShinde09/BANKFLOW-frontend)
- **Backend — Spring Boot REST API:** [BANKFLOW-backend](https://github.com/GauriShinde09/BANKFLOW-backend)

## Project Overview

BANKFLOW brings common banking workflows into one web application. Customers can manage account activity, make transfers, view transactions, apply for loans, and track repayments. Admin features support account status management and loan administration.

## Main Features

### Authentication and Security
- User registration and login
- JWT-based authentication
- Role-based access for customers and admins
- Forgot-password and password-reset workflow using email
- Passwords stored as BCrypt hashes

### Banking
- View account details and balance
- Deposit and withdraw funds
- Transfer funds between accounts
- Beneficiary management and beneficiary transfers
- Paginated transaction history with debit/credit details
- Download account statement as PDF
- Admin account freeze and unfreeze controls

### Loans
- Browse active loan types
- Apply for a loan with amount, tenure, and monthly income
- Basic EMI-based eligibility check
- Admin loan-type management
- Admin review, approval, or rejection of applications
- Loan disbursement
- Repayment schedule with principal, interest, and remaining balance
- EMI repayment tracking

## Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | React, Vite, Tailwind CSS, Axios, React Router |
| Backend | Java, Spring Boot, Spring Security, Spring Data JPA / Hibernate, REST APIs |
| Authentication | JWT, BCrypt password hashing, role-based authorization |
| Database | MySQL |
| PDF statements | Apache PDFBox |
| Email | Spring Boot Mail / SMTP |
| Deployment | Vercel (frontend), Render (backend), Aiven (MySQL) |
| Tools | Git, GitHub, Postman, Maven, VS Code / Spring Tools |

## Architecture

```text
                     ┌─────────────────────────┐
                     │  User's Browser          │
                     └────────────┬────────────┘
                                  │ HTTPS
                                  ▼
                     ┌─────────────────────────┐
                     │ React + Tailwind UI     │
                     │ Vercel                  │
                     └────────────┬────────────┘
                                  │ REST / JSON + JWT
                                  ▼
                     ┌─────────────────────────┐
                     │ Spring Boot REST API    │
                     │ Spring Security + JWT   │
                     │ Render                  │
                     └────────────┬────────────┘
                                  │ JPA / Hibernate
                                  ▼
                     ┌─────────────────────────┐
                     │ MySQL Database          │
                     │ Aiven                   │
                     └─────────────────────────┘
```

## Try the Live Demo

1. Open the [BANKFLOW web application](https://bankflow-frontend.vercel.app/).
2. Register a demo account or sign in with a test account you own.
3. Explore the banking and loan features available to that account's role.

The backend may take a short time to respond after inactivity depending on the hosting plan. Never publish test credentials, JWTs, passwords, or environment-variable values in this repository.

## Local Development

For source code and project-specific setup, use the dedicated repositories:

- [Frontend repository and setup](https://github.com/GauriShinde09/BANKFLOW-frontend)
- [Backend repository and setup](https://github.com/GauriShinde09/BANKFLOW-backend)

Configure environment variables locally for database access, email, the frontend origin, and the JWT secret. Keep real credentials in local environment settings and hosting-platform secret settings; do not commit them to GitHub. The frontend uses `VITE_API_BASE_URL` to choose the backend API URL.

## Security Notes

- Use only demo data in this portfolio project.
- Never commit passwords, app passwords, database URLs containing credentials, JWT secrets, access tokens, or SQL dumps.
- Use a strong, private JWT signing secret in the deployment environment.
- Production financial services require additional security reviews, monitoring, compliance controls, and testing beyond this educational project.

## Author

**Gauri Shinde**  
GitHub: [@GauriShinde09](https://github.com/GauriShinde09)

---

*Built as a full-stack learning project to practise secure API development, database-backed workflows, and cloud deployment.*
