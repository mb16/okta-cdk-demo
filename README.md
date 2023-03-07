

    new okta.appOauth.AppOauth(this, "MichaelApp", {
      label: "Michael App",
      type: "web",
      omitSecret: false,
      grantTypes: ["authorization_code"],
      responseTypes: ["code"],
      redirectUris: ["https://localhost:5001/signin-oidc"]
    })

    new okta.group.Group(this, "michaels_group", {
      description: "Group to verify CDK",
      name: "Michael's Group",
    });