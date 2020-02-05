---
title: Verwenden von Azure-Dienstprinzipalen mit Azure PowerShell
description: Hier erfahren Sie, wie Sie mit Azure PowerShell Dienstprinzipale erstellen und verwenden.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.openlocfilehash: 4c47d2bac2c63f13ac0ebbccda3e2eed12cd658f
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "77003097"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="e4623-103">Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e4623-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="e4623-104">Für automatisierte Tools, die Azure-Dienste verwenden, sollten stets eingeschränkte Berechtigungen festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="e4623-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="e4623-105">Azure bietet Dienstprinzipale, damit Anwendungen nicht als Benutzer mit uneingeschränkten Berechtigungen angemeldet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e4623-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="e4623-106">Ein Azure-Dienstprinzipal ist eine Identität, die zur Verwendung mit Anwendungen, gehosteten Diensten und automatisierten Tools für den Zugriff auf Azure-Ressourcen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e4623-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="e4623-107">Dieser Zugriff wird durch die dem Dienstprinzipal zugewiesenen Rollen eingeschränkt. Dadurch können Sie steuern, auf welcher Ebene auf welche Ressourcen zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="e4623-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="e4623-108">Aus Sicherheitsgründen wird stets empfohlen, Dienstprinzipale mit automatisierten Tools zu verwenden, statt ihnen die Anmeldung mit einer Benutzeridentität zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="e4623-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="e4623-109">In diesem Artikel wird Schritt für Schritt erläutert, wie Sie mit Azure PowerShell einen Dienstprinzipal erstellen, Informationen zu ihm abrufen und ihn zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="e4623-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="e4623-110">Erstellen eines Dienstprinzipals</span><span class="sxs-lookup"><span data-stu-id="e4623-110">Create a service principal</span></span>

<span data-ttu-id="e4623-111">Erstellen Sie mit dem Cmdlet [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) einen Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="e4623-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="e4623-112">Beim Erstellen eines Dienstprinzipals wählen Sie den Typ der von ihm verwendeten Anmeldeauthentifizierung aus.</span><span class="sxs-lookup"><span data-stu-id="e4623-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
>
> <span data-ttu-id="e4623-113">Wenn Ihr Konto nicht über Berechtigungen zum Erstellen eines Dienstprinzipals verfügt, gibt `New-AzADServicePrincipal` eine Fehlermeldung mit dem Hinweis „Nicht genügend Berechtigungen zum Abschließen des Vorgangs“ zurück.</span><span class="sxs-lookup"><span data-stu-id="e4623-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="e4623-114">Bitten Sie den Azure Active Directory-Administrator, einen Dienstprinzipal zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e4623-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="e4623-115">Für Dienstprinzipale stehen zwei Authentifizierungstypen zur Verfügung: Kennwortbasierte Authentifizierung und zertifikatbasierte Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="e4623-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="e4623-116">Kennwortbasierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="e4623-116">Password-based authentication</span></span>

<span data-ttu-id="e4623-117">Ohne weitere Authentifizierungsparameter wird die kennwortbasierte Authentifizierung mit einem für Sie erstellten zufälligen Kennwort verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4623-117">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="e4623-118">Diese Methode wird empfohlen, wenn Sie die kennwortbasierte Authentifizierung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="e4623-118">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="e4623-119">Das zurückgegebene Objekt enthält den `Secret`-Member; dabei handelt es sich um ein `SecureString`-Element, in dem das generierte Kennwort enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e4623-119">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="e4623-120">Achten Sie darauf, diesen Wert für die Authentifizierung beim Dienstprinzipal an einem sicheren Ort zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e4623-120">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="e4623-121">Der Wert __wird nicht__ in der Konsolenausgabe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e4623-121">Its value __won't__ be displayed in the console output.</span></span> <span data-ttu-id="e4623-122">Wenn Sie das Kennwort verlieren, [setzen Sie die Anmeldeinformationen des Dienstprinzipals zurück](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="e4623-122">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="e4623-123">Mit dem folgenden Code können Sie das Geheimnis exportieren:</span><span class="sxs-lookup"><span data-stu-id="e4623-123">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="e4623-124">Für benutzerdefinierte Kennwörter akzeptiert das `-PasswordCredential`-Argument `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`-Objekte.</span><span class="sxs-lookup"><span data-stu-id="e4623-124">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="e4623-125">Diese Objekte müssen gültige Werte für `StartDate` und `EndDate` haben und ein `Password`-Element in Klartext akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="e4623-125">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="e4623-126">Halten Sie sich beim Erstellen eines Kennworts unbedingt an die Vorgaben unter [Kennwortrichtlinien und -einschränkungen in Azure Active Directory](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="e4623-126">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="e4623-127">Verwenden Sie kein unsicheres Kennwort, und verwenden Sie ein Kennwort nicht erneut.</span><span class="sxs-lookup"><span data-stu-id="e4623-127">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="e4623-128">Das von `New-AzADServicePrincipal` zurückgegebene Objekt enthält die Member `Id` und `DisplayName`, die jeweils für die Anmeldung beim Dienstprinzipal verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e4623-128">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="e4623-129">Das Anmelden bei einem Dienstprinzipal erfordert die ID des Mandanten, unter dem der Dienstprinzipal erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e4623-129">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="e4623-130">Führen Sie den folgenden Befehl __unmittelbar nach__ der Erstellung des Dienstprinzipals aus, um den aktiven Mandanten abzurufen:</span><span class="sxs-lookup"><span data-stu-id="e4623-130">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a><span data-ttu-id="e4623-131">Zertifikatbasierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="e4623-131">Certificate-based authentication</span></span>

