---
title: Verwenden von Azure-Dienstprinzipalen mit Azure PowerShell
description: Hier erfahren Sie, wie Sie mit Azure PowerShell Dienstprinzipale erstellen und verwenden.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 196af9721ed8ab5141451159b12a8a1e5a5b1f3d
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251861"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="1c39a-103">Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1c39a-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="1c39a-104">Für automatisierte Tools, die Azure-Dienste verwenden, sollten stets eingeschränkte Berechtigungen festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="1c39a-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="1c39a-105">Azure bietet Dienstprinzipale, damit Anwendungen nicht als Benutzer mit uneingeschränkten Berechtigungen angemeldet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1c39a-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="1c39a-106">Ein Azure-Dienstprinzipal ist eine Identität, die zur Verwendung mit Anwendungen, gehosteten Diensten und automatisierten Tools für den Zugriff auf Azure-Ressourcen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1c39a-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="1c39a-107">Dieser Zugriff wird durch die dem Dienstprinzipal zugewiesenen Rollen eingeschränkt. Dadurch können Sie steuern, auf welcher Ebene auf welche Ressourcen zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="1c39a-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="1c39a-108">Aus Sicherheitsgründen wird stets empfohlen, Dienstprinzipale mit automatisierten Tools zu verwenden, statt ihnen die Anmeldung mit einer Benutzeridentität zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="1c39a-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="1c39a-109">In diesem Artikel wird Schritt für Schritt erläutert, wie Sie mit Azure PowerShell einen Dienstprinzipal erstellen, Informationen zu ihm abrufen und ihn zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="1c39a-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

