# Five9-webchat
static page to show me webchat
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Le Teleco | Home Broadband Provider</title>

  <!-- Five9 Web Chat Library -->
  <script src="https://cdn.prod.uk.five9.net/static/stable/chat/wrapper/index.js"></script>

  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      color: #333;
      background-color: #f8f9fa;
    }

    .header {
      background-color: #ffffff;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 40px;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }

    .logo {
      font-size: 1.5rem;
      font-weight: bold;
      color: #1a73e8;
    }

    .nav ul {
      list-style: none;
      display: flex;
      gap: 20px;
      margin: 0;
    }

    .nav a {
      text-decoration: none;
      color: #333;
      font-weight: 500;
    }

    .nav a:hover {
      color: #1a73e8;
    }

    .hero {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      padding: 60px 40px;
      background-color: #e9f2ff;
    }

    .hero-content {
      flex: 1;
      max-width: 600px;
    }

    .hero-content h1 {
      font-size: 2.5rem;
      margin-bottom: 20px;
      color: #1a73e8;
    }

    .hero-content p {
      font-size: 1.1rem;
      margin-bottom: 30px;
    }

    .cta-button {
      background-color: #1a73e8;
      color: #fff;
      padding: 12px 24px;
      text-decoration: none;
      border-radius: 4px;
      font-weight: bold;
    }

    .hero-image {
      flex: 1;
      text-align: center;
    }

    .hero-image img {
      max-width: 100%;
      height: auto;
    }

    .features {
      padding: 60px 40px;
      text-align: center;
      background-color: #fff;
    }

    .features h2 {
      font-size: 2rem;
      margin-bottom: 40px;
    }

    .feature-grid {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-around;
      gap: 40px;
    }

    .feature {
      max-width: 250px;
    }

    .feature img {
      width: 60px;
      margin-bottom: 20px;
    }

    .feature h3 {
      font-size: 1.2rem;
      margin-bottom: 10px;
    }

    .footer {
      text-align: center;
      padding: 20px;
      background-color: #f1f1f1;
      font-size: 0.9rem;
    }
  </style>
</head>
<body>
  <header class="header">
    <div class="logo">Le Teleco</div>
    <nav class="nav">
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Plans</a></li>
        <li><a href="#">Support</a></li>
        <li><a href="#">About Us</a></li>
        <li><a href="#">Login</a></li>
      </ul>
    </nav>
  </header>

  <section class="hero">
    <div class="hero-content">
      <h1>Fast. Reliable. Simple.</h1>
      <p>Le Teleco brings you high-speed home broadband with zero hassle. Stay connected, stream without buffering, and work from home with confidence.</p>
      <a href="#" class="cta-button">View Plans</a>
    </div>
    <div class="hero-image">
      <img src="images/home-broadband.jpg" alt="People enjoying fast broadband" />
    </div>
  </section>

  <section class="features">
    <h2>Why Choose Le Teleco?</h2>
    <div class="feature-grid">
      <div class="feature">
        <img src="images/speed-icon.png" alt="Speed icon" />
        <h3>Superfast Speeds</h3>
        <p>Enjoy up to 1Gbps download speeds across all our residential plans.</p>
      </div>
      <div class="feature">
        <img src="images/support-icon.png" alt="Support icon" />
        <h3>24/7 Support</h3>
        <p>Our team is here day and night to help you with anything you need.</p>
      </div>
      <div class="feature">
        <img src="images/router-icon.png" alt="Router icon" />
        <h3>Easy Setup</h3>
        <p>Plug-and-play routers make installation quick and effortless.</p>
      </div>
    </div>
  </section>

  <footer class="footer">
    <p>&copy; 2025 Le Teleco. All rights reserved.</p>
  </footer>

  <!-- Five9 Web Chat Initialisation -->
  <script>
    F9.Chat.Wrapper.init({
      cdn: 'prod-uk',
      useBusinessHours: false,
      languages: {
        "enabled": false,
        "backgroundColor": "#65758e"
      },
      l10n: {
        "en": {
          "messenger": {
            "customText": {}
          },
          "systemMessages": {
            "transferredToParticipant": "The chat has been transferred to {name}.",
            "transferredToGroup": "That chat has been transferred to group {group}."
          },
          "captureFields": [
            { "k": "name", "l": "Name", "p": "Enter your name..." },
            { "k": "email", "l": "Email Address", "p": "Enter your email..." },
            { "k": "Question", "l": "Question", "p": "What can we help you with today?" }
          ]
        }
      },
      prepopulatedFields: [
        { "k": "campaign", "v": "Show me WebChat" }
      ],
      messenger: {
        integrationId: "156d6683-1e30-4846-89e3-080d78c5ae63",
        soundNotificationEnabled: true,
        transcriptPrintingEnabled: false,
        menuItems: {
          imageUpload: true,
          fileUpload: true,
          shareLocation: true
        },
        embedded: false,
        setViewportScale: false,
        browserStorage: "sessionStorage",
        browserLogLevel: {
          info: true,
          debug: true,
          error: true
        },
        hideWidgetAfterBusinessHours: false,
        openLinkInSameTab: false,
        scheduleCallback: {
          isCallbackEnabled: false,
          requestCallbackList: "",
          customConfirmationMessage: "We will call you as soon as we can at [PHONE]",
          web2CampaignAPIHost: ""
        },
        fixedHeader: false,
        displayStyle: "button",
        customColors: {
          brandColor: "65758e",
          conversationColor: "4B5DFF",
          actionColor: "4B5DFF"
        },
        carouselType: "default"
      },
      clearMessagesTimeout: 3
    });
  </script>
</body>
</html>
