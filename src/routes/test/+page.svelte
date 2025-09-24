<script>
  // Clean Svelte component - no external API calls
</script>

<svelte:head>
  <title>Auth0 Documentation</title>
  <meta name="description" content="Authentication Module Documentation" />
</svelte:head>

<div class="container">
  <header>
    <h1>Auth0</h1>
    <p class="subtitle">Authentication Module</p>
  </header>

  <main class="content">
    <section class="overview">
      <h2>Overview</h2>
      <p>
        Auth0 is a flexible, drop-in solution to add authentication and authorization services to your applications. 
        It provides a universal authentication & authorization platform for web, mobile and legacy applications.
      </p>
    </section>

    <section class="features">
      <h2>Key Features</h2>
      <ul>
        <li>Single Sign-On (SSO)</li>
        <li>Multi-factor Authentication (MFA)</li>
        <li>Social Login Integration</li>
        <li>Enterprise Identity Providers</li>
        <li>User Management</li>
        <li>Anomaly Detection</li>
      </ul>
    </section>

    <section class="configuration">
      <h2>Configuration</h2>
      <p>
        To configure Auth0 for your application, you'll need to set up your Auth0 domain, 
        client ID, and client secret in your application settings.
      </p>
      
      <div class="code-block">
        <h3>Example Configuration</h3>
        <pre><code>{`{
  "domain": "your-domain.auth0.com",
  "clientId": "your-client-id",
  "clientSecret": "your-client-secret",
  "redirectUri": "http://localhost:3000/callback"
}`}</code></pre>
      </div>
    </section>

    <section class="getting-started">
      <h2>Getting Started</h2>
      <ol>
        <li>Create an Auth0 account</li>
        <li>Set up your application in the Auth0 dashboard</li>
        <li>Configure your callback URLs</li>
        <li>Install the Auth0 SDK for your platform</li>
        <li>Implement authentication in your application</li>
      </ol>
    </section>
  </main>
</div>

<style>
  .container {
    max-width: 800px;
    margin: 0 auto;
    padding: 2rem;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    line-height: 1.6;
    color: #333;
  }

  header {
    text-align: center;
    margin-bottom: 3rem;
    padding-bottom: 2rem;
    border-bottom: 2px solid #e0e0e0;
  }

  h1 {
    font-size: 3rem;
    font-weight: 700;
    color: #1976d2;
    margin: 0;
  }

  .subtitle {
    font-size: 1.2rem;
    color: #666;
    margin: 0.5rem 0 0 0;
  }

  .content {
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }

  section {
    background: #f8f9fa;
    padding: 2rem;
    border-radius: 8px;
    border-left: 4px solid #1976d2;
  }

  h2 {
    color: #1976d2;
    font-size: 1.8rem;
    margin-top: 0;
    margin-bottom: 1rem;
  }

  h3 {
    color: #333;
    font-size: 1.3rem;
    margin-bottom: 1rem;
  }

  p {
    margin-bottom: 1rem;
  }

  ul, ol {
    padding-left: 1.5rem;
  }

  li {
    margin-bottom: 0.5rem;
  }

  .code-block {
    background: #2d3748;
    color: #e2e8f0;
    padding: 1.5rem;
    border-radius: 6px;
    margin-top: 1rem;
  }

  .code-block h3 {
    color: #e2e8f0;
    margin-top: 0;
    margin-bottom: 1rem;
  }

  pre {
    margin: 0;
    overflow-x: auto;
  }

  code {
    font-family: 'Monaco', 'Menlo', 'Ubuntu Mono', monospace;
    font-size: 0.9rem;
  }

  @media (max-width: 768px) {
    .container {
      padding: 1rem;
    }
    
    h1 {
      font-size: 2.5rem;
    }
    
    section {
      padding: 1.5rem;
    }
  }
</style>

