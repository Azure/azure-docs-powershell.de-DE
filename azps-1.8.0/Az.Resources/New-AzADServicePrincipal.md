---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 9db3e3d0fcb52869a53b4bd2b76603d2935c4dd0
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/05/2020
ms.locfileid: "93665450"
---
# <span data-ttu-id="d4d8e-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d4d8e-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="d4d8e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4d8e-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d8e-103">Erstellt einen neuen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="d4d8e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4d8e-104">SYNTAX</span></span>

### <span data-ttu-id="d4d8e-105">SimpleParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d8e-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d8e-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4d8e-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d8e-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d8e-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d8e-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d8e-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d8e-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d8e-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d8e-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d8e-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d8e-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4d8e-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d8e-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d8e-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d8e-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d8e-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d8e-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d8e-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d8e-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d8e-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d8e-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d8e-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d8e-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d8e-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d8e-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d8e-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d8e-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d8e-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d8e-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4d8e-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4d8e-121">DESCRIPTION</span></span>
<span data-ttu-id="d4d8e-122">Erstellt einen neuen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="d4d8e-123">Der Standardparametersatz verwendet Standardwerte für Parameter, wenn der Benutzer keine für Sie bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="d4d8e-124">Weitere Informationen zu den verwendeten Standardwerten finden Sie unten in der Beschreibung der angegebenen Parameter.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="d4d8e-125">Dieses Cmdlet hat die Möglichkeit, dem Dienstprinzipal eine Rolle mit den `Role` und-Parametern zuzuweisen `Scope` , wenn keiner dieser Parameter angegeben wird, wird dem Dienstprinzipal keine Rolle zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="d4d8e-126">Die Standardwerte für die `Role` und- `Scope` Parameter sind "Mitwirkender" und das aktuelle Abonnement ( _Hinweis_ : die Standardwerte werden nur verwendet, wenn der Benutzer einen Wert für einen der beiden Parameter bereitstellt, aber nicht für den anderen).</span><span class="sxs-lookup"><span data-stu-id="d4d8e-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="d4d8e-127">Das Cmdlet erstellt auch implizit eine Anwendung und legt deren Eigenschaften fest (wenn die ApplicationId nicht bereitgestellt wird).</span><span class="sxs-lookup"><span data-stu-id="d4d8e-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="d4d8e-128">Verwenden Sie Set-AzADApplication-Cmdlet, um die anwendungsspezifischen Parameter zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-128">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="d4d8e-129">Wenn Sie einen Dienstprinzipal mithilfe des Befehls **New-AzADServicePrincipal** erstellen, enthält die Ausgabe Anmeldeinformationen, die Sie schützen müssen.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="d4d8e-130">Stellen Sie sicher, dass Sie diese Anmeldeinformationen nicht in Ihren Code einbeziehen, oder überprüfen Sie die Anmeldeinformationen in die Quellcodeverwaltung.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="d4d8e-131">Als Alternative empfiehlt es sich, [verwaltete Identitäten](/azure/active-directory/managed-identities-azure-resources/overview) zu verwenden, um die Verwendung von Anmeldeinformationen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="d4d8e-132">Standardmäßig weist **New-AzADServicePrincipal** dem Dienstprinzipal im Abonnement Bereich die Rolle [Contributor](/azure/role-based-access-control/built-in-roles#contributor) zu.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="d4d8e-133">Um das Risiko eines kompromittierten Dienst Prinzipals zu verringern, weisen Sie eine spezifischere Rolle zu, und schränken Sie den Bereich auf eine Ressource oder eine Ressourcengruppe ein.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="d4d8e-134">Weitere Informationen finden Sie unter [Schritte zum Hinzufügen einer Rollenzuweisung](/azure/role-based-access-control/role-assignments-steps) .</span><span class="sxs-lookup"><span data-stu-id="d4d8e-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="d4d8e-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4d8e-135">EXAMPLES</span></span>

### <span data-ttu-id="d4d8e-136">Beispiel 1 – Erstellen von einfachen AD-Dienst Prinzipalen</span><span class="sxs-lookup"><span data-stu-id="d4d8e-136">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="d4d8e-137">Der obige Befehl erstellt einen Anzeigendienst Prinzipal, wobei Standardwerte für nicht bereitgestellte Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-137">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="d4d8e-138">Da keine Anwendungs-ID bereitgestellt wurde, wurde eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-138">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="d4d8e-139">Da keine Werte für angegeben wurden `Role` oder hat `Scope` der erstellte Dienstprinzipal keine Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-139">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="d4d8e-140">Beispiel 2 – Erstellen einer einfachen AD-Dienstprinzipal Erstellung mit einer angegebenen Rolle und einem Standardbereich</span><span class="sxs-lookup"><span data-stu-id="d4d8e-140">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

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

