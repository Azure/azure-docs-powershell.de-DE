---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: cd82db28fbf9902b0dedf9415290d769db3ea231
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251590"
---
# <span data-ttu-id="a3306-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a3306-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="a3306-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3306-102">SYNOPSIS</span></span>
<span data-ttu-id="a3306-103">Erstellt einen neuen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="a3306-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="a3306-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3306-104">SYNTAX</span></span>

### <span data-ttu-id="a3306-105">SimpleParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3306-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3306-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3306-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3306-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3306-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3306-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3306-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3306-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3306-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3306-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3306-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3306-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3306-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3306-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3306-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3306-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3306-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3306-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3306-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3306-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3306-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3306-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3306-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3306-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3306-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3306-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3306-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication>
 -PasswordCredential <PSADPasswordCredential[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3306-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3306-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3306-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3306-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3306-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3306-121">DESCRIPTION</span></span>
<span data-ttu-id="a3306-122">Erstellt einen neuen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="a3306-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="a3306-123">Der Standardparametersatz verwendet Standardwerte für Parameter, wenn der Benutzer keinen parameter angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="a3306-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="a3306-124">Weitere Informationen zu den verwendeten Standardwerten finden Sie in der Beschreibung der angegebenen Parameter unten.</span><span class="sxs-lookup"><span data-stu-id="a3306-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="a3306-125">Dieses Cmdlet hat die Möglichkeit, dem Dienstprinzipal eine Rolle mit den Parametern und den Parametern zuzuordnen. Wenn keiner dieser Parameter bereitgestellt wird, wird dem Dienstprinzipal keine Rolle `Role` `Scope` zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a3306-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="a3306-126">Die Standardwerte für "Contributor" und "Parameters" sind "Contributor" bzw. das aktuelle Abonnement (Hinweis: Die Standardwerte werden nur verwendet, wenn der Benutzer einen Wert für einen der beiden Parameter, aber nicht für den anderen Parameter `Role` `Scope` liefert).</span><span class="sxs-lookup"><span data-stu-id="a3306-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively (_note_: the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="a3306-127">Das Cmdlet erstellt außerdem implizit eine Anwendung und legt deren Eigenschaften fest (wenn die ApplicationId nicht angegeben wird).</span><span class="sxs-lookup"><span data-stu-id="a3306-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="a3306-128">Um die anwendungsspezifischen Parameter zu aktualisieren, verwenden Sie Set-AzADApplication Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3306-128">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="a3306-129">Wenn Sie einen Dienstprinzipal mit dem Befehl **"New-AzADServicePrincipal"** erstellen, enthält die Ausgabe Anmeldeinformationen, die Sie schützen müssen.</span><span class="sxs-lookup"><span data-stu-id="a3306-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="a3306-130">Erwägen Sie alternativ die Verwendung [verwalteter Identitäten,](/azure/active-directory/managed-identities-azure-resources/overview) um die Verwendung von Anmeldeinformationen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="a3306-130">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="a3306-131">Standardmäßig weist **"New-AzADServicePrincipal"** dem Dienstprinzipal im Abonnementbereich die Rolle "Mitwirkender" zu. [](/azure/role-based-access-control/built-in-roles#contributor)</span><span class="sxs-lookup"><span data-stu-id="a3306-131">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="a3306-132">Um das Risiko eines beeinträchtigten Dienstprinzipal zu verringern, weisen Sie eine spezifischere Rolle zu, und grenzen Sie den Bereich auf eine Ressource oder Ressourcengruppe ein.</span><span class="sxs-lookup"><span data-stu-id="a3306-132">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="a3306-133">Weitere [Informationen finden Sie unter "Schritte zum Hinzufügen einer](/azure/role-based-access-control/role-assignments-steps) Rollenzuweisung".</span><span class="sxs-lookup"><span data-stu-id="a3306-133">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="a3306-134">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a3306-134">EXAMPLES</span></span>

### <span data-ttu-id="a3306-135">Beispiel 1: Einfache Erstellung des Ad -Dienstprinzipals</span><span class="sxs-lookup"><span data-stu-id="a3306-135">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="a3306-136">Der oben aufgeführte Befehl erstellt einen Ad-Dienstprinzipal mit Standardwerten für Parameter, die nicht bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a3306-136">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="a3306-137">Da keine Anwendungs-ID bereitgestellt wurde, wurde eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3306-137">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="a3306-138">Da für oder für den erstellten Dienstprinzipal keine Werte bereitgestellt wurden, hat der erstellte Dienstprinzipal `Role` `Scope` keine Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="a3306-138">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="a3306-139">Beispiel 2: Erstellung eines einfachen Ad -Dienstprinzipals mit einer bestimmten Rolle und einem Standardbereich</span><span class="sxs-lookup"><span data-stu-id="a3306-139">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="a3306-140">Der oben aufgeführte Befehl erstellt einen Ad-Dienstprinzipal, indem die Standardwerte für nicht bereitgestellte Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3306-140">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="a3306-141">Da die Anwendungs-ID nicht bereitgestellt wurde, wurde eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3306-141">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="a3306-142">Der Dienstprinzipal wurde mit Leseberechtigungen für das aktuelle Abonnement erstellt (da für den Parameter kein Wert angegeben `Scope` wurde).</span><span class="sxs-lookup"><span data-stu-id="a3306-142">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="a3306-143">Beispiel 3: Erstellung eines einfachen Ad -Dienstprinzipals mit einem angegebenen Bereich und einer Standardrolle</span><span class="sxs-lookup"><span data-stu-id="a3306-143">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="a3306-144">Der oben aufgeführte Befehl erstellt einen Ad-Dienstprinzipal, indem die Standardwerte für nicht bereitgestellte Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3306-144">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="a3306-145">Da die Anwendungs-ID nicht bereitgestellt wurde, wurde eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3306-145">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="a3306-146">Der Dienstprinzipal wurde mit "Mitwirkenden"-Berechtigungen (da für den Parameter kein Wert bereitgestellt wurde) über dem bereitgestellten `Role` Ressourcengruppenbereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3306-146">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="a3306-147">Beispiel 4: Einfache Erstellung des Ad -Dienstprinzipals mit einem angegebenen Bereich und einer bestimmten Rolle</span><span class="sxs-lookup"><span data-stu-id="a3306-147">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="a3306-148">Der oben aufgeführte Befehl erstellt einen Ad-Dienstprinzipal, indem die Standardwerte für nicht bereitgestellte Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3306-148">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="a3306-149">Da die Anwendungs-ID nicht bereitgestellt wurde, wurde eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3306-149">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="a3306-150">Der Dienstprinzipal wurde mit Leseberechtigungen für den bereitgestellten Ressourcengruppenbereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3306-150">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="a3306-151">Beispiel 5: Erstellen eines neuen Ad -Dienstprinzipal mithilfe der Anwendungs-ID mit Rollenzuweisung</span><span class="sxs-lookup"><span data-stu-id="a3306-151">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="a3306-152">Erstellt einen neuen Ad-Dienstprinzipal für die Anwendung mit der Anwendungs-ID '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span><span class="sxs-lookup"><span data-stu-id="a3306-152">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="a3306-153">Da für oder für den erstellten Dienstprinzipal keine Werte bereitgestellt wurden, hat der erstellte Dienstprinzipal `Role` `Scope` keine Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="a3306-153">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="a3306-154">Beispiel 6: Erstellen eines neuen Ad -Dienstprinzipal mithilfe der Piping</span><span class="sxs-lookup"><span data-stu-id="a3306-154">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="a3306-155">Ruft die Anwendung mit der Objekt-ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' ab und gibt diese an das cmdlet New-AzADServicePrincipal weiter, um einen neuen Ad-Dienstprinzipal für diese Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a3306-155">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="a3306-156">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3306-156">PARAMETERS</span></span>

### <span data-ttu-id="a3306-157">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a3306-157">-ApplicationId</span></span>
<span data-ttu-id="a3306-158">Die eindeutige Anwendungs-ID für einen Dienstprinzipal in einem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="a3306-158">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="a3306-159">Nach der Erstellen kann diese Eigenschaft nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a3306-159">Once created this property cannot be changed.</span></span>
<span data-ttu-id="a3306-160">Wenn keine Anwendungs-ID angegeben ist, wird eine generiert.</span><span class="sxs-lookup"><span data-stu-id="a3306-160">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="a3306-161">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="a3306-161">-ApplicationObject</span></span>
<span data-ttu-id="a3306-162">Das Objekt, das die Anwendung darstellt, für die der Dienstprinzipal erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a3306-162">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3306-163">-CertValue</span><span class="sxs-lookup"><span data-stu-id="a3306-163">-CertValue</span></span>
<span data-ttu-id="a3306-164">Der Wert des "asymmetrischen" Anmeldeinformationstyps.</span><span class="sxs-lookup"><span data-stu-id="a3306-164">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="a3306-165">Es stellt das 64-codierte Basiszertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="a3306-165">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="a3306-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3306-166">-DefaultProfile</span></span>
<span data-ttu-id="a3306-167">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a3306-167">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3306-168">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a3306-168">-DisplayName</span></span>
<span data-ttu-id="a3306-169">Der Anzeigename des Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="a3306-169">The friendly name of the service principal.</span></span> <span data-ttu-id="a3306-170">Wenn kein Anzeigename angegeben wird, wird für diesen Wert standardmäßig "azure-powershell-MM-dd-yyyy-HH-mm-ss" verwendet, wobei das Suffix der Zeitpunkt der Anwendungserstellung ist.</span><span class="sxs-lookup"><span data-stu-id="a3306-170">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="a3306-171">-EndDate</span><span class="sxs-lookup"><span data-stu-id="a3306-171">-EndDate</span></span>
<span data-ttu-id="a3306-172">Das Effektive Enddatum der Verwendung der Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="a3306-172">The effective end date of the credential usage.</span></span>
<span data-ttu-id="a3306-173">Der Standardmäßige Enddatumswert liegt ein Jahr nach heute.</span><span class="sxs-lookup"><span data-stu-id="a3306-173">The default end date value is one year from today.</span></span> <span data-ttu-id="a3306-174">Bei Anmeldeinformationen vom Typ "asymmetrischer Art" muss dies auf das Datum oder vor dem Datum festgelegt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="a3306-174">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="a3306-175">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="a3306-175">-KeyCredential</span></span>
<span data-ttu-id="a3306-176">Die Sammlung der Schlüsselanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a3306-176">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3306-177">-Password</span><span class="sxs-lookup"><span data-stu-id="a3306-177">-Password</span></span>
<span data-ttu-id="a3306-178">Das Kennwort, das dem Dienstprinzipal zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3306-178">The password to be associated with the service principal.</span></span> <span data-ttu-id="a3306-179">Wenn kein Kennwort angegeben wird, wird eine zufällige GUID generiert und als Kennwort verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3306-179">If a password is not provided, a random GUID will be generated and used as the password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3306-180">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="a3306-180">-PasswordCredential</span></span>
<span data-ttu-id="a3306-181">Die Sammlung von Kennwortanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a3306-181">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3306-182">-Role</span><span class="sxs-lookup"><span data-stu-id="a3306-182">-Role</span></span>
<span data-ttu-id="a3306-183">Die Rolle, die der Dienstprinzipal über den Bereich besitzt.</span><span class="sxs-lookup"><span data-stu-id="a3306-183">The role that the service principal has over the scope.</span></span> <span data-ttu-id="a3306-184">Wenn ein Wert für angegeben wird, für den aber kein Wert angegeben ist, wird standardmäßig die Rolle `Scope` `Role` `Role` "Mitwirkender" verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3306-184">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="a3306-185">-Scope</span><span class="sxs-lookup"><span data-stu-id="a3306-185">-Scope</span></span>
<span data-ttu-id="a3306-186">Der Bereich, für den der Dienstprinzipal Berechtigungen besitzt.</span><span class="sxs-lookup"><span data-stu-id="a3306-186">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="a3306-187">Wenn ein Wert für angegeben wird, für den aber kein Wert angegeben ist, wird standardmäßig `Role` das aktuelle Abonnement `Scope` `Scope` verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3306-187">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="a3306-188">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="a3306-188">-SkipAssignment</span></span>
<span data-ttu-id="a3306-189">Wenn dies festgelegt ist, wird die Erstellung der Standardrollezuweisung für den Dienstprinzipal übersprungen.</span><span class="sxs-lookup"><span data-stu-id="a3306-189">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="a3306-190">-StartDate</span><span class="sxs-lookup"><span data-stu-id="a3306-190">-StartDate</span></span>
<span data-ttu-id="a3306-191">Das Effektive Startdatum der Nutzung der Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="a3306-191">The effective start date of the credential usage.</span></span>
<span data-ttu-id="a3306-192">Der Standardwert für das Startdatum ist "Heute".</span><span class="sxs-lookup"><span data-stu-id="a3306-192">The default start date value is today.</span></span> <span data-ttu-id="a3306-193">Bei Anmeldeinformationen vom Typ "asymmetrischer Art" muss dies auf das Datum oder nach dem Datum festgelegt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="a3306-193">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="a3306-194">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3306-194">-Confirm</span></span>
<span data-ttu-id="a3306-195">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3306-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3306-196">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a3306-196">-WhatIf</span></span>
<span data-ttu-id="a3306-197">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3306-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3306-198">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3306-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3306-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3306-199">CommonParameters</span></span>
<span data-ttu-id="a3306-200">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3306-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3306-201">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3306-201">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3306-202">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a3306-202">INPUTS</span></span>

### <span data-ttu-id="a3306-203">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a3306-203">System.Guid</span></span>

### <span data-ttu-id="a3306-204">System.String</span><span class="sxs-lookup"><span data-stu-id="a3306-204">System.String</span></span>

### <span data-ttu-id="a3306-205">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.WERDENDApplication</span><span class="sxs-lookup"><span data-stu-id="a3306-205">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="a3306-206">Parameter: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a3306-206">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="a3306-207">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.WERDENDPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="a3306-207">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="a3306-208">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.WERDENDKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="a3306-208">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="a3306-209">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="a3306-209">System.Security.SecureString</span></span>

### <span data-ttu-id="a3306-210">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="a3306-210">System.DateTime</span></span>

## <span data-ttu-id="a3306-211">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a3306-211">OUTPUTS</span></span>

### <span data-ttu-id="a3306-212">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.WAHLDServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a3306-212">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="a3306-213">Microsoft.Azure.Commands.Resources.Models.Authorization.ODERDServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="a3306-213">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="a3306-214">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a3306-214">NOTES</span></span>
<span data-ttu-id="a3306-215">Schlüsselwörter: azure, Az, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="a3306-215">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a3306-216">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a3306-216">RELATED LINKS</span></span>

[<span data-ttu-id="a3306-217">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a3306-217">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="a3306-218">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a3306-218">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="a3306-219">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a3306-219">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="a3306-220">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a3306-220">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="a3306-221">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a3306-221">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="a3306-222">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a3306-222">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="a3306-223">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a3306-223">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