<span data-ttu-id="e4623-132">Dienstprinzipale mit zertifikatbasierter Authentifizierung werden mit dem Parameter `-CertValue` erstellt.</span><span class="sxs-lookup"><span data-stu-id="e4623-132">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="e4623-133">Dieser Parameter nimmt eine Base64-codierte ASCII-Zeichenfolge des öffentlichen Zertifikats entgegen.</span><span class="sxs-lookup"><span data-stu-id="e4623-133">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="e4623-134">Diese wird durch eine PEM-Datei oder eine textcodierte CRT- oder CER-Datei dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e4623-134">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="e4623-135">Binäre Codierungen des öffentlichen Zertifikats werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e4623-135">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="e4623-136">Für diese Anweisungen wird davon ausgegangen, dass bereits ein Zertifikat verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e4623-136">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="e4623-137">Sie können auch den Parameter `-KeyCredential` verwenden, der `PSADKeyCredential`-Objekte entgegennimmt.</span><span class="sxs-lookup"><span data-stu-id="e4623-137">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="e4623-138">Diese Objekte müssen gültige `StartDate`- und `EndDate`-Werte aufweisen, und der Member `CertValue` muss auf eine Base64-codierte ASCII-Zeichenfolge des öffentlichen Zertifikats festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="e4623-138">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="e4623-139">Das von `New-AzADServicePrincipal` zurückgegebene Objekt enthält die Member `Id` und `DisplayName`, die jeweils für die Anmeldung beim Dienstprinzipal verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e4623-139">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="e4623-140">Clients benötigen für die Anmeldung beim Dienstprinzipal außerdem Zugriff auf den privaten Schlüssel des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="e4623-140">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="e4623-141">Das Anmelden bei einem Dienstprinzipal erfordert die ID des Mandanten, unter dem der Dienstprinzipal erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e4623-141">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="e4623-142">Führen Sie den folgenden Befehl __unmittelbar nach__ der Erstellung des Dienstprinzipals aus, um den aktiven Mandanten abzurufen:</span><span class="sxs-lookup"><span data-stu-id="e4623-142">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="e4623-143">Abrufen eines vorhandenen Dienstprinzipals</span><span class="sxs-lookup"><span data-stu-id="e4623-143">Get an existing service principal</span></span>

<span data-ttu-id="e4623-144">Eine Liste der Dienstprinzipale für den derzeit aktiven Mandanten kann mit [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal) abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e4623-144">A list of service principals for the currently active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="e4623-145">Dieser Befehl gibt standardmäßig __alle__ Dienstprinzipale in einem Mandanten zurück, daher kann die Rückgabe von Ergebnissen für große Organisationen lange dauern.</span><span class="sxs-lookup"><span data-stu-id="e4623-145">By default this command returns __all__ service principals in a tenant, so for large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="e4623-146">Stattdessen wird die Verwendung eines der optionalen serverseitigen Filterungsargumente empfohlen:</span><span class="sxs-lookup"><span data-stu-id="e4623-146">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

* <span data-ttu-id="e4623-147">`-DisplayNameBeginsWith` fordert Dienstprinzipale mit einem _Präfix_ an, das dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="e4623-147">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="e4623-148">Der Anzeigename eines Dienstprinzipals ist der Wert, der während der Erstellung mit `-DisplayName` festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e4623-148">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
* <span data-ttu-id="e4623-149">`-DisplayName` fordert die _genaue Übereinstimmung_ eines Dienstprinzipalnamens an.</span><span class="sxs-lookup"><span data-stu-id="e4623-149">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="e4623-150">Verwalten von Dienstprinzipalrollen</span><span class="sxs-lookup"><span data-stu-id="e4623-150">Manage service principal roles</span></span>