<span data-ttu-id="d4d8e-141">Der obige Befehl erstellt einen Anzeigendienst Prinzipal, wobei die Standardwerte für nicht bereitgestellte Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-141">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="d4d8e-142">Da die Anwendungs-ID nicht angegeben wurde, wurde eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-142">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="d4d8e-143">Der Dienstprinzipal wurde mit "Reader"-Berechtigungen für das aktuelle Abonnement erstellt (da für den Parameter kein Wert angegeben wurde `Scope` ).</span><span class="sxs-lookup"><span data-stu-id="d4d8e-143">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="d4d8e-144">Beispiel 3 – Erstellen eines einfachen AD-Dienst Prinzipals mit einem angegebenen Bereich und einer Standardrolle</span><span class="sxs-lookup"><span data-stu-id="d4d8e-144">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

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

<span data-ttu-id="d4d8e-145">Der obige Befehl erstellt einen Anzeigendienst Prinzipal, wobei die Standardwerte für nicht bereitgestellte Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-145">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="d4d8e-146">Da die Anwendungs-ID nicht angegeben wurde, wurde eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-146">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="d4d8e-147">Der Dienstprinzipal wurde mit "Mitwirkenden"-Berechtigungen erstellt (da für den Parameter kein Wert angegeben wurde `Role` ) über den bereitgestellten Ressourcengruppen Bereich.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-147">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="d4d8e-148">Beispiel 4 – Erstellen eines einfachen AD-Dienst Prinzipals mit einem angegebenen Bereich und einer bestimmten Rolle</span><span class="sxs-lookup"><span data-stu-id="d4d8e-148">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

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

<span data-ttu-id="d4d8e-149">Der obige Befehl erstellt einen Anzeigendienst Prinzipal, wobei die Standardwerte für nicht bereitgestellte Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-149">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="d4d8e-150">Da die Anwendungs-ID nicht angegeben wurde, wurde eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-150">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="d4d8e-151">Der Dienstprinzipal wurde mit "Leser"-Berechtigungen für den bereitgestellten Ressourcengruppen Bereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-151">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="d4d8e-152">Beispiel 5 – Erstellen eines neuen Anzeigendienst Prinzipals mithilfe der Anwendungs-ID mit Rollenzuweisung</span><span class="sxs-lookup"><span data-stu-id="d4d8e-152">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="d4d8e-153">Erstellt einen neuen Anzeigendienst Prinzipal für die Anwendung mit der Anwendungs-ID "34a28ad2-DEC4-4a41-bc3b-d22ddf90000e".</span><span class="sxs-lookup"><span data-stu-id="d4d8e-153">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="d4d8e-154">Da keine Werte für angegeben wurden `Role` oder hat `Scope` der erstellte Dienstprinzipal keine Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-154">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="d4d8e-155">Beispiel 6: Erstellen eines neuen AD-Dienst Prinzipals mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="d4d8e-155">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="d4d8e-156">Ruft die Anwendung mit der Objekt-ID "3ede3c26-b443-4e0b-9efc-b05e68338dc3" und Pipes ab, die zum Cmdlet New-AzADServicePrincipal, um einen neuen AD-Dienstprinzipal für diese Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-156">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="d4d8e-157">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4d8e-157">PARAMETERS</span></span>

