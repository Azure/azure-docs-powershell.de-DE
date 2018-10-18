---
title: Anmelden mit Azure PowerShell
description: Es wird beschrieben, wie Sie sich mit Azure PowerShell als Benutzer, per Dienstprinzipal oder mit verwalteten Identitäten für Azure-Ressourcen anmelden.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 530eafcd0d14dbfd790a22d80c5922f304f4e0b2
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2018
ms.locfileid: "49398854"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="f01c7-103">Anmelden mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f01c7-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="f01c7-104">Azure PowerShell unterstützt mehrere Authentifizierungsmethoden.</span><span class="sxs-lookup"><span data-stu-id="f01c7-104">Azure PowerShell supports multiple authentication methods.</span></span> <span data-ttu-id="f01c7-105">Die einfachste Möglichkeit ist die interaktive Anmeldung über die Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="f01c7-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="f01c7-106">Interaktives Anmelden</span><span class="sxs-lookup"><span data-stu-id="f01c7-106">Sign in interactively</span></span>

<span data-ttu-id="f01c7-107">Verwenden Sie für die interaktive Anmeldung das Cmdlet [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).</span><span class="sxs-lookup"><span data-stu-id="f01c7-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="f01c7-108">Wenn Sie dieses Cmdlet ausführen, wird ein Dialogfeld angezeigt, in dem Sie zur Eingabe Ihrer E-Mail-Adresse und Ihres Kennworts für Ihr Azure-Konto aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f01c7-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="f01c7-109">Wenn Sie sich authentifizieren, werden diese Angaben für die aktuelle PowerShell-Sitzung gespeichert, das Dialogfeld wird geschlossen, und Sie haben Zugriff auf alle Azure PowerShell-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="f01c7-109">When you authenticate, that information is saved for the current PowerShell session, the dialog is closed, and you have access to all of the Azure PowerShell cmdlets.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f01c7-110">Diese Anmeldung gilt _nur_ für die aktuelle PowerShell-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f01c7-110">This sign in is for the current PowerShell session _only_.</span></span> <span data-ttu-id="f01c7-111">Informationen zur sitzungsübergreifenden Speicherung der Authentifizierung finden Sie im Artikel zu [beständigen Anmeldeinformationen](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="f01c7-111">To persist authentication across multiple sessions, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="f01c7-112">Anmelden mit einem Dienstprinzipal</span><span class="sxs-lookup"><span data-stu-id="f01c7-112">Sign in with a service principal</span></span>

<span data-ttu-id="f01c7-113">Dienstprinzipale ermöglichen die Erstellung nicht interaktiver Konten für die Ressourcenbearbeitung.</span><span class="sxs-lookup"><span data-stu-id="f01c7-113">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="f01c7-114">Dienstprinzipale sind vergleichbar mit Benutzerkonten, auf die Sie mithilfe von Azure Active Directory Regeln anwenden können.</span><span class="sxs-lookup"><span data-stu-id="f01c7-114">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="f01c7-115">Indem Sie einem Dienstprinzipal nur die erforderlichen Mindestberechtigungen erteilen, können Sie Ihre Automatisierungsskripts noch sicherer machen.</span><span class="sxs-lookup"><span data-stu-id="f01c7-115">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="f01c7-116">Informationen zur Erstellung eines Dienstprinzipals für die Verwendung mit PowerShell finden Sie unter [Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="f01c7-116">If you need to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="f01c7-117">Verwenden Sie für die Anmeldung mit einem Dienstprinzipal das Cmdlet `Connect-AzureRmAccount` mit dem Argument `-ServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="f01c7-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="f01c7-118">Sie benötigen auch die Anwendungs-ID und die Anmeldeinformationen des Dienstprinzipals sowie die dem Dienstprinzipal zugeordnete Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="f01c7-118">You will also need the service princpal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="f01c7-119">Verwenden Sie das Cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential), um die Anmeldeinformationen des Dienstprinzipals als entsprechendes Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f01c7-119">In order to get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="f01c7-120">Dieses Cmdlet zeigt ein Dialogfeld für die Eingabe der Benutzer-ID und des Kennworts des Dienstprinzipals an.</span><span class="sxs-lookup"><span data-stu-id="f01c7-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-managed-identities-for-azure-resources"></a><span data-ttu-id="f01c7-121">Anmelden mit verwalteten Identitäten für Azure-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f01c7-121">Sign in using managed identities for Azure resources</span></span>

<span data-ttu-id="f01c7-122">Verwaltete Identitäten für Azure-Ressourcen ist eine Funktion von Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f01c7-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="f01c7-123">Sie können den Dienstprinzipal einer verwalteten Identität für die Anmeldung verwenden und ein App-exklusives Zugriffstoken für den Zugriff auf andere Ressourcen beziehen.</span><span class="sxs-lookup"><span data-stu-id="f01c7-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="f01c7-124">Verwaltete Identitäten stehen nur für virtuelle Computer zur Verfügung, die in einer Azure-Cloud ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f01c7-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="f01c7-125">Weitere Informationen zu verwalteten Identitäten für Azure-Ressourcen finden Sie unter [Verwenden von verwalteten Identitäten für Azure-Ressourcen auf einem virtuellen Azure-Computer zum Abrufen eines Zugriffstokens](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="f01c7-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="f01c7-126">Anmelden bei einer anderen Cloud</span><span class="sxs-lookup"><span data-stu-id="f01c7-126">Sign in to another Cloud</span></span>

<span data-ttu-id="f01c7-127">Azure-Clouddienste bieten unterschiedliche Umgebungen, die den Datenverarbeitungsvorschriften verschiedener Regionen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f01c7-127">Azure cloud services provide different environments that adhere to the data-handling regulations of various regions.</span></span> <span data-ttu-id="f01c7-128">Wenn sich Ihr Azure-Konto in einer Cloud befindet, die einer dieser Regionen zugeordnet ist, müssen Sie bei der Anmeldung die Umgebung angeben.</span><span class="sxs-lookup"><span data-stu-id="f01c7-128">If your Azure account is in a cloud associated with one of these regions, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="f01c7-129">Wenn Ihr Konto beispielsweise in der Cloud für China enthalten ist, melden Sie sich mit dem folgenden Befehl an:</span><span class="sxs-lookup"><span data-stu-id="f01c7-129">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="f01c7-130">Verwenden Sie den folgenden Befehl, um eine Liste der verfügbaren Umgebungen zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="f01c7-130">Use the following command to get a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="f01c7-131">Weitere Informationen zum Verwalten des rollenbasierten Zugriffs in Azure</span><span class="sxs-lookup"><span data-stu-id="f01c7-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="f01c7-132">Weitere Informationen zur Authentifizierung und Abonnementverwaltung in Azure finden Sie unter [Verwalten von Konten, Abonnements und Administratorrollen](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="f01c7-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="f01c7-133">Azure PowerShell-Cmdlets für die Rollenverwaltung:</span><span class="sxs-lookup"><span data-stu-id="f01c7-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="f01c7-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f01c7-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="f01c7-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f01c7-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="f01c7-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f01c7-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="f01c7-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f01c7-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="f01c7-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f01c7-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="f01c7-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f01c7-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="f01c7-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f01c7-140">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
