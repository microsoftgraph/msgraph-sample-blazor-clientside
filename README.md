---
page_type: sample
description: This sample demonstrates how to use the Microsoft Graph .NET SDK to access data in Office 365 from Blazor WebAssembly apps.
products:
- ms-graph
- microsoft-graph-mail-api
- microsoft-graph-change-notifications-api
- office-exchange-online
- blazor
languages:
- csharp
---

# Microsoft Graph sample Blazor WebAssembly app

This sample demonstrates how to use the Microsoft Graph .NET SDK to access data in Office 365 from Blazor WebAssembly apps.

> **NOTE:** This sample was originally built from a tutorial published on the [Microsoft Graph tutorials](https://docs.microsoft.com/graph/tutorials) page. That tutorial has been removed.

## Prerequisites

- [.NET Core SDK](https://dotnet.microsoft.com/download)

## Register an app in Azure AD

1. Open a browser and navigate to the [Azure Active Directory admin center](https://aad.portal.azure.com). Login using a **personal account** (aka: Microsoft Account) or **Work or School Account**.

1. Select **Azure Active Directory** in the left-hand navigation, then select **App registrations** under **Manage**.

1. Select **New registration**. On the **Register an application** page, set the values as follows.

    - Set **Name** to `Blazor Graph Sample`.
    - Set **Supported account types** to **Accounts in any organizational directory and personal Microsoft accounts**.
    - Under **Redirect URI**, set the first drop-down to **Single-page application (SPA)** and set the value to `https://localhost:7067/authentication/login-callback`.

1. Select **Register**. On the **Blazor Graph Tutorial** page, copy the value of the **Application (client) ID** and save it, you will need it in the next step.

## Configure the sample

1. Create a new file in the **./GraphSample/wwwroot** directory named **appsettings.Development.json** and add the following code.

    ```json
    {
      "AzureAd": {
        "ClientId": "YOUR_CLIENT_ID_HERE"
      }
    }
    ```

1. Replace `YOUR_CLIENT_ID_HERE` with the **Application (client) ID** value from your app registration.

## Running the sample

Run the following command in the **GraphSample** directory.

```dotnetcli
dotnet run
```

Open your browser to `https://localhost:7067`.

## Code of conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Disclaimer

**THIS CODE IS PROVIDED _AS IS_ WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**
