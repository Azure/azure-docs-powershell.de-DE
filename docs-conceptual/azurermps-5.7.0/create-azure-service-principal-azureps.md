---
title: Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell
description: Hier erfahren Sie, wie Sie mit Azure PowerShell einen Dienstprinzipal für Ihre App oder Ihren Dienst erstellen.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: dd2528cf91495361343ff562b7a602e7c115d13b
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534689"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="07f50-104">Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="07f50-104">Create an Azure service principal with Azure PowerShell</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="07f50-105">Wenn Sie Ihre App oder Ihren Dienst mit Azure PowerShell verwalten möchten, sollten Sie sie bzw. ihn nicht unter Ihren eigenen Anmeldeinformationen, sondern unter einem AAD-Dienstprinzipal (Azure Active Directory) ausführen.</span><span class="sxs-lookup"><span data-stu-id="07f50-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="07f50-106">In diesem Thema wird Schritt für Schritt erläutert, wie Sie einen Sicherheitsprinzipal mit Azure PowerShell erstellen.</span><span class="sxs-lookup"><span data-stu-id="07f50-106">This topic steps you through creating a security principal with Azure PowerShell.</span></span>

> [!NOTE]
> <span data-ttu-id="07f50-107">Dienstprinzipale können auch über das Azure-Portal erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="07f50-107">You can also create a service principal through the Azure portal.</span></span> <span data-ttu-id="07f50-108">Ausführlichere Informationen finden Sie unter [Erstellen einer Active Directory-Anwendung und eines Dienstprinzipals mit Ressourcenzugriff mithilfe des Portals](/azure/azure-resource-manager/resource-group-create-service-principal-portal).</span><span class="sxs-lookup"><span data-stu-id="07f50-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="07f50-109">Was ist ein Dienstprinzipal?</span><span class="sxs-lookup"><span data-stu-id="07f50-109">What is a 'service principal'?</span></span>

<span data-ttu-id="07f50-110">Ein Azure-Dienstprinzipal ist eine Sicherheitsidentität, die durch von Benutzern erstellte Apps, Dienste und Automatisierungstools verwendet wird, um auf bestimmte Azure-Ressourcen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="07f50-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="07f50-111">Das Konzept lässt sich als Benutzeridentität (Benutzername und Kennwort oder Zertifikat) mit einer bestimmten Rolle und streng kontrollierten Berechtigungen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="07f50-111">Think of it as a 'user identity' (username and password or certificate) with a specific role, and tightly controlled permissions.</span></span> <span data-ttu-id="07f50-112">Im Gegensatz zu einer allgemeinen Benutzeridentität muss diese Identität nur ganz bestimmte Aktionen ausführen können.</span><span class="sxs-lookup"><span data-stu-id="07f50-112">It only needs to be able to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="07f50-113">Wenn Sie ihr nur die Berechtigungen gewähren, die sie zum Ausführen ihrer Verwaltungsaufgaben benötigt, verbessert das die Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="07f50-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="07f50-114">Überprüfen der eigenen Berechtigungsstufe</span><span class="sxs-lookup"><span data-stu-id="07f50-114">Verify your own permission level</span></span>

<span data-ttu-id="07f50-115">Zunächst einmal müssen Sie sowohl in der Azure Active Directory-Instanz als auch im Azure-Abonnement über ausreichende Berechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="07f50-115">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="07f50-116">Sie müssen insbesondere eine App in der Active Directory-Instanz erstellen und dem Dienstprinzipal eine Rolle zuweisen können.</span><span class="sxs-lookup"><span data-stu-id="07f50-116">Specifically, you must be able to create an app in the Active Directory, and assign a role to the service principal.</span></span>