> [!WARNING]
> <span data-ttu-id="1c39a-110">Wenn Sie mithilfe des Befehls [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) einen Dienstprinzipal erstellen, enthält die Ausgabe Anmeldeinformationen, die geschützt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1c39a-110">When you create a service principal using the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="1c39a-111">Verwenden Sie als Alternative ggf. [verwaltete Identitäten](/azure/active-directory/managed-identities-azure-resources/overview), um zu vermeiden, dass die Verwendung von Anmeldeinformationen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1c39a-111">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="1c39a-112">[New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) weist dem Dienstprinzipal standardmäßig auf Abonnementebene die Rolle [Mitwirkender](/azure/role-based-access-control/built-in-roles#contributor) zu.</span><span class="sxs-lookup"><span data-stu-id="1c39a-112">By default, [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="1c39a-113">Um das Risiko eines kompromittierten Dienstprinzipals zu verringern, weisen Sie eine spezifischere Rolle zu, und schränken Sie den Bereich auf eine Ressource oder Ressourcengruppe ein.</span><span class="sxs-lookup"><span data-stu-id="1c39a-113">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="1c39a-114">Weitere Informationen finden Sie unter [Schritte zum Hinzufügen einer Rollenzuweisung](/azure/role-based-access-control/role-assignments-steps).</span><span class="sxs-lookup"><span data-stu-id="1c39a-114">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="1c39a-115">Erstellen eines Dienstprinzipals</span><span class="sxs-lookup"><span data-stu-id="1c39a-115">Create a service principal</span></span>

<span data-ttu-id="1c39a-116">Erstellen Sie mit dem Cmdlet [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) einen Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="1c39a-116">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="1c39a-117">Beim Erstellen eines Dienstprinzipals wählen Sie den Typ der von ihm verwendeten Anmeldeauthentifizierung aus.</span><span class="sxs-lookup"><span data-stu-id="1c39a-117">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
> <span data-ttu-id="1c39a-118">Wenn Ihr Konto nicht über die Berechtigung zum Erstellen eines Dienstprinzipals verfügt, gibt `New-AzADServicePrincipal` eine Fehlermeldung mit dem Hinweis „Nicht genügend Berechtigungen zum Abschließen des Vorgangs“ zurück.</span><span class="sxs-lookup"><span data-stu-id="1c39a-118">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation".</span></span>
> <span data-ttu-id="1c39a-119">Bitten Sie den Azure Active Directory-Administrator, einen Dienstprinzipal zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c39a-119">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="1c39a-120">Für Dienstprinzipale stehen zwei Authentifizierungstypen zur Verfügung: Kennwortbasierte Authentifizierung und zertifikatbasierte Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="1c39a-120">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="1c39a-121">Kennwortbasierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="1c39a-121">Password-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c39a-122">Die Standardrolle für einen Dienstprinzipal mit kennwortbasierter Authentifizierung ist **Mitwirkender**.</span><span class="sxs-lookup"><span data-stu-id="1c39a-122">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="1c39a-123">Diese Rolle besitzt uneingeschränkte Berechtigungen für Lese- und Schreibvorgänge in einem Azure-Konto.</span><span class="sxs-lookup"><span data-stu-id="1c39a-123">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="1c39a-124">Informationen zum Verwalten von Rollenzuweisungen finden Sie unter [Verwalten von Dienstprinzipalrollen](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="1c39a-124">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="1c39a-125">Ohne weitere Authentifizierungsparameter wird die kennwortbasierte Authentifizierung mit einem für Sie erstellten zufälligen Kennwort verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c39a-125">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="1c39a-126">Diese Methode wird empfohlen, wenn Sie die kennwortbasierte Authentifizierung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="1c39a-126">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="1c39a-127">Das zurückgegebene Objekt enthält den `Secret`-Member; dabei handelt es sich um ein `SecureString`-Element, in dem das generierte Kennwort enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="1c39a-127">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="1c39a-128">Achten Sie darauf, diesen Wert für die Authentifizierung beim Dienstprinzipal an einem sicheren Ort zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1c39a-128">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="1c39a-129">Der Wert _wird nicht_ in der Konsolenausgabe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1c39a-129">Its value _won't_ be displayed in the console output.</span></span> <span data-ttu-id="1c39a-130">Wenn Sie das Kennwort verlieren, [setzen Sie die Anmeldeinformationen des Dienstprinzipals zurück](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="1c39a-130">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="1c39a-131">Mit dem folgenden Code können Sie das Geheimnis exportieren:</span><span class="sxs-lookup"><span data-stu-id="1c39a-131">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="1c39a-132">Für benutzerdefinierte Kennwörter akzeptiert das `-PasswordCredential`-Argument `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`-Objekte.</span><span class="sxs-lookup"><span data-stu-id="1c39a-132">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="1c39a-133">Diese Objekte müssen gültige Werte für `StartDate` und `EndDate` haben und ein `Password`-Element in Klartext akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="1c39a-133">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="1c39a-134">Halten Sie sich beim Erstellen eines Kennworts unbedingt an die Vorgaben unter [Kennwortrichtlinien und -einschränkungen in Azure Active Directory](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="1c39a-134">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span>
<span data-ttu-id="1c39a-135">Verwenden Sie kein unsicheres Kennwort, und verwenden Sie ein Kennwort nicht erneut.</span><span class="sxs-lookup"><span data-stu-id="1c39a-135">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="1c39a-136">Das von `New-AzADServicePrincipal` zurückgegebene Objekt enthält die Member `Id` und `DisplayName`, die jeweils für die Anmeldung beim Dienstprinzipal verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1c39a-136">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c39a-137">Das Anmelden bei einem Dienstprinzipal erfordert die ID des Mandanten, unter dem der Dienstprinzipal erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1c39a-137">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="1c39a-138">Führen Sie den folgenden Befehl _unmittelbar nach_ der Erstellung des Dienstprinzipals aus, um den aktiven Mandanten abzurufen:</span><span class="sxs-lookup"><span data-stu-id="1c39a-138">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a><span data-ttu-id="1c39a-139">Zertifikatbasierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="1c39a-139">Certificate-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c39a-140">Beim Erstellen eines Dienstprinzipals mit zertifikatbasierter Authentifizierung wird keine Standardrolle zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="1c39a-140">There is no default role assigned when creating a certificate-based authentication service principal.</span></span> <span data-ttu-id="1c39a-141">Informationen zum Verwalten von Rollenzuweisungen finden Sie unter [Verwalten von Dienstprinzipalrollen](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="1c39a-141">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="1c39a-142">Dienstprinzipale mit zertifikatbasierter Authentifizierung werden mit dem Parameter `-CertValue` erstellt.</span><span class="sxs-lookup"><span data-stu-id="1c39a-142">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="1c39a-143">Dieser Parameter nimmt eine Base64-codierte ASCII-Zeichenfolge des öffentlichen Zertifikats entgegen.</span><span class="sxs-lookup"><span data-stu-id="1c39a-143">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="1c39a-144">Diese wird durch eine PEM-Datei oder eine textcodierte CRT- oder CER-Datei dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1c39a-144">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="1c39a-145">Binäre Codierungen des öffentlichen Zertifikats werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c39a-145">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="1c39a-146">Für diese Anweisungen wird davon ausgegangen, dass bereits ein Zertifikat verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1c39a-146">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="1c39a-147">Sie können auch den Parameter `-KeyCredential` verwenden, der `PSADKeyCredential`-Objekte entgegennimmt.</span><span class="sxs-lookup"><span data-stu-id="1c39a-147">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="1c39a-148">Diese Objekte müssen gültige `StartDate`- und `EndDate`-Werte aufweisen, und der Member `CertValue` muss auf eine Base64-codierte ASCII-Zeichenfolge des öffentlichen Zertifikats festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="1c39a-148">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="1c39a-149">Das von `New-AzADServicePrincipal` zurückgegebene Objekt enthält die Member `Id` und `DisplayName`, die jeweils für die Anmeldung beim Dienstprinzipal verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1c39a-149">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="1c39a-150">Clients benötigen für die Anmeldung beim Dienstprinzipal außerdem Zugriff auf den privaten Schlüssel des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="1c39a-150">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c39a-151">Das Anmelden bei einem Dienstprinzipal erfordert die ID des Mandanten, unter dem der Dienstprinzipal erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1c39a-151">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="1c39a-152">Führen Sie den folgenden Befehl _unmittelbar nach_ der Erstellung des Dienstprinzipals aus, um den aktiven Mandanten abzurufen:</span><span class="sxs-lookup"><span data-stu-id="1c39a-152">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="1c39a-153">Abrufen eines vorhandenen Dienstprinzipals</span><span class="sxs-lookup"><span data-stu-id="1c39a-153">Get an existing service principal</span></span>

<span data-ttu-id="1c39a-154">Eine Liste der Dienstprinzipale für den aktiven Mandanten kann mit [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal) abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1c39a-154">A list of service principals for the active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="1c39a-155">Dieser Befehl gibt standardmäßig _alle_ Dienstprinzipale in einem Mandanten zurück.</span><span class="sxs-lookup"><span data-stu-id="1c39a-155">By default this command returns _all_ service principals in a tenant.</span></span> <span data-ttu-id="1c39a-156">Für große Organisationen kann es lange dauern, bis Ergebnisse zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1c39a-156">For large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="1c39a-157">Stattdessen wird die Verwendung eines der optionalen serverseitigen Filterungsargumente empfohlen:</span><span class="sxs-lookup"><span data-stu-id="1c39a-157">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

- <span data-ttu-id="1c39a-158">`-DisplayNameBeginsWith` fordert Dienstprinzipale mit einem _Präfix_ an, das dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="1c39a-158">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="1c39a-159">Der Anzeigename eines Dienstprinzipals ist der Wert, der während der Erstellung mit `-DisplayName` festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1c39a-159">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
- <span data-ttu-id="1c39a-160">`-DisplayName` fordert die _genaue Übereinstimmung_ eines Dienstprinzipalnamens an.</span><span class="sxs-lookup"><span data-stu-id="1c39a-160">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="1c39a-161">Verwalten von Dienstprinzipalrollen</span><span class="sxs-lookup"><span data-stu-id="1c39a-161">Manage service principal roles</span></span>

<span data-ttu-id="1c39a-162">Für die Verwaltung von Rollenzuweisungen stehen in Azure PowerShell folgende Cmdlets zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="1c39a-162">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

- [<span data-ttu-id="1c39a-163">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1c39a-163">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
- [<span data-ttu-id="1c39a-164">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1c39a-164">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
- [<span data-ttu-id="1c39a-165">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1c39a-165">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="1c39a-166">Die Standardrolle für einen Dienstprinzipal mit kennwortbasierter Authentifizierung ist **Mitwirkender**.</span><span class="sxs-lookup"><span data-stu-id="1c39a-166">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="1c39a-167">Diese Rolle besitzt uneingeschränkte Berechtigungen für Lese- und Schreibvorgänge in einem Azure-Konto.</span><span class="sxs-lookup"><span data-stu-id="1c39a-167">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="1c39a-168">Die Rolle **Leser** ist stärker eingeschränkt und bietet schreibgeschützten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="1c39a-168">The **Reader** role is more restrictive, with read-only access.</span></span> <span data-ttu-id="1c39a-169">Weitere Informationen zur rollenbasierten Zugriffssteuerung (Role-Based Access Control, RBAC) finden Sie unter [Rollenbasierte Zugriffssteuerung: Integrierte Rollen](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="1c39a-169">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="1c39a-170">Das folgende Beispiel fügt die Rolle **Leser** hinzu und entfernt die Rolle **Mitwirkender**:</span><span class="sxs-lookup"><span data-stu-id="1c39a-170">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> <span data-ttu-id="1c39a-171">Cmdlets für die Rollenzuweisung akzeptieren die Objekt-ID des Dienstprinzipals nicht.</span><span class="sxs-lookup"><span data-stu-id="1c39a-171">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="1c39a-172">Sie nehmen die zugeordnete Anwendungs-ID an, die zum Zeitpunkt der Erstellung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="1c39a-172">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="1c39a-173">Verwenden Sie `Get-AzADServicePrincipal` zum Abrufen der Anwendungs-ID für einen Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="1c39a-173">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="1c39a-174">Wenn Ihr Konto nicht über die Berechtigung zum Zuweisen einer Rolle verfügt, wird eine Fehlermeldung mit dem Hinweis angezeigt, dass Ihr Konto keine Berechtigung zum Ausführen der Aktion „Microsoft.Authorization/roleAssignments/write“ hat.</span><span class="sxs-lookup"><span data-stu-id="1c39a-174">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'".</span></span> <span data-ttu-id="1c39a-175">Bitten Sie den Azure Active Directory-Administrator um die Verwaltung von Rollen.</span><span class="sxs-lookup"><span data-stu-id="1c39a-175">Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="1c39a-176">Durch das Hinzufügen einer Rolle werden zuvor zugewiesene Berechtigungen _nicht_ eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="1c39a-176">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="1c39a-177">Beim Einschränken der Berechtigungen eines Dienstprinzipals sollte die Rolle **Mitwirkender** entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1c39a-177">When restricting a service principal's permissions, the **Contributor** role should be removed.</span></span>

<span data-ttu-id="1c39a-178">Die Änderungen können durch Auflisten der zugewiesenen Rollen überprüft werden:</span><span class="sxs-lookup"><span data-stu-id="1c39a-178">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="1c39a-179">Anmelden mithilfe eines Dienstprinzipals</span><span class="sxs-lookup"><span data-stu-id="1c39a-179">Sign in using a service principal</span></span>

<span data-ttu-id="1c39a-180">Testen Sie die Anmeldeinformationen und Berechtigungen des neuen Dienstprinzipals, indem Sie sich anmelden.</span><span class="sxs-lookup"><span data-stu-id="1c39a-180">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="1c39a-181">Zur Anmeldung bei einem Dienstprinzipal benötigen Sie den `applicationId`-Wert, der ihm zugeordnet ist, und den Mandanten, unter dem er erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1c39a-181">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="1c39a-182">So melden Sie sich mit einem Dienstprinzipal und einem Kennwort an:</span><span class="sxs-lookup"><span data-stu-id="1c39a-182">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID>
```

<span data-ttu-id="1c39a-183">Zertifikatbasierte Authentifizierung erfordert, dass Azure PowerShell Informationen von einem lokalen Zertifikatsspeicher basierend auf einem Fingerabdruck des Zertifikats abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="1c39a-183">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <tenant ID> -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="1c39a-184">Anweisungen zum Importieren eines Zertifikats in einen für PowerShell zugänglichen Anmeldeinformationsspeicher finden Sie unter [Anmelden mit Azure PowerShell](authenticate-azureps.md#sp-signin).</span><span class="sxs-lookup"><span data-stu-id="1c39a-184">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="1c39a-185">Zurücksetzen von Anmeldeinformation</span><span class="sxs-lookup"><span data-stu-id="1c39a-185">Reset credentials</span></span>

<span data-ttu-id="1c39a-186">Wenn Sie die Anmeldeinformationen für einen Dienstprinzipal vergessen, verwenden Sie [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential), um neue Anmeldeinformationen mit einem zufälligen Kennwort hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1c39a-186">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential with a random password.</span></span> <span data-ttu-id="1c39a-187">Dieses Cmdlet unterstützt beim Zurücksetzen des Kennworts keine benutzerdefinierten Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="1c39a-187">This cmdlet does not support user-defined credentials when resetting the password.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c39a-188">Vor dem Zuweisen von neuen Anmeldeinformationen empfiehlt es sich, vorhandene Anmeldeinformationen zu entfernen, um eine versehentliche Anmeldung damit zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="1c39a-188">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="1c39a-189">Verwenden Sie dazu das Cmdlet [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):</span><span class="sxs-lookup"><span data-stu-id="1c39a-189">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a><span data-ttu-id="1c39a-190">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="1c39a-190">Troubleshooting</span></span>

<span data-ttu-id="1c39a-191">Bei Anzeige der Fehlermeldung _„New-AzADServicePrincipal: Another object with the same value for property identifierUris already exists.“_ stellen Sie sicher, dass noch kein Dienstprinzipal mit dem gleichen Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1c39a-191">If you receive the error: _"New-AzADServicePrincipal: Another object with the same value for property identifierUris already exists."_, verify that a service principal with the same name doesn't already exist.</span></span>

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="1c39a-192">Wenn der vorhandene Dienstprinzipal nicht mehr benötigt wird, können Sie ihn mit dem folgenden Beispiel entfernen.</span><span class="sxs-lookup"><span data-stu-id="1c39a-192">If the existing service principal is no longer needed, you can remove it using the following example.</span></span>

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="1c39a-193">Dieser Fehler kann auch auftreten, wenn Sie zuvor einen Dienstprinzipal für eine Azure Active Directory-Anwendung erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="1c39a-193">This error can also occur when you've previously created a service principal for an Azure Active Directory application.</span></span> <span data-ttu-id="1c39a-194">Wenn Sie den Dienstprinzipal entfernen, ist die Anwendung weiterhin verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1c39a-194">If you remove the service principal, the application is still available.</span></span> <span data-ttu-id="1c39a-195">Diese Anwendung verhindert, dass Sie einen anderen Dienstprinzipal mit demselben Namen erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c39a-195">This application prevents you from creating another service principal with the same name.</span></span>

<span data-ttu-id="1c39a-196">Verwenden Sie das folgende Beispiel, um zu überprüfen, ob bereits eine Azure Active Directory-Anwendung mit demselben Namen vorhanden ist:</span><span class="sxs-lookup"><span data-stu-id="1c39a-196">You can use the following example to verify that an Azure Active Directory application with the same name doesn't exist:</span></span>

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="1c39a-197">Wenn eine Anwendung mit demselben Namen vorhanden ist und nicht mehr benötigt wird, kann Sie mithilfe des folgenden Beispiels entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1c39a-197">If an application with the same name does exist and is no longer needed, it can be removed using the following example.</span></span>

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="1c39a-198">Wählen Sie andernfalls einen alternativen Namen für den neuen Dienstprinzipal aus, den Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="1c39a-198">Otherwise, choose an alternate name for the new service principal that you're attempting to create.</span></span>
