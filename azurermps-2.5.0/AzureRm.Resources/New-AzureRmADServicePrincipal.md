---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 9d0fb4f188b3753e22258a27cf8632d85fe866dc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850288"
---
# <span data-ttu-id="2cdb9-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2cdb9-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="2cdb9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2cdb9-102">SYNOPSIS</span></span>
<span data-ttu-id="2cdb9-103">Erstellt einen neuen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cdb9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cdb9-104">SYNTAX</span></span>

### <span data-ttu-id="2cdb9-105">SimpleParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2cdb9-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cdb9-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cdb9-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cdb9-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cdb9-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cdb9-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cdb9-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cdb9-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cdb9-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cdb9-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cdb9-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cdb9-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cdb9-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cdb9-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cdb9-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cdb9-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cdb9-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cdb9-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cdb9-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cdb9-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cdb9-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cdb9-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cdb9-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cdb9-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cdb9-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2cdb9-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cdb9-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication>
 -PasswordCredential <PSADPasswordCredential[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2cdb9-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cdb9-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cdb9-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cdb9-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cdb9-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2cdb9-121">DESCRIPTION</span></span>
<span data-ttu-id="2cdb9-122">Erstellt einen neuen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="2cdb9-123">Der Standardparametersatz verwendet Standardwerte für Parameter, wenn der Benutzer keine für Sie bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="2cdb9-124">Weitere Informationen zu den verwendeten Standardwerten finden Sie unten in der Beschreibung der angegebenen Parameter.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="2cdb9-125">Dieses Cmdlet hat die Möglichkeit, dem Dienstprinzipal eine Rolle mit den `Role` und-Parametern zuzuweisen `Scope` , wenn keiner dieser Parameter angegeben wird, wird dem Dienstprinzipal keine Rolle zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="2cdb9-126">Die Standardwerte für die `Role` und- `Scope` Parameter sind "Mitwirkender" und das aktuelle Abonnement ( _Hinweis_ : die Standardwerte werden nur verwendet, wenn der Benutzer einen Wert für einen der beiden Parameter bereitstellt, aber nicht für den anderen).</span><span class="sxs-lookup"><span data-stu-id="2cdb9-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="2cdb9-127">Das Cmdlet erstellt auch implizit eine Anwendung und legt deren Eigenschaften fest (wenn die ApplicationId nicht bereitgestellt wird).</span><span class="sxs-lookup"><span data-stu-id="2cdb9-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="2cdb9-128">Verwenden Sie Set-AzureRmADApplication-Cmdlet, um die anwendungsspezifischen Parameter zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-128">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="2cdb9-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2cdb9-129">EXAMPLES</span></span>

### <span data-ttu-id="2cdb9-130">Beispiel 1 – Erstellen von einfachen AD-Dienst Prinzipalen</span><span class="sxs-lookup"><span data-stu-id="2cdb9-130">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzureRmADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="2cdb9-131">Der obige Befehl erstellt einen Anzeigendienst Prinzipal, wobei Standardwerte für nicht bereitgestellte Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-131">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="2cdb9-132">Da keine Anwendungs-ID bereitgestellt wurde, wurde eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-132">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="2cdb9-133">Da keine Werte für angegeben wurden `Role` oder hat `Scope` der erstellte Dienstprinzipal keine Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-133">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="2cdb9-134">Beispiel 2 – Erstellen einer einfachen AD-Dienstprinzipal Erstellung mit einer angegebenen Rolle und einem Standardbereich</span><span class="sxs-lookup"><span data-stu-id="2cdb9-134">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="2cdb9-135">Der obige Befehl erstellt einen Anzeigendienst Prinzipal, wobei die Standardwerte für nicht bereitgestellte Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-135">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="2cdb9-136">Da die Anwendungs-ID nicht angegeben wurde, wurde eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-136">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="2cdb9-137">Der Dienstprinzipal wurde mit "Reader"-Berechtigungen für das aktuelle Abonnement erstellt (da für den Parameter kein Wert angegeben wurde `Scope` ).</span><span class="sxs-lookup"><span data-stu-id="2cdb9-137">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="2cdb9-138">Beispiel 3 – Erstellen eines einfachen AD-Dienst Prinzipals mit einem angegebenen Bereich und einer Standardrolle</span><span class="sxs-lookup"><span data-stu-id="2cdb9-138">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="2cdb9-139">Der obige Befehl erstellt einen Anzeigendienst Prinzipal, wobei die Standardwerte für nicht bereitgestellte Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-139">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="2cdb9-140">Da die Anwendungs-ID nicht angegeben wurde, wurde eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-140">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="2cdb9-141">Der Dienstprinzipal wurde mit "Mitwirkenden"-Berechtigungen erstellt (da für den Parameter kein Wert angegeben wurde `Role` ) über den bereitgestellten Ressourcengruppen Bereich.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-141">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="2cdb9-142">Beispiel 4 – Erstellen eines einfachen AD-Dienst Prinzipals mit einem angegebenen Bereich und einer bestimmten Rolle</span><span class="sxs-lookup"><span data-stu-id="2cdb9-142">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="2cdb9-143">Der obige Befehl erstellt einen Anzeigendienst Prinzipal, wobei die Standardwerte für nicht bereitgestellte Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-143">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="2cdb9-144">Da die Anwendungs-ID nicht angegeben wurde, wurde eine Anwendung für den Dienstprinzipal erstellt.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-144">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="2cdb9-145">Der Dienstprinzipal wurde mit "Leser"-Berechtigungen für den bereitgestellten Ressourcengruppen Bereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-145">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="2cdb9-146">Beispiel 5 – Erstellen eines neuen Anzeigendienst Prinzipals mithilfe der Anwendungs-ID mit Rollenzuweisung</span><span class="sxs-lookup"><span data-stu-id="2cdb9-146">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="2cdb9-147">Erstellt einen neuen Anzeigendienst Prinzipal für die Anwendung mit der Anwendungs-ID "34a28ad2-DEC4-4a41-bc3b-d22ddf90000e".</span><span class="sxs-lookup"><span data-stu-id="2cdb9-147">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="2cdb9-148">Da keine Werte für angegeben wurden `Role` oder hat `Scope` der erstellte Dienstprinzipal keine Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-148">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="2cdb9-149">Beispiel 6: Erstellen eines neuen AD-Dienst Prinzipals mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="2cdb9-149">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzureRmADServicePrincipal
```

<span data-ttu-id="2cdb9-150">Ruft die Anwendung mit der Objekt-ID "3ede3c26-b443-4e0b-9efc-b05e68338dc3" und Pipes ab, die zum Cmdlet New-AzureRmADServicePrincipal, um einen neuen AD-Dienstprinzipal für diese Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-150">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzureRmADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="2cdb9-151">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cdb9-151">PARAMETERS</span></span>

### <span data-ttu-id="2cdb9-152">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2cdb9-152">-ApplicationId</span></span>
<span data-ttu-id="2cdb9-153">Die eindeutige Anwendungs-ID für einen Dienstprinzipal in einem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-153">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="2cdb9-154">Nach der Erstellung kann diese Eigenschaft nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-154">Once created this property cannot be changed.</span></span>
<span data-ttu-id="2cdb9-155">Wenn keine Anwendungs-ID angegeben wird, wird eine Anwendung generiert.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-155">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="2cdb9-156">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="2cdb9-156">-ApplicationObject</span></span>
<span data-ttu-id="2cdb9-157">Das Objekt, das die Anwendung darstellt, für die der Dienstprinzipal erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-157">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="2cdb9-158">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="2cdb9-158">-CertValue</span></span>
<span data-ttu-id="2cdb9-159">Der Wert des Anmeldeinformationstyps "asymmetrisch".</span><span class="sxs-lookup"><span data-stu-id="2cdb9-159">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="2cdb9-160">Es stellt das Basis 64-codierte Zertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-160">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="2cdb9-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cdb9-161">-DefaultProfile</span></span>
<span data-ttu-id="2cdb9-162">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2cdb9-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cdb9-163">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2cdb9-163">-DisplayName</span></span>
<span data-ttu-id="2cdb9-164">Der Anzeigename des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-164">The friendly name of the service principal.</span></span> <span data-ttu-id="2cdb9-165">Wenn kein Anzeigename angegeben wird, wird dieser Wert standardmäßig auf "Azure-PowerShell-mm-tt-yyyy-hh-mm-ss" gesetzt, wobei das Suffix der Zeitpunkt der Anwendungserstellung ist.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-165">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="2cdb9-166">-Enddate</span><span class="sxs-lookup"><span data-stu-id="2cdb9-166">-EndDate</span></span>
<span data-ttu-id="2cdb9-167">Das effektive Enddatum der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-167">The effective end date of the credential usage.</span></span>
<span data-ttu-id="2cdb9-168">Der Standardwert für Enddatum beträgt ein Jahr ab heute.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-168">The default end date value is one year from today.</span></span> <span data-ttu-id="2cdb9-169">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder vor dem Datum festgesetzt werden, an dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-169">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="2cdb9-170">-Keycredential</span><span class="sxs-lookup"><span data-stu-id="2cdb9-170">-KeyCredential</span></span>
<span data-ttu-id="2cdb9-171">Die Sammlung der wichtigen Anmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-171">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="2cdb9-172">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="2cdb9-172">-Password</span></span>
<span data-ttu-id="2cdb9-173">Das Kennwort, das dem Dienstprinzipal zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-173">The password to be associated with the service principal.</span></span> <span data-ttu-id="2cdb9-174">Wenn kein Kennwort angegeben wird, wird eine zufällige GUID generiert und als Kennwort verwendet.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-174">If a password is not provided, a random GUID will be generated and used as the password.</span></span>

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

### <span data-ttu-id="2cdb9-175">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="2cdb9-175">-PasswordCredential</span></span>
<span data-ttu-id="2cdb9-176">Die Sammlung der Kennwortanmeldeinformationen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-176">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="2cdb9-177">-Role</span><span class="sxs-lookup"><span data-stu-id="2cdb9-177">-Role</span></span>
<span data-ttu-id="2cdb9-178">Die Rolle, die der Dienstprinzipal über den Bereich hat.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-178">The role that the service principal has over the scope.</span></span> <span data-ttu-id="2cdb9-179">Wenn ein Wert für `Scope` angegeben ist, aber kein Wert angegeben wird `Role` , `Role` wird standardmäßig die Rolle "Mitwirkender" verwendet.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-179">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="2cdb9-180">-Scope</span><span class="sxs-lookup"><span data-stu-id="2cdb9-180">-Scope</span></span>
<span data-ttu-id="2cdb9-181">Der Bereich, für den der Dienstprinzipal Berechtigungen besitzt.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-181">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="2cdb9-182">Wenn ein Wert für `Role` angegeben ist, aber kein Wert angegeben wird `Scope` , `Scope` wird standardmäßig das aktuelle Abonnement verwendet.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-182">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="2cdb9-183">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="2cdb9-183">-SkipAssignment</span></span>
<span data-ttu-id="2cdb9-184">Wenn diese Einstellung aktiviert ist, wird das Erstellen der Standardrollenzuweisung für den Dienstprinzipal übersprungen.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-184">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="2cdb9-185">-StartDate</span><span class="sxs-lookup"><span data-stu-id="2cdb9-185">-StartDate</span></span>
<span data-ttu-id="2cdb9-186">Der effektive Anfangstermin der Anmelde Informationsverwendung.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-186">The effective start date of the credential usage.</span></span>
<span data-ttu-id="2cdb9-187">Der Standardwert für das Anfangsdatum ist heute.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-187">The default start date value is today.</span></span> <span data-ttu-id="2cdb9-188">Bei einer "asymmetrischen" Art von Anmeldeinformationen muss dies auf ein oder nach dem Datum festgesetzt werden, ab dem das X509-Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-188">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="2cdb9-189">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2cdb9-189">-Confirm</span></span>
<span data-ttu-id="2cdb9-190">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cdb9-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cdb9-191">-WhatIf</span></span>
<span data-ttu-id="2cdb9-192">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cdb9-193">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cdb9-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cdb9-194">CommonParameters</span></span>
<span data-ttu-id="2cdb9-195">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cdb9-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cdb9-196">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cdb9-196">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cdb9-197">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2cdb9-197">INPUTS</span></span>

### <span data-ttu-id="2cdb9-198">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2cdb9-198">System.Guid</span></span>

### <span data-ttu-id="2cdb9-199">System. String</span><span class="sxs-lookup"><span data-stu-id="2cdb9-199">System.String</span></span>

### <span data-ttu-id="2cdb9-200">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="2cdb9-200">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="2cdb9-201">Parameter: applicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2cdb9-201">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="2cdb9-202">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="2cdb9-202">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="2cdb9-203">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="2cdb9-203">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="2cdb9-204">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="2cdb9-204">System.Security.SecureString</span></span>

### <span data-ttu-id="2cdb9-205">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="2cdb9-205">System.DateTime</span></span>

## <span data-ttu-id="2cdb9-206">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2cdb9-206">OUTPUTS</span></span>

### <span data-ttu-id="2cdb9-207">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2cdb9-207">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="2cdb9-208">Microsoft. Azure. Commands. resources. Models. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="2cdb9-208">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="2cdb9-209">Notizen</span><span class="sxs-lookup"><span data-stu-id="2cdb9-209">NOTES</span></span>
<span data-ttu-id="2cdb9-210">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="2cdb9-210">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="2cdb9-211">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2cdb9-211">RELATED LINKS</span></span>

[<span data-ttu-id="2cdb9-212">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2cdb9-212">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="2cdb9-213">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2cdb9-213">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="2cdb9-214">Neu – AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="2cdb9-214">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="2cdb9-215">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="2cdb9-215">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="2cdb9-216">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2cdb9-216">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="2cdb9-217">Neu – AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2cdb9-217">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="2cdb9-218">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2cdb9-218">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

