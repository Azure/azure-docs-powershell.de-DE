---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 9fc7b3de271188c2f8ebd0be3293892a6fae56e3
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251776"
---
# <span data-ttu-id="2c8ec-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2c8ec-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="2c8ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c8ec-102">SYNOPSIS</span></span>
<span data-ttu-id="2c8ec-103">Erstellt einen neuen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="2c8ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c8ec-104">SYNTAX</span></span>

### <span data-ttu-id="2c8ec-105">SimpleParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2c8ec-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c8ec-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c8ec-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c8ec-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c8ec-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c8ec-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c8ec-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c8ec-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c8ec-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c8ec-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c8ec-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c8ec-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c8ec-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c8ec-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c8ec-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c8ec-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c8ec-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c8ec-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c8ec-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c8ec-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c8ec-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c8ec-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c8ec-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c8ec-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c8ec-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c8ec-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c8ec-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c8ec-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c8ec-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c8ec-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c8ec-120">DESCRIPTION</span></span>

<span data-ttu-id="2c8ec-121">Erstellt einen neuen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="2c8ec-122">Der Standardparametersatz verwendet Standardwerte für Parameter, wenn diese nicht bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="2c8ec-123">Weitere Informationen zu Standardwerten finden Sie in der Beschreibung für jeden Parameter.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="2c8ec-124">Dieses Cmdlet kann dem Dienstprinzipal mit den  Parametern "Rolle" und **"Bereich" eine Rolle** zuweisen.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="2c8ec-125">Fehlt beides, wird die Mitwirkenderolle dem Dienstprinzipal zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="2c8ec-126">Die Standardwerte für die Parameter **"Rolle"** und **"Bereich"** sind **"Mitwirkender"** für das aktuelle Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="2c8ec-127">Das Cmdlet erstellt eine Anwendung und legt deren Eigenschaften fest, wenn keine ApplicationId angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="2c8ec-128">Verwenden Sie das Cmdlet ["Update-AzADApplication",](./update-azadapplication.md) um die anwendungsspezifischen Parameter zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="2c8ec-129">Wenn Sie einen Dienstprinzipal mit dem Befehl **"New-AzADServicePrincipal"** erstellen, enthält die Ausgabe Anmeldeinformationen, die Sie schützen müssen.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="2c8ec-130">Erwägen Sie alternativ die Verwendung [verwalteter Identitäten,](/azure/active-directory/managed-identities-azure-resources/overview) um die Verwendung von Anmeldeinformationen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-130">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="2c8ec-131">Standardmäßig weist **"New-AzADServicePrincipal"** dem Dienstprinzipal im Abonnementbereich die Rolle "Mitwirkender" zu. [](/azure/role-based-access-control/built-in-roles#contributor)</span><span class="sxs-lookup"><span data-stu-id="2c8ec-131">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="2c8ec-132">Um das Risiko eines beeinträchtigten Dienstprinzipal zu verringern, weisen Sie eine spezifischere Rolle zu, und grenzen Sie den Bereich auf eine Ressource oder Ressourcengruppe ein.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-132">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="2c8ec-133">Weitere [Informationen finden Sie unter "Schritte zum Hinzufügen einer](/azure/role-based-access-control/role-assignments-steps) Rollenzuweisung".</span><span class="sxs-lookup"><span data-stu-id="2c8ec-133">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="2c8ec-134">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2c8ec-134">EXAMPLES</span></span>

### <span data-ttu-id="2c8ec-135">Beispiel 1: Einfache Erstellung des Ad -Dienstprinzipals</span><span class="sxs-lookup"><span data-stu-id="2c8ec-135">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="2c8ec-136">Im folgenden Beispiel wird ein Ad-Dienst-Prinzipal mit Standardwerten für nicht angegebene Parameter erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-136">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="2c8ec-137">Da keine Anwendungs-ID angegeben wird, wird eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-137">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="2c8ec-138">Da für "Rolle" oder **"Bereich"** keine Werte  bereitgestellt **werden,** wird dem erstellten Dienstprinzipal die Mitwirkenderolle für das aktuelle Abonnement zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-138">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="2c8ec-139">Beispiel 2: Einfache Erstellung des Ad -Dienstprinzipals mit einer bestimmten Rolle und einem Standardbereich</span><span class="sxs-lookup"><span data-stu-id="2c8ec-139">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="2c8ec-140">Im folgenden Beispiel wird ein Ad -Dienstprinzipal erstellt, in dem die Standardwerte für nicht angegebene Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-140">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="2c8ec-141">Da die Anwendungs-ID nicht angegeben wird, wird eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-141">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="2c8ec-142">Der Dienstprinzipal wird mit **Leseberechtigungen** für das aktuelle Abonnement erstellt, da für den Parameter **"Bereich"** kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-142">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000' to the new service principal.
```

### <span data-ttu-id="2c8ec-143">Beispiel 3: Einfache Erstellung des Ad -Dienstprinzipals mit einem angegebenen Bereich und einer Standardrolle</span><span class="sxs-lookup"><span data-stu-id="2c8ec-143">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="2c8ec-144">Im folgenden Beispiel wird ein Ad -Dienstprinzipal erstellt, in dem die Standardwerte für nicht angegebene Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-144">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="2c8ec-145">Da die Anwendungs-ID nicht angegeben wird, wird eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-145">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="2c8ec-146">Der Dienstprinzipal wird mit **Mitwirkendenberechtigungen für** den bereitgestellten Ressourcengruppenbereich erstellt, da für den Parameter **"Rolle"** kein Wert bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-146">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="2c8ec-147">Beispiel 4: Einfache Erstellung des Ad -Dienstprinzipals mit einem angegebenen Bereich und einer bestimmten Rolle</span><span class="sxs-lookup"><span data-stu-id="2c8ec-147">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="2c8ec-148">Im folgenden Beispiel wird ein Ad -Dienstprinzipal erstellt, in dem die Standardwerte für nicht angegebene Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-148">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="2c8ec-149">Da die Anwendungs-ID nicht angegeben wird, wird eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-149">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="2c8ec-150">Der Dienstprinzipal wird mit **Leseberechtigungen** für den bereitgestellten Ressourcengruppenbereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-150">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="2c8ec-151">Beispiel 5: Erstellen eines neuen Ad -Dienstprinzipal mithilfe der Anwendungs-ID mit Rollenzuweisung</span><span class="sxs-lookup"><span data-stu-id="2c8ec-151">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="2c8ec-152">Im folgenden Beispiel wird ein neuer Dienstprinzipal für die Anwendung mit der Anwendungs-ID '00000000-0000-0000-0000-000000000000' erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-152">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="2c8ec-153">Da für "Rolle" oder **"Bereich"** keine Werte  bereitgestellt **werden,** wird dem erstellten Dienstprinzipal die Mitwirkenderolle für das aktuelle Abonnement zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-153">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal -ApplicationId 00000000-0000-0000-0000-000000000000
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://my-temp-app}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : my-temp-app
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="2c8ec-154">Beispiel 6: Erstellen eines neuen Ad -Dienstprinzipal mithilfe der Piping</span><span class="sxs-lookup"><span data-stu-id="2c8ec-154">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="2c8ec-155">Im folgenden Beispiel wird die Anwendung mit der Objekt-ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' mit dem [Cmdlet "Get-AzADApplication"](./get-azadapplication.md) abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-155">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="2c8ec-156">Die Ergebnisse werden an das Cmdlet zu einem neuen `New-AzADServicePrincipal` Ad-Dienstprinzipal für diese Anwendung weitergedeh.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-156">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="2c8ec-157">Beispiel 7: Erstellen eines neuen Ad -Dienstprinzipals mit DisplayName und Kennwortanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="2c8ec-157">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="2c8ec-158">Im folgenden Beispiel wird eine neue Anwendung mit dem Namen **"ServicePrincipalName"** und dem Kennwort **"StrongPassworld!23" erstellt.**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-158">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="2c8ec-159">Der Dienstprinzipal wird basierend auf der erstellten Anwendung erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-159">It creates the service principal based on the created application.</span></span> <span data-ttu-id="2c8ec-160">Das Startdatum und das Enddatum werden den Anmeldeinformationen des Kennworts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-160">The start date and end date are added to the password credential.</span></span>

```powershell
$credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{
  StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password='StrongPassworld!23'}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000c
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

### <span data-ttu-id="2c8ec-161">Beispiel 8: Erstellen eines neuen Ad-Dienstprinzipals mit DisplayName und nur-Schlüssel-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="2c8ec-161">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="2c8ec-162">Im folgenden Beispiel wird eine neue Anwendung mit dem Namen **"ServicePrincipalName"** und einem **Zertifikat**$cert. Der Dienstprinzipal wird basierend auf der erstellten Anwendung erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-162">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="2c8ec-163">Das Enddatum wird den Schlüsselanmeldeinformationen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-163">The end date is added to key credential.</span></span>

```powershell
$cert = 'public certificate as Base64 encoded string'
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate '2021-01-01'
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

## <span data-ttu-id="2c8ec-164">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c8ec-164">PARAMETERS</span></span>

### <span data-ttu-id="2c8ec-165">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2c8ec-165">-ApplicationId</span></span>

<span data-ttu-id="2c8ec-166">Die eindeutige Anwendungs-ID für einen Dienstprinzipal in einem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-166">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="2c8ec-167">Nach der Erstellen kann diese Eigenschaft nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-167">Once created this property cannot be changed.</span></span> <span data-ttu-id="2c8ec-168">Wenn keine Anwendungs-ID für eine vorhandene Anwendung angegeben wird, wird eine Anwendung erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-168">If an application ID for an existing application is not specified, an application is created.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c8ec-169">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="2c8ec-169">-ApplicationObject</span></span>

<span data-ttu-id="2c8ec-170">Das Objekt, das die Anwendung darstellt, für die der Dienstprinzipal erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-170">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c8ec-171">-CertValue</span><span class="sxs-lookup"><span data-stu-id="2c8ec-171">-CertValue</span></span>

<span data-ttu-id="2c8ec-172">Der Wert des asymmetrischen Anmeldeinformationstyps.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-172">The value of the asymmetric credential type.</span></span> <span data-ttu-id="2c8ec-173">Sie stellt das base64-codierte Zertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-173">It represents the Base64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c8ec-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c8ec-174">-DefaultProfile</span></span>

<span data-ttu-id="2c8ec-175">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c8ec-176">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2c8ec-176">-DisplayName</span></span>

<span data-ttu-id="2c8ec-177">Der Anzeigename des Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-177">The friendly name of the service principal.</span></span> <span data-ttu-id="2c8ec-178">Wenn kein Anzeigename angegeben wird, wird für diesen Wert standardmäßig **"azure-powershell-MM-dd-yyyy-HH-mm-ss"** verwendet, wobei das Suffix der Zeitpunkt der Anwendungserstellung ist.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-178">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c8ec-179">-EndDate</span><span class="sxs-lookup"><span data-stu-id="2c8ec-179">-EndDate</span></span>

<span data-ttu-id="2c8ec-180">Das Effektive Enddatum der Verwendung der Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-180">The effective end date of the credential usage.</span></span> <span data-ttu-id="2c8ec-181">Der Standardmäßige Enddatumswert liegt ein Jahr nach heute.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-181">The default end date value is one year from today.</span></span>
<span data-ttu-id="2c8ec-182">Bei asymmetrischen Anmeldeinformationen muss dies auf das Datum oder vor dem Datum festgelegt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-182">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c8ec-183">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="2c8ec-183">-KeyCredential</span></span>

<span data-ttu-id="2c8ec-184">Die Sammlung der schlüsselanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-184">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c8ec-185">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="2c8ec-185">-PasswordCredential</span></span>

<span data-ttu-id="2c8ec-186">Die Sammlung von Kennwortanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-186">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c8ec-187">-Role</span><span class="sxs-lookup"><span data-stu-id="2c8ec-187">-Role</span></span>

<span data-ttu-id="2c8ec-188">Die Rolle, die der Dienstprinzipal über den Bereich besitzt.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-188">The role that the service principal has over the scope.</span></span> <span data-ttu-id="2c8ec-189">Wenn kein Wert angegeben wird, wird **"Rolle"** standardmäßig auf die **Mitwirkenderolle** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-189">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c8ec-190">-Scope</span><span class="sxs-lookup"><span data-stu-id="2c8ec-190">-Scope</span></span>

<span data-ttu-id="2c8ec-191">Der Bereich, für den der Dienstprinzipal Berechtigungen besitzt.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-191">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="2c8ec-192">Wenn kein Wert angegeben wird, **wird für den** Bereich standardmäßig das aktuelle Abonnement verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-192">If no value is provided, **Scope** defaults to the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c8ec-193">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="2c8ec-193">-SkipAssignment</span></span>

<span data-ttu-id="2c8ec-194">Wenn dies festgelegt ist, überspringen Sie die Erstellung der Standardrollezuweisung für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-194">If set, skip creating the default role assignment for the service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c8ec-195">-StartDate</span><span class="sxs-lookup"><span data-stu-id="2c8ec-195">-StartDate</span></span>

<span data-ttu-id="2c8ec-196">Das Effektive Startdatum der Nutzung der Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-196">The effective start date of the credential usage.</span></span> <span data-ttu-id="2c8ec-197">Der Standardwert für das Startdatum ist "Heute".</span><span class="sxs-lookup"><span data-stu-id="2c8ec-197">The default start date value is today.</span></span> <span data-ttu-id="2c8ec-198">Bei asymmetrischen Anmeldeinformationen muss dies auf das Datum oder nach dem Datum festgelegt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-198">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c8ec-199">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c8ec-199">-Confirm</span></span>

<span data-ttu-id="2c8ec-200">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-200">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c8ec-201">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2c8ec-201">-WhatIf</span></span>

<span data-ttu-id="2c8ec-202">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c8ec-203">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-203">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c8ec-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c8ec-204">CommonParameters</span></span>
<span data-ttu-id="2c8ec-205">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c8ec-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c8ec-206">Weitere Informationen finden Sie unter [about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="2c8ec-206">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="2c8ec-207">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2c8ec-207">INPUTS</span></span>

### <span data-ttu-id="2c8ec-208">System.Guid</span><span class="sxs-lookup"><span data-stu-id="2c8ec-208">System.Guid</span></span>

### <span data-ttu-id="2c8ec-209">System.String</span><span class="sxs-lookup"><span data-stu-id="2c8ec-209">System.String</span></span>

### <span data-ttu-id="2c8ec-210">Microsoft.Azure.Commands.ActiveDirectory.WERDENDApplication</span><span class="sxs-lookup"><span data-stu-id="2c8ec-210">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="2c8ec-211">Microsoft.Azure.Commands.ActiveDirectory.ODERDPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="2c8ec-211">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="2c8ec-212">Microsoft.Azure.Commands.ActiveDirectory.WERDENDKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="2c8ec-212">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="2c8ec-213">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="2c8ec-213">System.DateTime</span></span>

## <span data-ttu-id="2c8ec-214">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2c8ec-214">OUTPUTS</span></span>

### <span data-ttu-id="2c8ec-215">Microsoft.Azure.Commands.ActiveDirectory.WAHLDServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2c8ec-215">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="2c8ec-216">Microsoft.Azure.Commands.Resources.Models.Authorization.ODERDServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="2c8ec-216">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="2c8ec-217">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2c8ec-217">NOTES</span></span>

<span data-ttu-id="2c8ec-218">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="2c8ec-218">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="2c8ec-219">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2c8ec-219">RELATED LINKS</span></span>

[<span data-ttu-id="2c8ec-220">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2c8ec-220">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="2c8ec-221">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2c8ec-221">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="2c8ec-222">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="2c8ec-222">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="2c8ec-223">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="2c8ec-223">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="2c8ec-224">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2c8ec-224">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="2c8ec-225">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2c8ec-225">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="2c8ec-226">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2c8ec-226">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)