### <span data-ttu-id="d4d8e-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d4d8e-158">-ApplicationId</span></span>
<span data-ttu-id="d4d8e-159">Die eindeutige Anwendungs-ID für einen Dienstprinzipal in einem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-159">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="d4d8e-160">Nach der Erstellung kann diese Eigenschaft nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-160">Once created this property cannot be changed.</span></span>
<span data-ttu-id="d4d8e-161">Wenn keine Anwendungs-ID angegeben wird, wird eine Anwendung generiert.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-161">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="d4d8e-162">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="d4d8e-162">-ApplicationObject</span></span>
<span data-ttu-id="d4d8e-163">Das Objekt, das die Anwendung darstellt, für die der Dienstprinzipal erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-163">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="d4d8e-164">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="d4d8e-164">-CertValue</span></span>
<span data-ttu-id="d4d8e-165">Der Wert des Anmeldeinformationstyps "asymmetrisch".</span><span class="sxs-lookup"><span data-stu-id="d4d8e-165">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="d4d8e-166">Es stellt das Basis 64-codierte Zertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-166">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="d4d8e-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4d8e-167">-DefaultProfile</span></span>
<span data-ttu-id="d4d8e-168">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d4d8e-168">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4d8e-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d4d8e-169">-DisplayName</span></span>
<span data-ttu-id="d4d8e-170">Der Anzeigename des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-170">The friendly name of the service principal.</span></span> <span data-ttu-id="d4d8e-171">Wenn kein Anzeigename angegeben wird, wird dieser Wert standardmäßig auf "Azure-PowerShell-mm-tt-yyyy-hh-mm-ss" gesetzt, wobei das Suffix der Zeitpunkt der Anwendungserstellung ist.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-171">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="d4d8e-172">-Enddate</span><span class="sxs-lookup"><span data-stu-id="d4d8e-172">-EndDate</span></span>
<span data-ttu-id="d4d8e-173">Das effektive Enddatum der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-173">The effective end date of the credential usage.</span></span>
<span data-ttu-id="d4d8e-174">Der Standardwert für Enddatum beträgt ein Jahr ab heute.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-174">The default end date value is one year from today.</span></span> <span data-ttu-id="d4d8e-175">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder vor dem Datum festgesetzt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-175">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="d4d8e-176">-Keycredential</span><span class="sxs-lookup"><span data-stu-id="d4d8e-176">-KeyCredential</span></span>
<span data-ttu-id="d4d8e-177">Die Sammlung der wichtigen Anmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-177">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="d4d8e-178">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="d4d8e-178">-PasswordCredential</span></span>
<span data-ttu-id="d4d8e-179">Die Sammlung der Kennwortanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-179">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="d4d8e-180">-Role</span><span class="sxs-lookup"><span data-stu-id="d4d8e-180">-Role</span></span>
<span data-ttu-id="d4d8e-181">Die Rolle, die der Dienstprinzipal über den Bereich hat.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-181">The role that the service principal has over the scope.</span></span> <span data-ttu-id="d4d8e-182">Wenn ein Wert für `Scope` angegeben ist, aber kein Wert angegeben wird `Role` , `Role` wird standardmäßig die Rolle "Mitwirkender" verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-182">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="d4d8e-183">-Scope</span><span class="sxs-lookup"><span data-stu-id="d4d8e-183">-Scope</span></span>
<span data-ttu-id="d4d8e-184">Der Bereich, für den der Dienstprinzipal Berechtigungen besitzt.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-184">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="d4d8e-185">Wenn ein Wert für `Role` angegeben ist, aber kein Wert angegeben wird `Scope` , `Scope` wird standardmäßig das aktuelle Abonnement verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-185">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="d4d8e-186">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="d4d8e-186">-SkipAssignment</span></span>
<span data-ttu-id="d4d8e-187">Wenn diese Einstellung aktiviert ist, wird das Erstellen der Standardrollenzuweisung für den Dienstprinzipal übersprungen.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-187">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="d4d8e-188">-StartDate</span><span class="sxs-lookup"><span data-stu-id="d4d8e-188">-StartDate</span></span>
<span data-ttu-id="d4d8e-189">Der effektive Anfangstermin der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-189">The effective start date of the credential usage.</span></span>
<span data-ttu-id="d4d8e-190">Der Standardwert für das Anfangsdatum ist heute.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-190">The default start date value is today.</span></span> <span data-ttu-id="d4d8e-191">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder nach dem Datum festgesetzt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-191">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="d4d8e-192">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4d8e-192">-Confirm</span></span>
<span data-ttu-id="d4d8e-193">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4d8e-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4d8e-194">-WhatIf</span></span>
<span data-ttu-id="d4d8e-195">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-195">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4d8e-196">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4d8e-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d8e-197">CommonParameters</span></span>
<span data-ttu-id="d4d8e-198">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d8e-199">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4d8e-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d8e-200">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4d8e-200">INPUTS</span></span>

### <span data-ttu-id="d4d8e-201">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d4d8e-201">System.Guid</span></span>

### <span data-ttu-id="d4d8e-202">System. String</span><span class="sxs-lookup"><span data-stu-id="d4d8e-202">System.String</span></span>

### <span data-ttu-id="d4d8e-203">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="d4d8e-203">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="d4d8e-204">Microsoft. Azure. Commands. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="d4d8e-204">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="d4d8e-205">Microsoft. Azure. Commands. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="d4d8e-205">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="d4d8e-206">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="d4d8e-206">System.DateTime</span></span>

## <span data-ttu-id="d4d8e-207">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4d8e-207">OUTPUTS</span></span>

### <span data-ttu-id="d4d8e-208">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d4d8e-208">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="d4d8e-209">Microsoft. Azure. Commands. resources. Models. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="d4d8e-209">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="d4d8e-210">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4d8e-210">NOTES</span></span>
<span data-ttu-id="d4d8e-211">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="d4d8e-211">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d4d8e-212">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4d8e-212">RELATED LINKS</span></span>

[<span data-ttu-id="d4d8e-213">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d4d8e-213">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="d4d8e-214">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d4d8e-214">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="d4d8e-215">Neu – AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d4d8e-215">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="d4d8e-216">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d4d8e-216">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="d4d8e-217">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d4d8e-217">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="d4d8e-218">Neu – AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d4d8e-218">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="d4d8e-219">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d4d8e-219">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

