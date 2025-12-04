# Claimlog Client

A simple embedding of a claim log into a Web page.

## Build

```bash
npm install
npm run build
```

## Embed

Include the claims in your website use this HTML fragment:

```(html)
<html>
<head>
        <title>My Claims</title>

        <link rel='eventlog' href='https://mycontributions.info/service/c/trace?artifact=https://research.test.edu.nl/@alsvanounds'/>
        <script defer src='https://mycontributions.info/apps/claimlog.js'></script>

        <style>
        html, body {
            margin: 0;
            padding: 0;
            font-family: "Inter", sans-serif;
            font-size: 16px;
        }
        </style>
</head>
<body>
        <h1>Fetze Alsvanouds Claims</h1>
        <div id="claims"></div>
</body>
</html>
```

where the **link** HTML header points to your claim log.

See an example here: https://labs.eventnotifications.net/claims/index.html