<span data-ttu-id="07f50-117">Die einfachste Möglichkeit zum Überprüfen, ob Ihr Konto über die erforderlichen Berechtigungen verfügt, ist über das Portal.</span><span class="sxs-lookup"><span data-stu-id="07f50-117">The easiest way to check whether your account has adequate permissions is through the portal.</span></span> <span data-ttu-id="07f50-118">Siehe [Überprüfen der erforderlichen Berechtigung im Portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="07f50-118">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="07f50-119">Erstellen eines Dienstprinzipals für Ihre App</span><span class="sxs-lookup"><span data-stu-id="07f50-119">Create a service principal for your app</span></span>

<span data-ttu-id="07f50-120">Nachdem Sie sich bei Ihrem Azure-Konto angemeldet haben, können Sie den Dienstprinzipal erstellen.</span><span class="sxs-lookup"><span data-stu-id="07f50-120">Once you are signed into your Azure account, you can create the service principal.</span></span> <span data-ttu-id="07f50-121">Ihre bereitgestellte App muss auf eine der folgenden Arten identifiziert werden:</span><span class="sxs-lookup"><span data-stu-id="07f50-121">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="07f50-122">Mithilfe des eindeutigen Namens Ihrer bereitgestellten App („MyDemoWebApp“ in den folgenden Beispielen). Oder:</span><span class="sxs-lookup"><span data-stu-id="07f50-122">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples, or</span></span>
* <span data-ttu-id="07f50-123">Mithilfe der Anwendungs-ID (GUID, die Ihrer bereitgestellten App, Ihrem bereitgestellten Dienst oder Ihrem bereitgestellten Objekt zugeordnet ist)</span><span class="sxs-lookup"><span data-stu-id="07f50-123">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="07f50-124">Abrufen von Informationen zu Ihrer Anwendung</span><span class="sxs-lookup"><span data-stu-id="07f50-124">Get information about your application</span></span>

<span data-ttu-id="07f50-125">Mit dem Cmdlet `Get-AzureRmADApplication` können Sie Informationen zu Ihrer Anwendung ermitteln.</span><span class="sxs-lookup"><span data-stu-id="07f50-125">The `Get-AzureRmADApplication` cmdlet can be used to discover information about your application.</span></span>

```azurepowershell-interactive
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="07f50-126">Erstellen eines Dienstprinzipals für Ihre Anwendung</span><span class="sxs-lookup"><span data-stu-id="07f50-126">Create a service principal for your application</span></span>

<span data-ttu-id="07f50-127">Das Cmdlet `New-AzureRmADServicePrincipal` dient zum Erstellen des Dienstprinzipals.</span><span class="sxs-lookup"><span data-stu-id="07f50-127">The `New-AzureRmADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
$securePassword = ConvertTo-SecureString -Force -AsPlainText -String $password
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $securePassword
```

```output
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="07f50-128">Abrufen von Informationen zum Dienstprinzipal</span><span class="sxs-lookup"><span data-stu-id="07f50-128">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="07f50-129">Anmelden mithilfe des Dienstprinzipals</span><span class="sxs-lookup"><span data-stu-id="07f50-129">Sign in using the service principal</span></span>

<span data-ttu-id="07f50-130">Nun können Sie sich als der neue Dienstprinzipal für die App anmelden. Verwenden Sie dabei die Werte für *appId* und *password*, die Sie angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="07f50-130">You can now sign in as the new service principal for your app using the *appId* and *password* you provided.</span></span> <span data-ttu-id="07f50-131">Geben Sie die Mandanten-ID für Ihr Konto an.</span><span class="sxs-lookup"><span data-stu-id="07f50-131">You need to supply the Tenant Id for your account.</span></span> <span data-ttu-id="07f50-132">Ihre Mandanten-ID wird angezeigt, wenn Sie sich mit Ihren persönlichen Anmeldeinformationen bei Azure anmelden.</span><span class="sxs-lookup"><span data-stu-id="07f50-132">Your Tenant Id is displayed when you sign into Azure with your personal credentials.</span></span>

```azurepowershell-interactive
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Connect-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="07f50-133">Führen Sie diesen Befehl in einer neuen PowerShell-Sitzung aus.</span><span class="sxs-lookup"><span data-stu-id="07f50-133">Run this command from a new PowerShell session.</span></span> <span data-ttu-id="07f50-134">Nach erfolgreicher Anmeldung wird eine Ausgabe wie die folgende angezeigt:</span><span class="sxs-lookup"><span data-stu-id="07f50-134">After a successfully signing on you see output something like this:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="07f50-135">Glückwunsch!</span><span class="sxs-lookup"><span data-stu-id="07f50-135">Congratulations!</span></span> <span data-ttu-id="07f50-136">Die Anmeldeinformationen können zum Ausführen Ihrer App verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07f50-136">You can use these credentials to run your app.</span></span> <span data-ttu-id="07f50-137">Als Nächstes müssen Sie die Berechtigungen des Dienstprinzipals anpassen.</span><span class="sxs-lookup"><span data-stu-id="07f50-137">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="07f50-138">Verwalten von Rollen</span><span class="sxs-lookup"><span data-stu-id="07f50-138">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="07f50-139">Bei der rollenbasierten Zugriffssteuerung (Role-Based Access Control, RBAC) in Azure handelt es sich um ein Modell zum Definieren und Verwalten von Rollen für Benutzer- und Dienstprinzipale.</span><span class="sxs-lookup"><span data-stu-id="07f50-139">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="07f50-140">Rollen sind bestimmte Berechtigungen zugeordnet, die bestimmen, welche Ressourcen ein Prinzipal lesen, aufrufen, schreiben oder verwalten kann.</span><span class="sxs-lookup"><span data-stu-id="07f50-140">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="07f50-141">Weitere Informationen zu RBAC und Rollen finden Sie unter [Integrierte Rollen für die rollenbasierte Zugriffssteuerung in Azure](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="07f50-141">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="07f50-142">Für die Verwaltung von Rollenzuweisungen stehen in Azure PowerShell folgende Cmdlets zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="07f50-142">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="07f50-143">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="07f50-143">Get-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [<span data-ttu-id="07f50-144">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="07f50-144">New-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [<span data-ttu-id="07f50-145">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="07f50-145">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/remove-azurermroleassignment)

<span data-ttu-id="07f50-146">Standardmäßig hat ein Dienstprinzipal die Rolle **Mitwirkender**.</span><span class="sxs-lookup"><span data-stu-id="07f50-146">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="07f50-147">Je nachdem, in welchem Maß Ihrer App mit Azure Services interagiert, ist das unter Umständen nicht die beste Wahl, da diese Rolle über umfassende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="07f50-147">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="07f50-148">Die Rolle **Leser** ist stärker eingeschränkt und bietet sich für Apps ohne Schreibzugriff an.</span><span class="sxs-lookup"><span data-stu-id="07f50-148">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="07f50-149">Über das Azure-Portal können Sie Details zu rollenspezifischen Berechtigungen anzeigen oder benutzerdefinierte Berechtigungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="07f50-149">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="07f50-150">Im folgenden Beispiel fügen wir unserem vorherigen Beispiel die Rolle **Leser** hinzu und löschen die Rolle **Mitwirkender**:</span><span class="sxs-lookup"><span data-stu-id="07f50-150">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="07f50-151">So zeigen Sie die derzeit zugewiesenen Rollen an:</span><span class="sxs-lookup"><span data-stu-id="07f50-151">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

<span data-ttu-id="07f50-152">Weitere Azure PowerShell-Cmdlets für die Rollenverwaltung:</span><span class="sxs-lookup"><span data-stu-id="07f50-152">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="07f50-153">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="07f50-153">Get-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="07f50-154">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="07f50-154">New-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="07f50-155">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="07f50-155">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="07f50-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="07f50-156">Set-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="07f50-157">Ändern der Anmeldeinformationen des Sicherheitsprinzipals</span><span class="sxs-lookup"><span data-stu-id="07f50-157">Change the credentials of the security principal</span></span>

<span data-ttu-id="07f50-158">Aus Sicherheitsgründen empfiehlt es sich, regelmäßig die Berechtigungen zu überprüfen und das Kennwort zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="07f50-158">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="07f50-159">Darüber hinaus sollten Sie auch die Sicherheitsanmeldeinformationen verwalten und ändern, wenn sich Ihre App verändert.</span><span class="sxs-lookup"><span data-stu-id="07f50-159">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="07f50-160">Zum Ändern des Dienstprinzipalkennworts können wir beispielsweise ein neues Kennwort erstellen und das alte entfernen.</span><span class="sxs-lookup"><span data-stu-id="07f50-160">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="07f50-161">Hinzufügen eines neuen Kennworts für den Dienstprinzipal</span><span class="sxs-lookup"><span data-stu-id="07f50-161">Add a new password for the service principal</span></span>

```azurepowershell-interactive
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="07f50-162">Abrufen einer Liste mit Anmeldeinformationen für den Dienstprinzipal</span><span class="sxs-lookup"><span data-stu-id="07f50-162">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="07f50-163">Entfernen des alten Kennworts für den Dienstprinzipal</span><span class="sxs-lookup"><span data-stu-id="07f50-163">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="07f50-164">Überprüfen der Liste mit Anmeldeinformationen für den Dienstprinzipal</span><span class="sxs-lookup"><span data-stu-id="07f50-164">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
