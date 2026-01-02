
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Steve Perry VIP | Exclusive Fan Portal</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700&family=Playfair+Display:wght@400;500;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #1a1a2e;
            --secondary: #16213e;
            --accent: #e63946;
            --gold: #d4af37;
            --platinum: #e5e4e2;
            --light: #f8f9fa;
            --gray: #6c757d;
            --transition: all 0.3s ease;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            line-height: 1.6;
            color: var(--light);
            background-color: var(--primary);
            overflow-x: hidden;
        }

        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .container {
            width: 100%;
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header & Navigation */
        header {
            background-color: rgba(22, 33, 62, 0.95);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            padding: 15px 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            backdrop-filter: blur(10px);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo-icon {
            color: var(--gold);
            font-size: 2rem;
        }

        .logo-text {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            font-weight: 700;
            background: linear-gradient(to right, var(--gold), #fff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        .nav-links a {
            color: var(--light);
            text-decoration: none;
            font-weight: 500;
            font-size: 1rem;
            transition: var(--transition);
            position: relative;
        }

        .nav-links a:hover {
            color: var(--gold);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--gold);
            transition: var(--transition);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .user-controls {
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .user-icon {
            font-size: 1.5rem;
            color: var(--gold);
            cursor: pointer;
        }

        .btn {
            padding: 10px 24px;
            border-radius: 30px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            transition: var(--transition);
            border: none;
            font-size: 0.9rem;
        }

        .btn-primary {
            background-color: var(--accent);
            color: white;
        }

        .btn-primary:hover {
            background-color: #c1121f;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(230, 57, 70, 0.3);
        }

        .btn-secondary {
            background-color: transparent;
            color: var(--gold);
            border: 2px solid var(--gold);
        }

        .btn-secondary:hover {
            background-color: rgba(212, 175, 55, 0.1);
            transform: translateY(-3px);
        }

        .btn-platinum {
            background-color: var(--platinum);
            color: var(--primary);
            font-weight: 700;
        }

        .btn-platinum:hover {
            background-color: #fff;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(229, 228, 226, 0.4);
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), 
                        url('https://images.unsplash.com/photo-1489599809516-9827b6d1cf13?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            position: relative;
            margin-top: 70px;
        }

        .hero-content {
            max-width: 700px;
            animation: fadeUp 1s ease-out;
        }

        @keyframes fadeUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            line-height: 1.2;
        }

        .hero h1 span {
            color: var(--gold);
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            color: rgba(255, 255, 255, 0.9);
            max-width: 600px;
        }

        /* Features Section */
        .section-title {
            text-align: center;
            margin: 80px 0 50px;
            position: relative;
        }

        .section-title h2 {
            font-size: 2.5rem;
            display: inline-block;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: var(--accent);
        }

        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 80px;
        }

        .feature-card {
            background-color: var(--secondary);
            border-radius: 10px;
            overflow: hidden;
            transition: var(--transition);
            height: 100%;
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }

        .feature-icon {
            height: 180px;
            background-color: rgba(212, 175, 55, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            color: var(--gold);
        }

        .feature-content {
            padding: 25px;
        }

        .feature-content h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }

        /* Exclusive Content */
        .exclusive-content {
            background-color: var(--secondary);
            padding: 80px 0;
            margin: 80px 0;
        }

        .content-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .content-card {
            border-radius: 10px;
            overflow: hidden;
            position: relative;
            height: 300px;
            cursor: pointer;
        }

        .content-card img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }

        .content-card:hover img {
            transform: scale(1.05);
        }

        .content-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(to top, rgba(0, 0, 0, 0.9), transparent);
            padding: 30px 20px 20px;
            color: white;
        }

        .content-overlay h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
        }

        .vip-badge {
            background-color: var(--gold);
            color: var(--primary);
            font-weight: 700;
            padding: 5px 10px;
            border-radius: 4px;
            font-size: 0.8rem;
            position: absolute;
            top: 15px;
            right: 15px;
        }

        /* Membership Tiers - UPDATED FOR LUXURY PRICING */
        .tiers {
            margin: 80px 0;
        }

        .tier-cards {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 30px;
        }

        .tier-card {
            background-color: var(--secondary);
            border-radius: 15px;
            padding: 40px 30px;
            width: 100%;
            max-width: 380px;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: var(--transition);
            position: relative;
            overflow: hidden;
        }

        .tier-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(to right, var(--gold), var(--platinum));
        }

        .tier-card.featured {
            border-color: var(--gold);
            transform: scale(1.05);
            box-shadow: 0 15px 40px rgba(212, 175, 55, 0.3);
            background: linear-gradient(to bottom, rgba(22, 33, 62, 0.9), rgba(10, 15, 35, 0.95));
        }

        .tier-card.featured::before {
            background: linear-gradient(to right, #ffd700, var(--gold), #ffd700);
            height: 7px;
        }

        .tier-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
        }

        .tier-card.featured:hover {
            transform: scale(1.05) translateY(-15px);
        }

        .tier-name {
            font-size: 2rem;
            margin-bottom: 10px;
            color: var(--gold);
        }

        .tier-card.featured .tier-name {
            color: var(--platinum);
            text-shadow: 0 0 10px rgba(212, 175, 55, 0.5);
        }

        .tier-price {
            font-size: 3rem;
            font-weight: 800;
            margin-bottom: 20px;
            color: var(--light);
        }

        .tier-card.featured .tier-price {
            color: var(--platinum);
        }

        .tier-price span {
            font-size: 1.2rem;
            color: var(--gray);
            font-weight: 400;
        }

        .tier-period {
            font-size: 1rem;
            color: var(--gray);
            margin-bottom: 25px;
            display: block;
        }

        .tier-features {
            list-style: none;
            margin-bottom: 30px;
            text-align: left;
        }

        .tier-features li {
            padding: 12px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            display: flex;
            align-items: center;
        }

        .tier-features li i {
            color: var(--gold);
            margin-right: 15px;
            font-size: 1.1rem;
            min-width: 20px;
        }

        .tier-features li.featured i {
            color: var(--platinum);
        }

        .tier-note {
            font-size: 0.9rem;
            color: var(--gray);
            font-style: italic;
            margin-top: 20px;
        }

        /* Footer */
        footer {
            background-color: #0f1424;
            padding: 60px 0 30px;
            margin-top: 80px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-column h3 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: var(--gold);
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 12px;
        }

        .footer-links a {
            color: rgba(255, 255, 255, 0.7);
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-links a:hover {
            color: var(--gold);
            padding-left: 5px;
        }

        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            transition: var(--transition);
        }

        .social-icons a:hover {
            background-color: var(--gold);
            transform: translateY(-5px);
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            color: rgba(255, 255, 255, 0.5);
            font-size: 0.9rem;
        }

        /* Luxury Badge */
        .luxury-badge {
            position: absolute;
            top: 20px;
            right: 20px;
            background: linear-gradient(45deg, var(--gold), #ffd700);
            color: var(--primary);
            font-weight: 700;
            padding: 8px 15px;
            border-radius: 30px;
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            box-shadow: 0 4px 10px rgba(212, 175, 55, 0.3);
        }

        /* Mobile Navigation */
        .mobile-menu-btn {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--light);
        }

        /* Login Popup Styles */
        .login-popup-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.85);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 2000;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.3s ease, visibility 0.3s ease;
        }

        .login-popup-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .login-popup {
            background: linear-gradient(145deg, var(--secondary), #0d142b);
            width: 90%;
            max-width: 500px;
            border-radius: 15px;
            padding: 40px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(212, 175, 55, 0.2);
            position: relative;
            transform: translateY(30px);
            transition: transform 0.4s ease;
        }

        .login-popup-overlay.active .login-popup {
            transform: translateY(0);
        }

        .login-popup-close {
            position: absolute;
            top: 20px;
            right: 20px;
            background: none;
            border: none;
            color: var(--gold);
            font-size: 1.5rem;
            cursor: pointer;
            transition: var(--transition);
        }

        .login-popup-close:hover {
            transform: rotate(90deg);
            color: var(--platinum);
        }

        .login-popup h2 {
            text-align: center;
            color: var(--gold);
            font-size: 2.2rem;
            margin-bottom: 10px;
        }

        .login-popup p {
            text-align: center;
            color: rgba(255, 255, 255, 0.7);
            margin-bottom: 30px;
            font-size: 1rem;
        }

        .login-form {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .form-group {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .form-group label {
            color: var(--gold);
            font-weight: 600;
            font-size: 0.95rem;
        }

        .form-group input {
            padding: 15px 20px;
            border-radius: 10px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            background-color: rgba(0, 0, 0, 0.3);
            color: white;
            font-size: 1rem;
            transition: var(--transition);
        }

        .form-group input:focus {
            outline: none;
            border-color: var(--gold);
            box-shadow: 0 0 0 2px rgba(212, 175, 55, 0.2);
        }

        .form-group input::placeholder {
            color: rgba(255, 255, 255, 0.4);
        }

        .login-form .btn {
            margin-top: 10px;
            padding: 15px;
            font-size: 1rem;
        }

        .login-options {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 20px;
            font-size: 0.9rem;
        }

        .remember-me {
            display: flex;
            align-items: center;
            gap: 8px;
            color: rgba(255, 255, 255, 0.7);
        }

        .remember-me input {
            width: 18px;
            height: 18px;
        }

        .forgot-password {
            color: var(--gold);
            text-decoration: none;
            transition: var(--transition);
        }

        .forgot-password:hover {
            color: var(--platinum);
            text-decoration: underline;
        }

        .signup-link {
            text-align: center;
            margin-top: 25px;
            color: rgba(255, 255, 255, 0.7);
        }

        .signup-link a {
            color: var(--gold);
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
        }

        .signup-link a:hover {
            color: var(--platinum);
            text-decoration: underline;
        }

        /* Success Popup Styles */
        .success-popup-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.9);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 2001;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.3s ease, visibility 0.3s ease;
        }

        .success-popup-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .success-popup {
            background: linear-gradient(145deg, var(--secondary), #0d142b);
            width: 90%;
            max-width: 600px;
            border-radius: 15px;
            padding: 50px 40px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);
            border: 2px solid var(--gold);
            position: relative;
            text-align: center;
            transform: scale(0.9);
            transition: transform 0.4s ease;
        }

        .success-popup-overlay.active .success-popup {
            transform: scale(1);
        }

        .success-popup-close {
            position: absolute;
            top: 20px;
            right: 20px;
            background: none;
            border: none;
            color: var(--gold);
            font-size: 1.5rem;
            cursor: pointer;
            transition: var(--transition);
        }

        .success-popup-close:hover {
            transform: rotate(90deg);
            color: var(--platinum);
        }

        .success-icon {
            font-size: 5rem;
            color: var(--gold);
            margin-bottom: 20px;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }

        .success-popup h2 {
            color: var(--gold);
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .success-popup p {
            color: rgba(255, 255, 255, 0.9);
            font-size: 1.2rem;
            line-height: 1.6;
            margin-bottom: 30px;
        }

        .success-popup .btn {
            margin-top: 10px;
        }

        /* Dashboard Styles - New Addition */
        .dashboard-section {
            display: none;
            padding-top: 100px;
            min-height: 100vh;
        }

        .dashboard-section.active {
            display: block;
        }

        .dashboard-header {
            background: linear-gradient(145deg, var(--secondary), #0d142b);
            padding: 60px 0 40px;
            margin-bottom: 40px;
            border-bottom: 1px solid rgba(212, 175, 55, 0.2);
        }

        .dashboard-welcome {
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
        }

        .dashboard-welcome h1 {
            font-size: 3rem;
            color: var(--gold);
            margin-bottom: 10px;
        }

        .dashboard-welcome p {
            font-size: 1.2rem;
            color: rgba(255, 255, 255, 0.8);
            margin-bottom: 30px;
        }

        .dashboard-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }

        .dashboard-card {
            background: linear-gradient(145deg, var(--secondary), #0d142b);
            border-radius: 15px;
            padding: 30px;
            border: 1px solid rgba(255, 255, 255, 0.05);
            transition: var(--transition);
        }

        .dashboard-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }

        .dashboard-card h3 {
            color: var(--gold);
            font-size: 1.5rem;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .dashboard-card h3 i {
            font-size: 1.2rem;
        }

        .user-info {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .info-item {
            display: flex;
            justify-content: space-between;
            padding: 12px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }

        .info-label {
            color: rgba(255, 255, 255, 0.7);
            font-weight: 500;
        }

        .info-value {
            color: var(--light);
            font-weight: 600;
        }

        .membership-status {
            background: linear-gradient(45deg, rgba(212, 175, 55, 0.1), transparent);
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
        }

        .status-badge {
            display: inline-block;
            background: linear-gradient(45deg, var(--gold), #ffd700);
            color: var(--primary);
            font-weight: 700;
            padding: 8px 20px;
            border-radius: 30px;
            margin-bottom: 15px;
        }

        .progress-bar {
            height: 8px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 4px;
            margin: 20px 0;
            overflow: hidden;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(to right, var(--gold), var(--accent));
            border-radius: 4px;
            width: 75%;
        }

        .quick-stats {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin-top: 20px;
        }

        .stat-item {
            text-align: center;
            padding: 15px;
            background-color: rgba(0, 0, 0, 0.2);
            border-radius: 10px;
        }

        .stat-value {
            font-size: 2rem;
            font-weight: 700;
            color: var(--gold);
            margin-bottom: 5px;
        }

        .stat-label {
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.7);
        }

        .recent-activity {
            list-style: none;
        }

        .activity-item {
            display: flex;
            align-items: center;
            gap: 15px;
            padding: 15px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }

        .activity-item:last-child {
            border-bottom: none;
        }

        .activity-icon {
            width: 40px;
            height: 40px;
            background-color: rgba(212, 175, 55, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--gold);
            font-size: 1.2rem;
        }

        .activity-content h4 {
            font-size: 1rem;
            margin-bottom: 5px;
            color: var(--light);
        }

        .activity-content p {
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.6);
        }

        .activity-time {
            font-size: 0.8rem;
            color: var(--gray);
        }

        .dashboard-actions {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
        }

        .dashboard-actions .btn {
            flex: 1;
            min-width: 150px;
            text-align: center;
        }

        .exclusive-access-list {
            list-style: none;
        }

        .access-item {
            display: flex;
            align-items: center;
            gap: 15px;
            padding: 12px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }

        .access-item:last-child {
            border-bottom: none;
        }

        .access-item i {
            color: var(--gold);
            font-size: 1.2rem;
        }

        /* Responsive Styles */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 2.8rem;
            }
            
            .tier-cards {
                flex-direction: column;
                align-items: center;
            }
            
            .tier-card.featured {
                transform: none;
            }
            
            .tier-card.featured:hover {
                transform: translateY(-15px);
            }
            
            .tier-price {
                font-size: 2.5rem;
            }
            
            .dashboard-welcome h1 {
                font-size: 2.5rem;
            }
        }

        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }
            
            .nav-links {
                position: fixed;
                top: 70px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 70px);
                background-color: var(--secondary);
                flex-direction: column;
                align-items: center;
                justify-content: flex-start;
                padding-top: 50px;
                transition: var(--transition);
                gap: 30px;
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .login-popup {
                padding: 30px 20px;
            }
            
            .login-popup h2 {
                font-size: 1.8rem;
            }
            
            .dashboard-grid {
                grid-template-columns: 1fr;
            }
            
            .quick-stats {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <div class="logo-icon">
                    <i class="fas fa-crown"></i>
                </div>
                <div class="logo-text">SP VIP</div>
            </div>
            
            <div class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fas fa-bars"></i>
            </div>
            
            <nav>
                <ul class="nav-links" id="navLinks">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#features">Features</a></li>
                    <li><a href="#exclusive">Exclusive Content</a></li>
                    <li><a href="#tiers">Membership</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#dashboard" id="dashboardLink" style="display: none;">Dashboard</a></li>
                </ul>
            </nav>
            
            <div class="user-controls">
                <div class="user-icon">
                    <i class="fas fa-user-circle"></i>
                </div>
                <button class="btn btn-primary" id="loginBtn">VIP Login</button>
            </div>
        </div>
    </header>

    <!-- Main Content Sections (Hidden when dashboard is active) -->
    <main id="mainContent">
        <!-- Hero Section -->
        <section class="hero" id="home">
            <div class="container">
                <div class="hero-content">
                    <h1>The Ultimate <span>Steve Perry</span> VIP Experience</h1>
                    <p>An exclusive, invitation-only portal for Steve Perry's most dedicated patrons. Access unparalleled experiences, personal interactions, and content unavailable anywhere else in the world.</p>
                    <div class="hero-buttons">
                        <button class="btn btn-primary" style="margin-right: 15px;" id="applyMembershipBtn">Apply for Membership</button>
                        <button class="btn btn-secondary" id="consultationBtn">Schedule a Consultation</button>
                    </div>
                </div>
            </div>
        </section>

        <!-- Features Section -->
        <section class="container" id="features">
            <div class="section-title">
                <h2>Unparalleled VIP Benefits</h2>
            </div>
            
            <div class="features">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-film"></i>
                    </div>
                    <div class="feature-content">
                        <h3>Ultimate Content Access</h3>
                        <p>Unrestricted access to Steve's personal archives, unreleased projects, and exclusive behind-the-scenes footage from his entire career.</p>
                    </div>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-ticket-alt"></i>
                    </div>
                    <div class="feature-content">
                        <h3>Premier Event Access</h3>
                        <p>VIP seating at all premieres, exclusive after-parties, and private screenings with Steve perry  and industry insiders.</p>
                    </div>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-users"></i>
                    </div>
                    <div class="feature-content">
                        <h3>Elite Community</h3>
                        <p>Connect with fellow elite patrons in our exclusive circles. Networking events with industry leaders and celebrities.</p>
                    </div>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-gift"></i>
                    </div>
                    <div class="feature-content">
                        <h3>Personalized Memorabilia</h3>
                        <p>Custom, personally signed memorabilia, props from actual film sets, and limited edition collections created exclusively for members.</p>
                    </div>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-calendar-star"></i>
                    </div>
                    <div class="feature-content">
                        <h3>Private Experiences</h3>
                        <p>Private dinners, set visits, one-on-one conversations, and personalized video messages from Steve Perry himself.</p>
                    </div>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-newspaper"></i>
                    </div>
                    <div class="feature-content">
                        <h3>First Access & Influence</h3>
                        <p>Be the first to know about projects in development, provide input on creative decisions, and receive personal updates.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Exclusive Content Section -->
        <section class="exclusive-content" id="exclusive">
            <div class="container">
                <div class="section-title">
                    <h2>Exclusive Content</h2>
                </div>
                
                <div class="content-grid">
                    <div class="content-card">
                        <div class="vip-badge">ULTIMATE ACCESS</div>
                        <img src="https://images.unsplash.com/photo-1489599809516-9827b6d1cf13?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Behind the Scenes">
                        <div class="content-overlay">
                            <h3>Behind The Scenes: "Has Fallen"</h3>
                            <p>Exclusive look at the making of the latest action thriller</p>
                        </div>
                    </div>
                    
                    <div class="content-card">
                        <div class="vip-badge">PRIVATE EVENT</div>
                        <img src="https://images.unsplash.com/photo-1513106580091-1d82408b8cd6?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Q&A Session">
                        <div class="content-overlay">
                            <h3>Live Q&A with Steve Perry</h3>
                            <p>Recording of our exclusive members-only virtual event</p>
                        </div>
                    </div>
                    
                    <div class="content-card">
                        <div class="vip-badge">PERSONAL ARCHIVE</div>
                        <img src="https://images.unsplash.com/photo-1493225457124-a3eb161ffa5f?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Personal Vlog">
                        <div class="content-overlay">
                            <h3>Personal Vlog: Scotland Retreat</h3>
                            <p>Join steve perry on a personal trip back to his roots in california</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Membership Tiers - UPDATED WITH LUXURY PRICING -->
        <section class="container tiers" id="tiers">
            <div class="section-title">
                <h2>Elite Membership Tiers</h2>
            </div>
            
            <div class="tier-cards">
                <div class="tier-card">
                    <div class="luxury-badge">Exclusive</div>
                    <div class="tier-name">Patron</div>
                    <div class="tier-price">$5,000<span>+</span></div>
                    <span class="tier-period">Annual Membership</span>
                    <ul class="tier-features">
                        <li><i class="fas fa-check"></i> All digital exclusive content access</li>
                        <li><i class="fas fa-check"></i> Invitation to 2 virtual events annually</li>
                        <li><i class="fas fa-check"></i> Limited edition signed merchandise</li>
                        <li><i class="fas fa-check"></i> Priority booking for public events</li>
                        <li><i class="fas fa-check"></i> Members-only newsletter & updates</li>
                        <li><i class="fas fa-check"></i> Access to patron community forums</li>
                    </ul>
                    <button class="btn btn-secondary" id="inquireBtn">Inquire Now</button>
                    <p class="tier-note">Annual commitment required</p>
                </div>
                
                <div class="tier-card featured">
                    <div class="luxury-badge">Premium</div>
                    <div class="tier-name">Elite</div>
                    <div class="tier-price">$15,000<span>+</span></div>
                    <span class="tier-period">Annual Membership</span>
                    <ul class="tier-features">
                        <li class="featured"><i class="fas fa-check"></i> All Patron benefits</li>
                        <li class="featured"><i class="fas fa-check"></i> Invitation to 4 in-person events annually</li>
                        <li class="featured"><i class="fas fa-check"></i> Personal video message from Gerard</li>
                        <li class="featured"><i class="fas fa-check"></i> Set visit to current production (1 annually)</li>
                        <li class="featured"><i class="fas fa-check"></i> Personalized signed memorabilia collection</li>
                        <li class="featured"><i class="fas fa-check"></i> Priority access to premieres & after-parties</li>
                        <li class="featured"><i class="fas fa-check"></i> Direct communication with management team</li>
                    </ul>
                    <button class="btn btn-platinum" id="applyEliteBtn">Apply for Membership</button>
                    <p class="tier-note">Includes all Patron benefits plus exclusive additions</p>
                </div>
                
                <div class="tier-card">
                    <div class="luxury-badge">Ultimate</div>
                    <div class="tier-name">Connoisseur</div>
                    <div class="tier-price">$35,000<span>+</span></div>
                    <span class="tier-period">Annual Membership</span>
                    <ul class="tier-features">
                        <li><i class="fas fa-check"></i> All Elite benefits</li>
                        <li><i class="fas fa-check"></i> Private dinner with Gerard (1 annually)</li>
                        <li><i class="fas fa-check"></i> Unlimited set visits (subject to scheduling)</li>
                        <li><i class="fas fa-check"></i> Original props from Gerard's films</li>
                        <li><i class="fas fa-check"></i> Executive producer credit on select projects</li>
                        <li><i class="fas fa-check"></i> 24/7 dedicated member concierge</li>
                        <li><i class="fas fa-check"></i> Creative input opportunities on projects</li>
                    </ul>
                    <button class="btn btn-secondary" id="scheduleConsultationBtn">Schedule Consultation</button>
                    <p class="tier-note">Customizable packages available - contact for details</p>
                </div>
            </div>
            
            <div style="text-align: center; margin-top: 50px; max-width: 800px; margin-left: auto; margin-right: auto;">
                <h3 style="color: var(--gold); margin-bottom: 20px;">Bespoke Membership Packages</h3>
                <p style="color: rgba(255, 255, 255, 0.8);">For those seeking truly unique experiences, we offer fully customized membership packages starting at $75,000 annually. These include personalized experiences, investment opportunities in 's projects, and unparalleled access. Contact our membership director for a private consultation.</p>
                <button class="btn btn-primary" style="margin-top: 20px;" id="contactDirectorBtn">Contact Membership Director</button>
            </div>
        </section>

        <!-- Footer -->
        <footer id="about">
            <div class="container">
                <div class="footer-content">
                    <div class="footer-column">
                        <h3>ST VIP Portal</h3>
                        <p>The ultimate exclusive community for Steve perry most dedicated patrons. An invitation-only experience offering unparalleled access and bespoke interactions.</p>
                        <div class="social-icons">
                            <a href="#"><i class="fab fa-facebook-f"></i></a>
                            <a href="#"><i class="fab fa-twitter"></i></a>
                            <a href="#"><i class="fab fa-instagram"></i></a>
                            <a href="#"><i class="fab fa-youtube"></i></a>
                        </div>
                    </div>
                    
                    <div class="footer-column">
                        <h3>Quick Links</h3>
                        <ul class="footer-links">
                            <li><a href="#home">Home</a></li>
                            <li><a href="#features">Features</a></li>
                            <li><a href="#exclusive">Exclusive Content</a></li>
                            <li><a href="#tiers">Membership</a></li>
                            <li><a href="#">FAQ</a></li>
                        </ul>
                    </div>
                    
                    <div class="footer-column">
                        <h3>Legal</h3>
                        <ul class="footer-links">
                            <li><a href="#">Privacy Policy</a></li>
                            <li><a href="#">Terms of Service</a></li>
                            <li><a href="#">Cookie Policy</a></li>
                            <li><a href="#">Community Guidelines</a></li>
                        </ul>
                    </div>
                    
                    <div class="footer-column">
                        <h3>Member Services</h3>
                        <ul class="footer-links">
                            <li><i class="fas fa-envelope"></i> concierge@gerardbutlervip.com</li>
                            <li><i class="fas fa-phone"></i> +1 (888) 555-STVIP</li>
                            <li><i class="fas fa-map-marker-alt"></i> VIP Member Relations, Beverly Hills, CA</li>
                            <li><i class="fas fa-clock"></i> Concierge: 24/7 for Elite & Connoisseur tiers</li>
                        </ul>
                    </div>
                </div>
                
                <div class="copyright">
                    <p>&copy; 2023 Steve Perry VIP Portal. All rights reserved. This is an exclusive, invitation-only community. All memberships are subject to approval.</p>
                </div>
            </div>
        </footer>
    </main>

    <!-- Dashboard Section (Hidden by default) -->
    <section class="dashboard-section" id="dashboardSection">
        <div class="dashboard-header">
            <div class="container">
                <div class="dashboard-welcome">
                    <h1 id="dashboardUserName">Welcome Back, VIP Member!</h1>
                    <p id="dashboardUserEmail">Your exclusive portal to all Steve Peery VIP content and experiences</p>
                    <button class="btn btn-secondary" id="logoutBtn">Logout</button>
                </div>
            </div>
        </div>
        
        <div class="container">
            <div class="dashboard-grid">
                <!-- User Profile Card -->
                <div class="dashboard-card">
                    <h3><i class="fas fa-user-crown"></i> VIP Profile</h3>
                    <div class="user-info">
                        <div class="info-item">
                            <span class="info-label">Full Name:</span>
                            <span class="info-value" id="profileName"></span>
                        </div>
                        <div class="info-item">
                            <span class="info-label">Email:</span>
                            <span class="info-value" id="profileEmail"></span>
                        </div>
                        <div class="info-item">
                            <span class="info-label">Member Since:</span>
                            <span class="info-value">January, 2025</span>
                        </div>
                        <div class="info-item">
                            <span class="info-label">VIP ID:</span>
                            <span class="info-value">ST-VIP-2023-00142</span>
                        </div>
                        <div class="info-item">
                            <span class="info-label">Location:</span>
                            <span class="info-value">United States</span>
                        </div>
                    </div>
                    
                    <div class="membership-status">
                        <div class="status-badge">ELITE MEMBER</div>
                        <p>Your membership renews on: <strong>December, 2026</strong></p>
                        <div class="progress-bar">
                            <div class="progress-fill"></div>
                        </div>
                        <p>90% of membership year remaining</p>
                    </div>
                </div>
                
                <!-- Membership Stats Card -->
                <div class="dashboard-card">
                    <h3><i class="fas fa-chart-line"></i> Membership Overview</h3>
                    <div class="quick-stats">
                        <div class="stat-item">
                            <div class="stat-value">12</div>
                            <div class="stat-label">Exclusive Events</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-value">47</div>
                            <div class="stat-label">Content Access</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-value">3</div>
                            <div class="stat-label">Set Visits</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-value">$15K</div>
                            <div class="stat-label">Tier Level</div>
                        </div>
                    </div>
                    
                    <h3 style="margin-top: 30px;"><i class="fas fa-crown"></i> Membership Benefits</h3>
                    <ul class="exclusive-access-list">
                        <li class="access-item">
                            <i class="fas fa-check-circle"></i>
                            <span>Full digital content library access</span>
                        </li>
                        <li class="access-item">
                            <i class="fas fa-check-circle"></i>
                            <span>4 in-person events annually</span>
                        </li>
                        <li class="access-item">
                            <i class="fas fa-check-circle"></i>
                            <span>Personal video message from Steve Perry</span>
                        </li>
                        <li class="access-item">
                            <i class="fas fa-check-circle"></i>
                            <span>Annual set visit</span>
                        </li>
                    </ul>
                </div>
                
                <!-- Recent Activity Card -->
                <div class="dashboard-card">
                    <h3><i class="fas fa-history"></i> Recent Activity</h3>
                    <ul class="recent-activity">
                        <li class="activity-item">
                            <div class="activity-icon">
                                <i class="fas fa-play-circle"></i>
                            </div>
                            <div class="activity-content">
                                <h4>Watched Exclusive Content</h4>
                                <p>"Behind The Scenes: Has Fallen"</p>
                                <div class="activity-time">2 hours ago</div>
                            </div>
                        </li>
                        <li class="activity-item">
                            <div class="activity-icon">
                                <i class="fas fa-calendar-check"></i>
                            </div>
                            <div class="activity-content">
                                <h4>Event Registration</h4>
                                <p>Virtual Q&A with Gerard Butler</p>
                                <div class="activity-time">1 day ago</div>
                            </div>
                        </li>
                        <li class="activity-item">
                            <div class="activity-icon">
                                <i class="fas fa-gift"></i>
                            </div>
                            <div class="activity-content">
                                <h4>Received Exclusive Gift</h4>
                                <p>Signed "Olympus Has Fallen" poster</p>
                                <div class="activity-time">3 days ago</div>
                            </div>
                        </li>
                        <li class="activity-item">
                            <div class="activity-icon">
                                <i class="fas fa-users"></i>
                            </div>
                            <div class="activity-content">
                                <h4>Community Interaction</h4>
                                <p>Posted in VIP members forum</p>
                                <div class="activity-time">1 week ago</div>
                            </div>
                        </li>
                    </ul>
                </div>
                
                <!-- Upcoming Events Card -->
                <div class="dashboard-card">
                    <h3><i class="fas fa-calendar-star"></i> Upcoming Events</h3>
                    <ul class="recent-activity">
                        <li class="activity-item">
                            <div class="activity-icon" style="background-color: rgba(230, 57, 70, 0.1); color: var(--accent);">
                                <i class="fas fa-ticket-alt"></i>
                            </div>
                            <div class="activity-content">
                                <h4>"Kandahar" Premiere</h4>
                                <p>Red carpet event + afterparty</p>
                                <div class="activity-time">November 15, 2023</div>
                            </div>
                        </li>
                        <li class="activity-item">
                            <div class="activity-icon" style="background-color: rgba(212, 175, 55, 0.1); color: var(--gold);">
                                <i class="fas fa-video"></i>
                            </div>
                            <div class="activity-content">
                                <h4>Virtual Q&A Session</h4>
                                <p>Live with Gerard Butler</p>
                                <div class="activity-time">November 28, 2023</div>
                            </div>
                        </li>
                        <li class="activity-item">
                            <div class="activity-icon" style="background-color: rgba(229, 228, 226, 0.1); color: var(--platinum);">
                                <i class="fas fa-film"></i>
                            </div>
                            <div class="activity-content">
                                <h4>Set Visit</h4>
                                <p>"Den of Thieves 2" filming location</p>
                                <div class="activity-time">December 5, 2023</div>
                            </div>
                        </li>
                    </ul>
                    
                    <div class="dashboard-actions">
                        <button class="btn btn-secondary">View All Events</button>
                        <button class="btn btn-primary">RSVP Now</button>
                    </div>
                </div>
                
                <!-- Exclusive Content Card -->
                <div class="dashboard-card">
                    <h3><i class="fas fa-film"></i> New Exclusive Content</h3>
                    <div class="content-grid" style="grid-template-columns: 1fr; margin-top: 20px;">
                        <div class="content-card" style="height: 200px;">
                            <div class="vip-badge">NEW</div>
                            <img src="https://images.unsplash.com/photo-1489599809516-9827b6d1cf13?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Behind the Scenes">
                            <div class="content-overlay">
                                <h3>Gerard's Workout Routine</h3>
                                <p>Exclusive look at Gerard's fitness regimen</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="dashboard-actions">
                        <button class="btn btn-secondary">Browse Content Library</button>
                        <button class="btn btn-primary">Watch Now</button>
                    </div>
                </div>
                
                <!-- Quick Actions Card -->
                <div class="dashboard-card">
                    <h3><i class="fas fa-bolt"></i> Quick Actions</h3>
                    <div class="dashboard-actions" style="flex-direction: column; margin-top: 20px;">
                        <button class="btn btn-secondary">
                            <i class="fas fa-envelope"></i> Contact Concierge
                        </button>
                        <button class="btn btn-secondary">
                            <i class="fas fa-credit-card"></i> Update Payment
                        </button>
                        <button class="btn btn-secondary">
                            <i class="fas fa-user-edit"></i> Edit Profile
                        </button>
                        <button class="btn btn-primary">
                            <i class="fas fa-star"></i> Upgrade Membership
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Login Popup -->
    <div class="login-popup-overlay" id="loginPopup">
        <div class="login-popup">
            <button class="login-popup-close" id="loginCloseBtn">&times;</button>
            <h2>VIP Member Login</h2>
            <p>Access your exclusive Steve Perry VIP portal</p>
            
            <form class="login-form" id="loginForm">
                <div class="form-group">
                    <label for="name">Full Name</label>
                    <input type="text" id="name" name="name" placeholder="Enter your full name" required>
                </div>
                
                <div class="form-group">
                    <label for="email">Email Address</label>
                    <input type="email" id="email" name="email" placeholder="Enter your VIP email" required>
                </div>
                
                <div class="form-group">
                    <label for="password">Password</label>
                    <input type="password" id="password" name="password" placeholder="Enter your password" required>
                </div>
                
                <div class="login-options">
                    <div class="remember-me">
                        <input type="checkbox" id="remember">
                        <label for="remember">Remember me</label>
                    </div>
                    <a href="#" class="forgot-password">Forgot Password?</a>
                </div>
                
                <button type="submit" class="btn btn-primary">Login to VIP Portal</button>
            </form>
            
            <div class="signup-link">
                <p>Not a VIP member yet? <a href="#" id="signupLink">Apply for membership</a></p>
            </div>
        </div>
    </div>

    <!-- Success Popup -->
    <div class="success-popup-overlay" id="successPopup">
        <div class="success-popup">
            <button class="success-popup-close" id="successCloseBtn">&times;</button>
            <div class="success-icon">
                <i class="fas fa-crown"></i>
            </div>
            <h2>Welcome to the VIP Circle!</h2>
            <p id="successMessage">Congratulations! You have successfully logged into your Steve Perry VIP portal. You now have access to exclusive content, member-only events, and the entire ST VIP experience.</p>
            <button class="btn btn-primary" id="explorePortalBtn">Go to Your Dashboard</button>
        </div>
    </div>

    <script>
        // Mobile menu toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const navLinks = document.getElementById('navLinks');
        
        mobileMenuBtn.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            
            // Change menu icon
            const icon = mobileMenuBtn.querySelector('i');
            if (navLinks.classList.contains('active')) {
                icon.classList.remove('fa-bars');
                icon.classList.add('fa-times');
            } else {
                icon.classList.remove('fa-times');
                icon.classList.add('fa-bars');
            }
        });
        
        // Close mobile menu when clicking a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
                const icon = mobileMenuBtn.querySelector('i');
                icon.classList.remove('fa-times');
                icon.classList.add('fa-bars');
            });
        });

        // Login Popup Functionality
        const loginBtn = document.getElementById('loginBtn');
        const loginPopup = document.getElementById('loginPopup');
        const loginCloseBtn = document.getElementById('loginCloseBtn');
        const loginForm = document.getElementById('loginForm');
        const successPopup = document.getElementById('successPopup');
        const successCloseBtn = document.getElementById('successCloseBtn');
        const successMessage = document.getElementById('successMessage');
        const explorePortalBtn = document.getElementById('explorePortalBtn');
        const signupLink = document.getElementById('signupLink');
        const logoutBtn = document.getElementById('logoutBtn');
        const dashboardLink = document.getElementById('dashboardLink');
        
        // Dashboard elements
        const mainContent = document.getElementById('mainContent');
        const dashboardSection = document.getElementById('dashboardSection');
        const dashboardUserName = document.getElementById('dashboardUserName');
        const dashboardUserEmail = document.getElementById('dashboardUserEmail');
        const profileName = document.getElementById('profileName');
        const profileEmail = document.getElementById('profileEmail');

        // Open login popup
        loginBtn.addEventListener('click', () => {
            loginPopup.classList.add('active');
            document.body.style.overflow = 'hidden'; // Prevent scrolling
        });

        // Close login popup
        loginCloseBtn.addEventListener('click', () => {
            loginPopup.classList.remove('active');
            document.body.style.overflow = 'auto'; // Re-enable scrolling
        });

        // Close login popup when clicking outside
        loginPopup.addEventListener('click', (e) => {
            if (e.target === loginPopup) {
                loginPopup.classList.remove('active');
                document.body.style.overflow = 'auto';
            }
        });

        // Handle login form submission
        loginForm.addEventListener('submit', (e) => {
            e.preventDefault();
            
            // Get form values
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const password = document.getElementById('password').value;
            
            // Simple validation
            if (!name || !email || !password) {
                alert('Please fill in all fields');
                return;
            }
            
            // Store user data for dashboard
            localStorage.setItem('st_vip_user_name', name);
            localStorage.setItem('st_vip_user_email', email);
            
            // Close login popup
            loginPopup.classList.remove('active');
            
            // Update success message with user's name
            successMessage.innerHTML = `Congratulations <strong>${name}</strong>! You have successfully logged into your Steve Perry VIP portal. You now have exclusive access to all VIP content, member-only events, and the entire GB VIP experience.`;
            
            // Show success popup after a short delay
            setTimeout(() => {
                successPopup.classList.add('active');
                document.body.style.overflow = 'hidden';
            }, 300);
            
            // Reset form
            loginForm.reset();
        });

        // Close success popup
        successCloseBtn.addEventListener('click', () => {
            successPopup.classList.remove('active');
            document.body.style.overflow = 'auto';
        });

        // Close success popup when clicking outside
        successPopup.addEventListener('click', (e) => {
            if (e.target === successPopup) {
                successPopup.classList.remove('active');
                document.body.style.overflow = 'auto';
            }
        });

        // Explore portal button - Show dashboard
        explorePortalBtn.addEventListener('click', () => {
            successPopup.classList.remove('active');
            
            // Get user data from localStorage
            const userName = localStorage.getItem('st_vip_user_name') || 'VIP Member';
            const userEmail = localStorage.getItem('st_vip_user_email') || 'vip@example.com';
            
            // Update dashboard with user info
            dashboardUserName.textContent = `Welcome Back, ${userName}!`;
            dashboardUserEmail.textContent = userEmail;
            profileName.textContent = userName;
            profileEmail.textContent = userEmail;
            
            // Hide main content and show dashboard
            mainContent.style.display = 'none';
            dashboardSection.classList.add('active');
            
            // Show dashboard link in navigation
            dashboardLink.style.display = 'block';
            
            // Change login button to show user is logged in
            loginBtn.innerHTML = '<i class="fas fa-user-circle"></i> ' + userName.split(' ')[0];
            loginBtn.disabled = true;
            
            document.body.style.overflow = 'auto';
            
            // Scroll to top
            window.scrollTo(0, 0);
        });

        // Logout functionality
        logoutBtn.addEventListener('click', () => {
            // Clear user data
            localStorage.removeItem('st_vip_user_name');
            localStorage.removeItem('st_vip_user_email');
            
            // Hide dashboard and show main content
            dashboardSection.classList.remove('active');
            mainContent.style.display = 'block';
            
            // Hide dashboard link in navigation
            dashboardLink.style.display = 'none';
            
            // Reset login button
            loginBtn.innerHTML = 'VIP Login';
            loginBtn.disabled = false;
            
            // Scroll to top
            window.scrollTo(0, 0);
            
            // Show logout message
            alert('You have been successfully logged out.');
        });

        // Dashboard link in navigation
        dashboardLink.addEventListener('click', (e) => {
            e.preventDefault();
            
            // Get user data from localStorage
            const userName = localStorage.getItem('st_vip_user_name') || 'VIP Member';
            const userEmail = localStorage.getItem('st_vip_user_email') || 'vip@example.com';
            
            // Update dashboard with user info
            dashboardUserName.textContent = `Welcome Back, ${userName}!`;
            dashboardUserEmail.textContent = userEmail;
            profileName.textContent = userName;
            profileEmail.textContent = userEmail;
            
            // Hide main content and show dashboard
            mainContent.style.display = 'none';
            dashboardSection.classList.add('active');
            
            // Scroll to top
            window.scrollTo(0, 0);
        });

        // Signup link - open login with signup mode
        signupLink.addEventListener('click', (e) => {
            e.preventDefault();
            loginPopup.classList.remove('active');
            
            // Change the login form to signup mode
            const loginTitle = document.querySelector('.login-popup h2');
            const loginSubmit = document.querySelector('.login-form .btn');
            const signupText = document.querySelector('.signup-link p');
            
            loginTitle.textContent = 'Apply for VIP Membership';
            loginSubmit.textContent = 'Submit Application';
            signupText.innerHTML = 'Already have an account? <a href="#" id="loginLink">Login here</a>';
            
            // Re-open the popup
            setTimeout(() => {
                loginPopup.classList.add('active');
            }, 100);
            
            // Add listener for the new login link
            setTimeout(() => {
                const loginLink = document.getElementById('loginLink');
                if (loginLink) {
                    loginLink.addEventListener('click', (e) => {
                        e.preventDefault();
                        loginPopup.classList.remove('active');
                        
                        // Reset to login mode
                        loginTitle.textContent = 'VIP Member Login';
                        loginSubmit.textContent = 'Login to VIP Portal';
                        signupText.innerHTML = 'Not a VIP member yet? <a href="#" id="signupLink">Apply for membership</a>';
                        
                        // Re-open
                        setTimeout(() => {
                            loginPopup.classList.add('active');
                        }, 100);
                    });
                }
            }, 200);
        });

        // Check if user is already logged in
        document.addEventListener('DOMContentLoaded', function() {
            const userName = localStorage.getItem('gb_vip_user_name');
            
            if (userName) {
                // User is logged in, show dashboard link
                dashboardLink.style.display = 'block';
                loginBtn.innerHTML = '<i class="fas fa-user-circle"></i> ' + userName.split(' ')[0];
                loginBtn.disabled = true;
            }
            
            // Other button click animations
            document.querySelectorAll('.btn:not(#loginBtn):not(.login-popup-close):not(.success-popup-close):not(#explorePortalBtn):not(#signupLink):not(#logoutBtn)').forEach(button => {
                button.addEventListener('click', function() {
                    // Add a ripple effect
                    const ripple = document.createElement('span');
                    const rect = this.getBoundingClientRect();
                    const size = Math.max(rect.width, rect.height);
                    const x = event.clientX - rect.left - size/2;
                    const y = event.clientY - rect.top - size/2;
                    
                    ripple.style.width = ripple.style.height = size + 'px';
                    ripple.style.left = x + 'px';
                    ripple.style.top = y + 'px';
                    ripple.classList.add('ripple');
                    
                    this.appendChild(ripple);
                    
                    // Remove ripple after animation completes
                    setTimeout(() => {
                        ripple.remove();
                    }, 600);
                    
                    // Handle other button actions
                    const btnText = this.textContent.trim();
                    if (btnText.includes('Apply') || btnText.includes('Inquire') || btnText.includes('Schedule') || btnText.includes('Contact')) {
                        alert('Thank you for your interest in our exclusive VIP memberships. A member of our concierge team will contact you within 24 hours to discuss membership options and arrange a private consultation.');
                    }
                });
            });
            
            // Add luxury styling for ripple effect
            const style = document.createElement('style');
            style.textContent = `
                .ripple {
                    position: absolute;
                    border-radius: 50%;
                    background-color: rgba(255, 255, 255, 0.7);
                    transform: scale(0);
                    animation: ripple-animation 0.6s linear;
                }
                
                @keyframes ripple-animation {
                    to {
                        transform: scale(4);
                        opacity: 0;
                    }
                }
                
                .btn {
                    position: relative;
                    overflow: hidden;
                }
                
                /* Luxury hover effects for tier cards */
                .tier-card {
                    transition: transform 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275), box-shadow 0.4s ease;
                }
            `;
            document.head.appendChild(style);
            
            // Add subtle animation to tier cards on page load
            const tierCards = document.querySelectorAll('.tier-card');
            tierCards.forEach((card, index) => {
                setTimeout(() => {
                    card.style.opacity = '1';
                    card.style.transform = 'translateY(0)';
                }, 300 + (index * 200));
            });
            
            // Set initial state for animation
            tierCards.forEach(card => {
                card.style.opacity = '0';
                card.style.transform = 'translateY(30px)';
                card.style.transition = 'opacity 0.8s ease, transform 0.8s ease';
            });
        });
    </script>
</body>
</html>