<span data-ttu-id="e4623-151">Für die Verwaltung von Rollenzuweisungen stehen in Azure PowerShell folgende Cmdlets zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="e4623-151">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="e4623-152">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e4623-152">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="e4623-153">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e4623-153">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="e4623-154">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e4623-154">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="e4623-155">Standardmäßig hat ein Dienstprinzipal die Rolle **Mitwirkender**.</span><span class="sxs-lookup"><span data-stu-id="e4623-155">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="e4623-156">Diese Rolle besitzt uneingeschränkte Berechtigungen für Lese- und Schreibvorgänge in einem Azure-Konto.</span><span class="sxs-lookup"><span data-stu-id="e4623-156">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="e4623-157">Die Rolle **Leser** ist stärker eingeschränkt und bietet schreibgeschützten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="e4623-157">The **Reader** role is more restrictive, with read-only access.</span></span>  <span data-ttu-id="e4623-158">Weitere Informationen zur rollenbasierten Zugriffssteuerung (Role-Based Access Control, RBAC) finden Sie unter [Rollenbasierte Zugriffssteuerung: Integrierte Rollen](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="e4623-158">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="e4623-159">Das folgende Beispiel fügt die Rolle **Leser** hinzu und entfernt die Rolle **Mitwirkender**:</span><span class="sxs-lookup"><span data-stu-id="e4623-159">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> <span data-ttu-id="e4623-160">Cmdlets für die Rollenzuweisung akzeptieren die Objekt-ID des Dienstprinzipals nicht.</span><span class="sxs-lookup"><span data-stu-id="e4623-160">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="e4623-161">Sie nehmen die zugeordnete Anwendungs-ID an, die zum Zeitpunkt der Erstellung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="e4623-161">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="e4623-162">Verwenden Sie `Get-AzADServicePrincipal` zum Abrufen der Anwendungs-ID für einen Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="e4623-162">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="e4623-163">Wenn Ihr Konto nicht über Berechtigungen zum Zuweisen einer Rolle verfügt, wird eine Fehlermeldung mit dem Hinweis angezeigt, dass Ihr Konto keine Berechtigung zum Ausführen der Aktion „Microsoft.Authorization/roleAssignments/write“ hat. Bitten Sie den Azure Active Directory-Administrator um die Verwaltung von Rollen.</span><span class="sxs-lookup"><span data-stu-id="e4623-163">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'." Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="e4623-164">Durch das Hinzufügen einer Rolle werden zuvor zugewiesene Berechtigungen _nicht_ eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="e4623-164">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="e4623-165">Beim Einschränken der Berechtigungen eines Dienstprinzipals sollte die Rolle __Mitwirkender__ entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e4623-165">When restricting a service principal's permissions, the __Contributor__ role should be removed.</span></span>

<span data-ttu-id="e4623-166">Die Änderungen können durch Auflisten der zugewiesenen Rollen überprüft werden:</span><span class="sxs-lookup"><span data-stu-id="e4623-166">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="e4623-167">Anmelden mithilfe eines Dienstprinzipals</span><span class="sxs-lookup"><span data-stu-id="e4623-167">Sign in using a service principal</span></span>

<span data-ttu-id="e4623-168">Testen Sie die Anmeldeinformationen und Berechtigungen des neuen Dienstprinzipals, indem Sie sich anmelden.</span><span class="sxs-lookup"><span data-stu-id="e4623-168">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="e4623-169">Zur Anmeldung bei einem Dienstprinzipal benötigen Sie den `applicationId`-Wert, der ihm zugeordnet ist, und den Mandanten, unter dem er erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e4623-169">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="e4623-170">So melden Sie sich mit einem Dienstprinzipal und einem Kennwort an:</span><span class="sxs-lookup"><span data-stu-id="e4623-170">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

<span data-ttu-id="e4623-171">Zertifikatbasierte Authentifizierung erfordert, dass Azure PowerShell Informationen von einem lokalen Zertifikatsspeicher basierend auf einem Fingerabdruck des Zertifikats abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="e4623-171">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <tenant ID> -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="e4623-172">Anweisungen zum Importieren eines Zertifikats in einen für PowerShell zugänglichen Anmeldeinformationsspeicher finden Sie unter [Anmelden mit Azure PowerShell](authenticate-azureps.md#sp-signin).</span><span class="sxs-lookup"><span data-stu-id="e4623-172">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="e4623-173">Zurücksetzen von Anmeldeinformation</span><span class="sxs-lookup"><span data-stu-id="e4623-173">Reset credentials</span></span>

<span data-ttu-id="e4623-174">Wenn Sie die Anmeldeinformationen für einen Dienstprinzipal vergessen, verwenden Sie [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential), um neue Anmeldeinformationen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e4623-174">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential.</span></span> <span data-ttu-id="e4623-175">Dieses Cmdlet akzeptiert die gleichen Argumente und Typen von Anmeldeinformationen wie `New-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="e4623-175">This cmdlet takes the same credential arguments and types as `New-AzADServicePrincipal`.</span></span> <span data-ttu-id="e4623-176">Ohne Argumente für die Anmeldeinformationen wird ein neues `PasswordCredential`-Element mit einem zufällig generierten Kennwort erstellt.</span><span class="sxs-lookup"><span data-stu-id="e4623-176">Without any credential arguments, a new `PasswordCredential` with a random password is created.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e4623-177">Vor dem Zuweisen von neuen Anmeldeinformationen empfiehlt es sich, vorhandene Anmeldeinformationen zu entfernen, um eine versehentliche Anmeldung damit zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="e4623-177">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="e4623-178">Verwenden Sie dazu das Cmdlet [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):</span><span class="sxs-lookup"><span data-stu-id="e4623-178">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```
