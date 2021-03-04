---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: 0e0163fd6a73aaf79e105ba78567d3c4048c9220
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927075"
---
# <span data-ttu-id="93791-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="93791-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="93791-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93791-102">SYNOPSIS</span></span>
<span data-ttu-id="93791-103">Erstellt oder aktualisiert eine Registrierungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="93791-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="93791-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93791-104">SYNTAX</span></span>

### <span data-ttu-id="93791-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="93791-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -PrincipalId <String> -RoleDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93791-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="93791-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> -PlanName <String> -PlanPublisher <String>
 -PlanProduct <String> -PlanVersion <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93791-107">ByAuthorization</span><span class="sxs-lookup"><span data-stu-id="93791-107">ByAuthorization</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93791-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93791-108">DESCRIPTION</span></span>
<span data-ttu-id="93791-109">Erstellt oder aktualisiert eine Registrierungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="93791-109">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="93791-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="93791-110">EXAMPLES</span></span>

### <span data-ttu-id="93791-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="93791-111">Example 1</span></span>
```
PS C:\> New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b732e39c-c034-44cd-b5a1-094669ccc8c5 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/b732e39c-c034-44cd-b5a1-094669ccc8c5 Succeeded


PS C:\>
```

<span data-ttu-id="93791-112">Erstellt eine Registrierungsdefinition nach roleDefinitionId- und principalId-Werten, die direkt angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="93791-112">Creates a registration definition by roleDefinitionId and principalId values given directly.</span></span>

### <span data-ttu-id="93791-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="93791-113">Example 2</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\>
```

<span data-ttu-id="93791-114">Erstellt oder aktualisiert eine Registrierungsdefinition mit Autorisierungsdetails.</span><span class="sxs-lookup"><span data-stu-id="93791-114">Creates or updates a registration definition with authorization details.</span></span>

### <span data-ttu-id="93791-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="93791-115">Example 3</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" },
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "9980e02c-c2be-4d73-94e8-173b1dc7cf3c"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7


PS C:\> $definition.Name
55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths -Name 55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7
714160ec-87d5-42bb-8b17-287c0dd7417d 9980e02c-c2be-4d73-94e8-173b1dc7cf3c

PS C:\>
```

<span data-ttu-id="93791-116">Aktualisiert eine Registrierungsdefinition mit Autorisierungsdetails und Namen der Registrierungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="93791-116">Updates a registration definition with authorization details and name of the registration definition.</span></span>

## <span data-ttu-id="93791-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="93791-117">PARAMETERS</span></span>

### <span data-ttu-id="93791-118">-Autorisierung</span><span class="sxs-lookup"><span data-stu-id="93791-118">-Authorization</span></span>
<span data-ttu-id="93791-119">Die Autorisierungszuordnungsliste mit principalId – roleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="93791-119">The authorization mapping list with principalId - roleDefinitionId.</span></span>

```yaml
Type: Microsoft.Azure.Management.ManagedServices.Models.Authorization[]
Parameter Sets: ByPlan, ByAuthorization
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93791-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93791-120">-DefaultProfile</span></span>
<span data-ttu-id="93791-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93791-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93791-122">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93791-122">-Description</span></span>
<span data-ttu-id="93791-123">Die Beschreibung der Registrierungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="93791-123">The description of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93791-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="93791-124">-DisplayName</span></span>
<span data-ttu-id="93791-125">Der Anzeigename der Registrierungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="93791-125">The display name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93791-126">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="93791-126">-ManagedByTenantId</span></span>
<span data-ttu-id="93791-127">Der ManagedBy-Mandantenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="93791-127">The ManagedBy Tenant Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93791-128">-Name</span><span class="sxs-lookup"><span data-stu-id="93791-128">-Name</span></span>
<span data-ttu-id="93791-129">Der eindeutige Name der Registrierungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="93791-129">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93791-130">-PlanName</span><span class="sxs-lookup"><span data-stu-id="93791-130">-PlanName</span></span>
<span data-ttu-id="93791-131">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="93791-131">The name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93791-132">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="93791-132">-PlanProduct</span></span>
<span data-ttu-id="93791-133">Der Name des Produkts.</span><span class="sxs-lookup"><span data-stu-id="93791-133">The name of the Product.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93791-134">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="93791-134">-PlanPublisher</span></span>
<span data-ttu-id="93791-135">Der Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="93791-135">The name of the Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93791-136">-PlanVersion</span><span class="sxs-lookup"><span data-stu-id="93791-136">-PlanVersion</span></span>
<span data-ttu-id="93791-137">Die Versionsnummer des Plans.</span><span class="sxs-lookup"><span data-stu-id="93791-137">The version number of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93791-138">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="93791-138">-PrincipalId</span></span>
<span data-ttu-id="93791-139">Der ManagedBy Principal Identifier.</span><span class="sxs-lookup"><span data-stu-id="93791-139">The ManagedBy Principal Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93791-140">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="93791-140">-RoleDefinitionId</span></span>
<span data-ttu-id="93791-141">Der Rollendefinitionsbezeichner zum Erteilen von Berechtigungen für den Prinzipalbezeichner.</span><span class="sxs-lookup"><span data-stu-id="93791-141">The role definition identifier to grant permissions to principal identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93791-142">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93791-142">-AsJob</span></span>
<span data-ttu-id="93791-143">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="93791-143">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93791-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="93791-144">-Confirm</span></span>
<span data-ttu-id="93791-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="93791-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93791-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93791-146">-WhatIf</span></span>
<span data-ttu-id="93791-147">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="93791-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93791-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="93791-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93791-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93791-149">CommonParameters</span></span>
<span data-ttu-id="93791-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93791-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93791-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93791-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93791-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="93791-152">INPUTS</span></span>

### <span data-ttu-id="93791-153">Keine</span><span class="sxs-lookup"><span data-stu-id="93791-153">None</span></span>
## <span data-ttu-id="93791-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="93791-154">OUTPUTS</span></span>

### <span data-ttu-id="93791-155">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="93791-155">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="93791-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="93791-156">NOTES</span></span>

## <span data-ttu-id="93791-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="93791-157">RELATED LINKS</span></span>
