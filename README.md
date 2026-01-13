# AI-Powered Microservices Job Portal

An enterprise-ready, **AI-integrated Job Portal** built using a highly scalable **Microservices Architecture**. This platform moves beyond traditional job boards by leveraging **Generative AI** to provide candidates with automated resume analysis and personalized career roadmaps.

The system is engineered for high reliability and performance, utilizing **Apache Kafka** for asynchronous background processing (such as critical email notifications) and **Redis** for high-speed token management and password reset flows. By decoupling services like Payments, Auth, and AI Utilities, the architecture ensures that the failure of one service does not compromise the integrity of the entire ecosystem.

---

## 🛠️ Comprehensive Tech Stack

### **Core Frameworks & Languages**

* **Frontend**: [Next.js](https://nextjs.org/) 14+ (App Router), TypeScript, Tailwind CSS.
* **Backend**: Node.js, Express.js, TypeScript.
* **Runtime Environment**: Docker (for containerized Kafka services).

### **Databases & State Management**

* **PostgreSQL**: Hosted on [Neon DB](https://neon.tech/) for serverless relational data storage.
* **Redis**: Hosted on [Upstash](https://upstash.com/) for fast session handling and secure reset tokens.
* **Context API**: Global state management in the frontend for user sessions and real-time notifications.

### **Microservices & Communication**

* **Message Broker**: [Apache Kafka](https://kafka.apache.org/) handles background email queues.
* **HTTP Client**: [Axios](https://axios-http.com/) for inter-service communication and frontend API calls.
* **Real-time Mailer**: [Nodemailer](https://nodemailer.com/) integrated with Kafka consumers.

### **AI & Third-Party Integrations**

* **AI Engine**: [Google Gemini AI](https://deepmind.google/technologies/gemini/) (Pro & Flash models) for Resume Analysis and Career Guidance.
* **Payment Gateway**: [Razorpay](https://razorpay.com/) for premium job-seeker subscriptions.
* **Cloud Storage**: [Cloudinary](https://cloudinary.com/) for storing profile pictures and PDF resumes.

### **UI Components & Icons**

* **UI Library**: [Shadcn UI](https://ui.shadcn.com/) for high-quality, accessible components.
* **Iconography**: [Lucide React](https://lucide.dev/) icons.
* **Toast Notifications**: [React Hot Toast](https://react-hot-toast.com/).

---

## 🚀 Key Features

* **AI Resume Analyzer**: Uses Gemini AI to provide an ATS compatibility score and point-by-point improvement suggestions.
* **AI Career Guide**: Generates a custom learning roadmap and job recommendations based on a user's technical stack.
* **Priority Application System**: A subscription model where premium users' resumes are highlighted and prioritized for recruiters.
* **Kafka-Powered Notifications**: Ensures application status updates and password resets are sent reliably via asynchronous email workers.
* **Secure Authentication**: Custom JWT implementation with **Bearer Token** verification and **Redis-backed** secure reset flows.
* **Relational Data Integrity**: Built with raw SQL (PostgreSQL) for complex joins and cascading deletes.

---

## 📸 Screenshots

| Feature | Screenshot |
| --- | --- |
| **Hero Section** |  |
| **AI Career Guide** |  |
| **Resume Analyzer** |  |
| **Recruiter Dashboard** |  |

---

## ⚙️ Setup & Installation

### **1. Environmental Variables (.env)**

You must configure unique `.env` files for **each** microservice folder and the frontend.

**Common Keys Required:**

```env
PORT=xxxx
DATABASE_URL=your_postgresql_url
REDIS_URL=your_upstash_redis_url
JWT_SEC=your_secret_key
KAFKA_BROKER=localhost:9092

```

### **2. Execution Order**

1. **Start Infrastructure**: Ensure your Kafka Docker container is running.
2. **Install Dependencies**: Run `npm install` in the root and all service directories.
3. **Compile Services**: Run `npx tsc` in each backend folder to generate the `dist` files.
4. **Launch Ecosystem**: Run `npm run dev` in all backend terminals and the frontend terminal.

---

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project.
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`).
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the Branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

---

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.
