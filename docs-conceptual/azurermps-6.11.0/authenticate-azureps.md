---
title: Anmelden mit Azure PowerShell
description: Es wird beschrieben, wie Sie sich mit Azure PowerShell als Benutzer, per Dienstprinzipal oder mit verwalteten Identitäten für Azure-Ressourcen anmelden.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: c19d9ade0f69f4af9f14c68ad22b327c27c8ccfd
ms.sourcegitcommit: 1f699b72bf544d92459da9d888cc0091f9415b65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "50972161"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="54100-103">Anmelden mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="54100-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="54100-104">Azure PowerShell unterstützt mehrere Authentifizierungsmethoden.</span><span class="sxs-lookup"><span data-stu-id="54100-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="54100-105">Die einfachste Möglichkeit ist die interaktive Anmeldung über die Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="54100-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="54100-106">Interaktives Anmelden</span><span class="sxs-lookup"><span data-stu-id="54100-106">Sign in interactively</span></span>

<span data-ttu-id="54100-107">Verwenden Sie für die interaktive Anmeldung das Cmdlet [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).</span><span class="sxs-lookup"><span data-stu-id="54100-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="54100-108">Wenn Sie dieses Cmdlet ausführen, wird ein Dialogfeld angezeigt, in dem Sie zur Eingabe Ihrer E-Mail-Adresse und Ihres Kennworts für Ihr Azure-Konto aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="54100-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="54100-109">Diese Authentifizierung gilt jeweils für die aktuelle PowerShell-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="54100-109">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="54100-110">Ab Azure PowerShell 6.3.0 werden Ihre Anmeldeinformationen in mehreren PowerShell-Sitzungen gemeinsam verwendet, solange Sie bei Windows angemeldet bleiben.</span><span class="sxs-lookup"><span data-stu-id="54100-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="54100-111">Weitere Informationen finden Sie im Artikel zu [beständigen Anmeldeinformationen](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="54100-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="54100-112">Anmelden mit einem Dienstprinzipal</span><span class="sxs-lookup"><span data-stu-id="54100-112">Sign in with a service principal</span></span>

<span data-ttu-id="54100-113">Dienstprinzipale sind nicht interaktive Azure-Konten.</span><span class="sxs-lookup"><span data-stu-id="54100-113">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="54100-114">Wie bei anderen Benutzerkonten auch, werden die Berechtigungen mit Azure Active Directory verwaltet.</span><span class="sxs-lookup"><span data-stu-id="54100-114">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="54100-115">Indem für einen Dienstprinzipal nur die benötigten Berechtigungen gewährt werden, bleibt die Sicherheit Ihrer Automatisierungsskripts gewahrt.</span><span class="sxs-lookup"><span data-stu-id="54100-115">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="54100-116">Informationen zur Erstellung eines Dienstprinzipals für die Verwendung mit PowerShell finden Sie unter [Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="54100-116">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="54100-117">Verwenden Sie für die Anmeldung mit einem Dienstprinzipal das Cmdlet `Connect-AzureRmAccount` mit dem Argument `-ServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="54100-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="54100-118">Sie benötigen auch die Anwendungs-ID und die Anmeldeinformationen des Dienstprinzipals sowie die dem Dienstprinzipal zugeordnete Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="54100-118">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="54100-119">Verwenden Sie das Cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential), um die Anmeldeinformationen des Dienstprinzipals als entsprechendes Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="54100-119">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="54100-120">Dieses Cmdlet zeigt ein Dialogfeld für die Eingabe der Benutzer-ID und des Kennworts des Dienstprinzipals an.</span><span class="sxs-lookup"><span data-stu-id="54100-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="54100-121">Anmelden mit einer verwalteten Azure-Dienstidentität</span><span class="sxs-lookup"><span data-stu-id="54100-121">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="54100-122">Verwaltete Identitäten für Azure-Ressourcen ist eine Funktion von Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="54100-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="54100-123">Sie können den Dienstprinzipal einer verwalteten Identität für die Anmeldung verwenden und ein App-exklusives Zugriffstoken für den Zugriff auf andere Ressourcen beziehen.</span><span class="sxs-lookup"><span data-stu-id="54100-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="54100-124">Verwaltete Identitäten stehen nur für virtuelle Computer zur Verfügung, die in einer Azure-Cloud ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="54100-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="54100-125">Weitere Informationen zu verwalteten Identitäten für Azure-Ressourcen finden Sie unter [Verwenden von verwalteten Identitäten für Azure-Ressourcen auf einem virtuellen Azure-Computer zum Abrufen eines Zugriffstokens](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="54100-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="54100-126">Anmelden als Cloud Solution Provider (CSP)</span><span class="sxs-lookup"><span data-stu-id="54100-126">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="54100-127">Eine Anmeldung als [(Cloud Solution Provider, CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) erfordert die Verwendung von `-TenantId`.</span><span class="sxs-lookup"><span data-stu-id="54100-127">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="54100-128">In der Regel kann dieser Parameter entweder als Mandanten-ID oder als Domänenname angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="54100-128">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="54100-129">Für die CSP-Anmeldung muss jedoch eine **Mandanten-ID** bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="54100-129">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="54100-130">Anmelden bei einer anderen Cloud</span><span class="sxs-lookup"><span data-stu-id="54100-130">Sign in to another Cloud</span></span>

<span data-ttu-id="54100-131">Azure-Clouddienste verfügen über Umgebungen, die jeweils mit den regionalen Bestimmungen zum Umgang mit Daten konform sind.</span><span class="sxs-lookup"><span data-stu-id="54100-131">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="54100-132">Legen Sie die Umgebung für Konten in einer regionalen Cloud fest, wenn Sie sich mit dem Argument `-Environment` anmelden.</span><span class="sxs-lookup"><span data-stu-id="54100-132">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="54100-133">Beispiel für den Fall, dass sich Ihr Konto in der Cloud in China befindet:</span><span class="sxs-lookup"><span data-stu-id="54100-133">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="54100-134">Mit dem folgenden Befehl wird eine Liste mit den verfügbaren Umgebungen abgerufen:</span><span class="sxs-lookup"><span data-stu-id="54100-134">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="54100-135">Weitere Informationen zum Verwalten des rollenbasierten Zugriffs in Azure</span><span class="sxs-lookup"><span data-stu-id="54100-135">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="54100-136">Weitere Informationen zur Authentifizierung und Abonnementverwaltung in Azure finden Sie unter [Verwalten von Konten, Abonnements und Administratorrollen](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="54100-136">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="54100-137">Azure PowerShell-Cmdlets für die Rollenverwaltung:</span><span class="sxs-lookup"><span data-stu-id="54100-137">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="54100-138">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="54100-138">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="54100-139">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="54100-139">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="54100-140">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="54100-140">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="54100-141">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="54100-141">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="54100-142">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="54100-142">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="54100-143">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="54100-143">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="54100-144">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="54100-144">Set-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
