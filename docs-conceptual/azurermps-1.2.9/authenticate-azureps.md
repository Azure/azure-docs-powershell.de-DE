---
title: Anmelden mit Azure PowerShell
description: Anmelden mit Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 71a2554052f5a25ea86fe44b6dcf5d9343c81f3e
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399194"
---
# <a name="log-in-with-azure-powershell"></a><span data-ttu-id="a9317-103">Anmelden mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a9317-103">Log in with Azure PowerShell</span></span>

<span data-ttu-id="a9317-104">Azure PowerShell unterstützt mehrere Anmeldemethoden.</span><span class="sxs-lookup"><span data-stu-id="a9317-104">Azure PowerShell supports multiple login methods.</span></span> <span data-ttu-id="a9317-105">Die einfachste Möglichkeit ist die interaktive Anmeldung über die Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="a9317-105">The simplest way to get started is to log in interactively at the command line.</span></span>

## <a name="interactive-log-in"></a><span data-ttu-id="a9317-106">Interaktive Anmeldung</span><span class="sxs-lookup"><span data-stu-id="a9317-106">Interactive log in</span></span>

1. <span data-ttu-id="a9317-107">Geben Sie `Login-AzureRmAccount`ein.</span><span class="sxs-lookup"><span data-stu-id="a9317-107">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="a9317-108">Im daraufhin erscheinenden Dialogfeld werden Sie zur Eingabe Ihrer Azure-Anmeldeinformationen aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="a9317-108">You will get dialog box asking for your Azure credentials.</span></span>

2. <span data-ttu-id="a9317-109">Geben Sie die dem Konto zugeordnete E-Mail-Adresse und das zugehörige Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="a9317-109">Type the email address and password associated with your account.</span></span> <span data-ttu-id="a9317-110">Die Anmeldeinformationen werden von Azure authentifiziert und gespeichert, dann wird das Fenster geschlossen.</span><span class="sxs-lookup"><span data-stu-id="a9317-110">Azure authenticates and saves the credential information, and then closes the window.</span></span>

## <a name="log-in-with-a-service-principal"></a><span data-ttu-id="a9317-111">Anmeldung mit einem Dienstprinzipal</span><span class="sxs-lookup"><span data-stu-id="a9317-111">Log in with a service principal</span></span>

<span data-ttu-id="a9317-112">Dienstprinzipale ermöglichen die Erstellung nicht interaktiver Konten für die Ressourcenbearbeitung.</span><span class="sxs-lookup"><span data-stu-id="a9317-112">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="a9317-113">Dienstprinzipale sind vergleichbar mit Benutzerkonten, auf die Sie mithilfe von Azure Active Directory Regeln anwenden können.</span><span class="sxs-lookup"><span data-stu-id="a9317-113">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="a9317-114">Indem Sie einem Dienstprinzipal nur die erforderlichen Mindestberechtigungen erteilen, können Sie Ihre Automatisierungsskripts noch sicherer machen.</span><span class="sxs-lookup"><span data-stu-id="a9317-114">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

1. <span data-ttu-id="a9317-115">Falls Sie noch nicht über einen Dienstprinzipal verfügen, [erstellen Sie einen](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="a9317-115">If you don't already have a service principal, [create one](create-azure-service-principal-azureps.md).</span></span>

2. <span data-ttu-id="a9317-116">Melden Sie sich mit dem Dienstprinzipal an.</span><span class="sxs-lookup"><span data-stu-id="a9317-116">Log in with the service principal.</span></span>

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    <span data-ttu-id="a9317-117">Wenn Sie Ihre Mandanten-ID ermitteln möchten, melden Sie sich interaktiv an, und rufen Sie anschließend die Mandanten-ID aus Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="a9317-117">To get your TenantId, log in interactively and then get the TenantId from your subscription.</span></span>

    ```powershell
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-managed-identities-for-azure-resources"></a><span data-ttu-id="a9317-118">Anmelden mit verwalteten Identitäten für Azure-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a9317-118">Log in using managed identities for Azure resources</span></span>

<span data-ttu-id="a9317-119">Verwaltete Identitäten für Azure-Ressourcen ist eine Funktion von Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a9317-119">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="a9317-120">Sie können den Dienstprinzipal einer verwalteten Identität für die Anmeldung verwenden und ein App-exklusives Zugriffstoken für den Zugriff auf andere Ressourcen beziehen.</span><span class="sxs-lookup"><span data-stu-id="a9317-120">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span>

<span data-ttu-id="a9317-121">Weitere Informationen zu verwalteten Identitäten für Azure-Ressourcen finden Sie unter [Verwenden von verwalteten Identitäten für Azure-Ressourcen auf einem virtuellen Azure-Computer zum Abrufen eines Zugriffstokens](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="a9317-121">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="log-in-to-another-cloud"></a><span data-ttu-id="a9317-122">Anmelden bei einer anderen Cloud</span><span class="sxs-lookup"><span data-stu-id="a9317-122">Log in to another Cloud</span></span>

<span data-ttu-id="a9317-123">Azure-Clouddienste bieten unterschiedliche Umgebungen, die den Datenverarbeitungsvorschriften verschiedener Staaten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a9317-123">Azure cloud services provide different environments that adhere to the data-handling regulations of various governments.</span></span> <span data-ttu-id="a9317-124">Wenn Ihr Azure-Konto in einer dieser staatsspezifischen Clouds enthalten ist, müssen Sie die Umgebung angeben, wenn Sie sich anmelden.</span><span class="sxs-lookup"><span data-stu-id="a9317-124">If your Azure account is in one the government clouds, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="a9317-125">Wenn Ihr Konto beispielsweise in der Cloud für China enthalten ist, melden Sie sich mit dem folgenden Befehl an:</span><span class="sxs-lookup"><span data-stu-id="a9317-125">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

<span data-ttu-id="a9317-126">Verwenden Sie den folgenden Befehl, um eine Liste der verfügbaren Umgebungen zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="a9317-126">Use the following command to get a list of available environments:</span></span>

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```output
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="a9317-127">Weitere Informationen zum Verwalten des rollenbasierten Zugriffs in Azure</span><span class="sxs-lookup"><span data-stu-id="a9317-127">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="a9317-128">Weitere Informationen zur Authentifizierung und Abonnementverwaltung in Azure finden Sie unter [Verwalten von Konten, Abonnements und Administratorrollen](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="a9317-128">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="a9317-129">Azure PowerShell-Cmdlets für die Rollenverwaltung</span><span class="sxs-lookup"><span data-stu-id="a9317-129">Azure PowerShell cmdlets for role management</span></span>

* [<span data-ttu-id="a9317-130">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a9317-130">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="a9317-131">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a9317-131">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="a9317-132">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a9317-132">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="a9317-133">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a9317-133">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="a9317-134">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a9317-134">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="a9317-135">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a9317-135">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="a9317-136">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a9317-136">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
