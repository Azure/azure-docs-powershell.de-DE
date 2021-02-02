---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: aa46a09eec134797f1dcacfeb0541769c4569e9e
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251740"
---
# <span data-ttu-id="55640-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="55640-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="55640-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55640-102">SYNOPSIS</span></span>
<span data-ttu-id="55640-103">Erstellt einen neuen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="55640-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="55640-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55640-104">SYNTAX</span></span>

### <span data-ttu-id="55640-105">SimpleParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="55640-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55640-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="55640-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55640-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="55640-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55640-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="55640-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55640-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="55640-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55640-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="55640-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55640-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="55640-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55640-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="55640-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55640-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="55640-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55640-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="55640-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55640-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="55640-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55640-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="55640-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55640-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="55640-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55640-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="55640-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55640-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="55640-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55640-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="55640-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55640-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55640-121">DESCRIPTION</span></span>
<span data-ttu-id="55640-122">Erstellt einen neuen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="55640-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="55640-123">Der Standardparametersatz verwendet Standardwerte für Parameter, wenn der Benutzer keinen parameter angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="55640-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="55640-124">Weitere Informationen zu den verwendeten Standardwerten finden Sie in der Beschreibung der angegebenen Parameter unten.</span><span class="sxs-lookup"><span data-stu-id="55640-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="55640-125">Dieses Cmdlet hat die Möglichkeit, dem Dienstprinzipal eine Rolle mit den Parametern und den Parametern zuzuordnen. Wenn keiner dieser Parameter bereitgestellt wird, wird dem Dienstprinzipal keine Rolle `Role` `Scope` zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="55640-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="55640-126">Die Standardwerte für "Contributor" und "Parameters" sind "Contributor" bzw. das aktuelle Abonnement (Hinweis: Die Standardwerte werden nur verwendet, wenn der Benutzer einen Wert für einen der beiden Parameter, aber nicht für den anderen Parameter `Role` `Scope` liefert).</span><span class="sxs-lookup"><span data-stu-id="55640-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively (_note_: the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="55640-127">Das Cmdlet erstellt außerdem implizit eine Anwendung und legt deren Eigenschaften fest (wenn die ApplicationId nicht angegeben wird).</span><span class="sxs-lookup"><span data-stu-id="55640-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="55640-128">Um die anwendungsspezifischen Parameter zu aktualisieren, verwenden Sie Set-AzADApplication Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55640-128">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="55640-129">Wenn Sie einen Dienstprinzipal mit dem Befehl **"New-AzADServicePrincipal"** erstellen, enthält die Ausgabe Anmeldeinformationen, die Sie schützen müssen.</span><span class="sxs-lookup"><span data-stu-id="55640-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="55640-130">Erwägen Sie alternativ die Verwendung [verwalteter Identitäten,](/azure/active-directory/managed-identities-azure-resources/overview) um die Verwendung von Anmeldeinformationen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="55640-130">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="55640-131">Standardmäßig weist **"New-AzADServicePrincipal"** dem Dienstprinzipal im Abonnementbereich die Rolle "Mitwirkender" zu. [](/azure/role-based-access-control/built-in-roles#contributor)</span><span class="sxs-lookup"><span data-stu-id="55640-131">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="55640-132">Um das Risiko eines beeinträchtigten Dienstprinzipal zu verringern, weisen Sie eine spezifischere Rolle zu, und grenzen Sie den Bereich auf eine Ressource oder Ressourcengruppe ein.</span><span class="sxs-lookup"><span data-stu-id="55640-132">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="55640-133">Weitere [Informationen finden Sie unter "Schritte zum Hinzufügen einer](/azure/role-based-access-control/role-assignments-steps) Rollenzuweisung".</span><span class="sxs-lookup"><span data-stu-id="55640-133">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="55640-134">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="55640-134">EXAMPLES</span></span>

### <span data-ttu-id="55640-135">Beispiel 1: Einfache Erstellung des Ad -Dienstprinzipals</span><span class="sxs-lookup"><span data-stu-id="55640-135">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="55640-136">Der oben aufgeführte Befehl erstellt einen Ad-Dienstprinzipal mit Standardwerten für Parameter, die nicht bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="55640-136">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="55640-137">Da keine Anwendungs-ID bereitgestellt wurde, wurde eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="55640-137">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="55640-138">Da für oder für den erstellten Dienstprinzipal keine Werte bereitgestellt wurden, verfügt der erstellte Dienstprinzipal `Role` `Scope` nicht über Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="55640-138">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="55640-139">Beispiel 2: Erstellung eines einfachen Ad -Dienstprinzipals mit einer bestimmten Rolle und einem Standardbereich</span><span class="sxs-lookup"><span data-stu-id="55640-139">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

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

<span data-ttu-id="55640-140">Der oben aufgeführte Befehl erstellt einen Ad-Dienstprinzipal, indem die Standardwerte für nicht bereitgestellte Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55640-140">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="55640-141">Da die Anwendungs-ID nicht bereitgestellt wurde, wurde eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="55640-141">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="55640-142">Der Dienstprinzipal wurde mit Leseberechtigungen für das aktuelle Abonnement erstellt (da für den Parameter kein Wert angegeben `Scope` wurde).</span><span class="sxs-lookup"><span data-stu-id="55640-142">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="55640-143">Beispiel 3: Erstellung eines einfachen Ad -Dienstprinzipals mit einem angegebenen Bereich und einer Standardrolle</span><span class="sxs-lookup"><span data-stu-id="55640-143">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

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

<span data-ttu-id="55640-144">Der oben aufgeführte Befehl erstellt einen Ad-Dienstprinzipal, indem die Standardwerte für nicht bereitgestellte Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55640-144">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="55640-145">Da die Anwendungs-ID nicht bereitgestellt wurde, wurde eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="55640-145">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="55640-146">Der Dienstprinzipal wurde mit "Mitwirkenden"-Berechtigungen (da für den Parameter kein Wert bereitgestellt wurde) über dem bereitgestellten `Role` Ressourcengruppenbereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="55640-146">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="55640-147">Beispiel 4: Einfache Erstellung des Ad -Dienstprinzipals mit einem angegebenen Bereich und einer bestimmten Rolle</span><span class="sxs-lookup"><span data-stu-id="55640-147">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

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

<span data-ttu-id="55640-148">Der oben aufgeführte Befehl erstellt einen Ad-Dienstprinzipal, indem die Standardwerte für nicht bereitgestellte Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55640-148">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="55640-149">Da die Anwendungs-ID nicht bereitgestellt wurde, wurde eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="55640-149">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="55640-150">Der Dienstprinzipal wurde mit Leseberechtigungen für den bereitgestellten Ressourcengruppenbereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="55640-150">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="55640-151">Beispiel 5: Erstellen eines neuen Ad -Dienstprinzipal mithilfe der Anwendungs-ID mit Rollenzuweisung</span><span class="sxs-lookup"><span data-stu-id="55640-151">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="55640-152">Erstellt einen neuen Ad-Dienstprinzipal für die Anwendung mit der Anwendungs-ID '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span><span class="sxs-lookup"><span data-stu-id="55640-152">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="55640-153">Da für oder für den erstellten Dienstprinzipal keine Werte bereitgestellt wurden, hat der erstellte Dienstprinzipal `Role` `Scope` keine Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="55640-153">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="55640-154">Beispiel 6: Erstellen eines neuen Ad -Dienstprinzipal mithilfe der Piping</span><span class="sxs-lookup"><span data-stu-id="55640-154">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="55640-155">Ruft die Anwendung mit der Objekt-ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' ab und gibt diese an das Cmdlet New-AzADServicePrincipal weiter, um einen neuen Ad-Dienstprinzipal für diese Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="55640-155">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="55640-156">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55640-156">PARAMETERS</span></span>

### <span data-ttu-id="55640-157">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="55640-157">-ApplicationId</span></span>
<span data-ttu-id="55640-158">Die eindeutige Anwendungs-ID für einen Dienstprinzipal in einem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="55640-158">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="55640-159">Nach der Erstellen kann diese Eigenschaft nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="55640-159">Once created this property cannot be changed.</span></span>
<span data-ttu-id="55640-160">Wenn keine Anwendungs-ID angegeben ist, wird eine generiert.</span><span class="sxs-lookup"><span data-stu-id="55640-160">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="55640-161">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="55640-161">-ApplicationObject</span></span>
<span data-ttu-id="55640-162">Das Objekt, das die Anwendung darstellt, für die der Dienstprinzipal erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="55640-162">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55640-163">-CertValue</span><span class="sxs-lookup"><span data-stu-id="55640-163">-CertValue</span></span>
<span data-ttu-id="55640-164">Der Wert des "asymmetrischen" Anmeldeinformationstyps.</span><span class="sxs-lookup"><span data-stu-id="55640-164">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="55640-165">Es stellt das 64-codierte Basiszertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="55640-165">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="55640-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55640-166">-DefaultProfile</span></span>
<span data-ttu-id="55640-167">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="55640-167">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55640-168">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="55640-168">-DisplayName</span></span>
<span data-ttu-id="55640-169">Der Anzeigename des Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="55640-169">The friendly name of the service principal.</span></span> <span data-ttu-id="55640-170">Wenn kein Anzeigename angegeben wird, wird für diesen Wert standardmäßig "azure-powershell-MM-dd-yyyy-HH-mm-ss" verwendet, wobei das Suffix der Zeitpunkt der Anwendungserstellung ist.</span><span class="sxs-lookup"><span data-stu-id="55640-170">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="55640-171">-EndDate</span><span class="sxs-lookup"><span data-stu-id="55640-171">-EndDate</span></span>
<span data-ttu-id="55640-172">Das Effektive Enddatum der Verwendung der Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="55640-172">The effective end date of the credential usage.</span></span>
<span data-ttu-id="55640-173">Der Standardmäßige Enddatumswert liegt ein Jahr nach heute.</span><span class="sxs-lookup"><span data-stu-id="55640-173">The default end date value is one year from today.</span></span> <span data-ttu-id="55640-174">Bei Anmeldeinformationen vom Typ "asymmetrischer Art" muss dies auf das Datum oder vor dem Datum festgelegt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="55640-174">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="55640-175">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="55640-175">-KeyCredential</span></span>
<span data-ttu-id="55640-176">Die Sammlung der schlüsselanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="55640-176">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="55640-177">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="55640-177">-PasswordCredential</span></span>
<span data-ttu-id="55640-178">Die Sammlung von Kennwortanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="55640-178">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="55640-179">-Role</span><span class="sxs-lookup"><span data-stu-id="55640-179">-Role</span></span>
<span data-ttu-id="55640-180">Die Rolle, die der Dienstprinzipal über den Bereich besitzt.</span><span class="sxs-lookup"><span data-stu-id="55640-180">The role that the service principal has over the scope.</span></span> <span data-ttu-id="55640-181">Wenn ein Wert für angegeben wird, für den aber kein Wert angegeben ist, wird standardmäßig die Rolle `Scope` `Role` `Role` "Mitwirkender" verwendet.</span><span class="sxs-lookup"><span data-stu-id="55640-181">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="55640-182">-Scope</span><span class="sxs-lookup"><span data-stu-id="55640-182">-Scope</span></span>
<span data-ttu-id="55640-183">Der Bereich, für den der Dienstprinzipal Berechtigungen besitzt.</span><span class="sxs-lookup"><span data-stu-id="55640-183">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="55640-184">Wenn ein Wert für angegeben wird, für den aber kein Wert angegeben ist, wird standardmäßig `Role` das aktuelle Abonnement `Scope` `Scope` verwendet.</span><span class="sxs-lookup"><span data-stu-id="55640-184">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="55640-185">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="55640-185">-SkipAssignment</span></span>
<span data-ttu-id="55640-186">Wenn dies festgelegt ist, wird die Erstellung der Standardrollezuweisung für den Dienstprinzipal übersprungen.</span><span class="sxs-lookup"><span data-stu-id="55640-186">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="55640-187">-StartDate</span><span class="sxs-lookup"><span data-stu-id="55640-187">-StartDate</span></span>
<span data-ttu-id="55640-188">Das Effektive Startdatum der Verwendung der Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="55640-188">The effective start date of the credential usage.</span></span>
<span data-ttu-id="55640-189">Der Standardwert für das Startdatum ist "Heute".</span><span class="sxs-lookup"><span data-stu-id="55640-189">The default start date value is today.</span></span> <span data-ttu-id="55640-190">Bei Anmeldeinformationen vom Typ "asymmetrischer Art" muss dies auf das Datum oder nach dem Datum festgelegt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="55640-190">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="55640-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55640-191">-Confirm</span></span>
<span data-ttu-id="55640-192">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55640-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55640-193">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="55640-193">-WhatIf</span></span>
<span data-ttu-id="55640-194">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55640-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55640-195">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55640-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55640-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55640-196">CommonParameters</span></span>
<span data-ttu-id="55640-197">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55640-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55640-198">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55640-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55640-199">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="55640-199">INPUTS</span></span>

### <span data-ttu-id="55640-200">System.Guid</span><span class="sxs-lookup"><span data-stu-id="55640-200">System.Guid</span></span>

### <span data-ttu-id="55640-201">System.String</span><span class="sxs-lookup"><span data-stu-id="55640-201">System.String</span></span>

### <span data-ttu-id="55640-202">Microsoft.Azure.Commands.ActiveDirectory.WERDENDApplication</span><span class="sxs-lookup"><span data-stu-id="55640-202">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="55640-203">Microsoft.Azure.Commands.ActiveDirectory.ODERDPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="55640-203">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="55640-204">Microsoft.Azure.Commands.ActiveDirectory.WERDENDKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="55640-204">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="55640-205">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="55640-205">System.DateTime</span></span>

## <span data-ttu-id="55640-206">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="55640-206">OUTPUTS</span></span>

### <span data-ttu-id="55640-207">Microsoft.Azure.Commands.ActiveDirectory.ODERDServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="55640-207">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="55640-208">Microsoft.Azure.Commands.Resources.Models.Authorization.ODERDServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="55640-208">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="55640-209">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="55640-209">NOTES</span></span>
<span data-ttu-id="55640-210">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="55640-210">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="55640-211">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="55640-211">RELATED LINKS</span></span>

[<span data-ttu-id="55640-212">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="55640-212">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="55640-213">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="55640-213">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="55640-214">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="55640-214">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="55640-215">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="55640-215">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="55640-216">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="55640-216">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="55640-217">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="55640-217">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="55640-218">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="55640-218">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

