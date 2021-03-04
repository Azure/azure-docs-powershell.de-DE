---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: 6b646e22ff32d9fe361cdedd6dbb6fa5c9fba270
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948035"
---
# <span data-ttu-id="f74ca-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="f74ca-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="f74ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f74ca-102">SYNOPSIS</span></span>
<span data-ttu-id="f74ca-103">Holen Sie sich eine oder mehrere Blaupausendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f74ca-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="f74ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f74ca-104">SYNTAX</span></span>

### <span data-ttu-id="f74ca-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="f74ca-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f74ca-106">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="f74ca-106">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f74ca-107">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="f74ca-107">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f74ca-108">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="f74ca-108">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f74ca-109">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="f74ca-109">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f74ca-110">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="f74ca-110">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f74ca-111">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="f74ca-111">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f74ca-112">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="f74ca-112">ManagementGroupScope</span></span>
```
Get-AzBlueprint -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f74ca-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f74ca-113">DESCRIPTION</span></span>
<span data-ttu-id="f74ca-114">Holen Sie sich eine oder mehrere Blaupausendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f74ca-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="f74ca-115">Blaupausendefinitionen sind in der Verwaltungsgruppe oder im Abonnementbereich vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f74ca-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="f74ca-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f74ca-116">EXAMPLES</span></span>

### <span data-ttu-id="f74ca-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f74ca-117">Example 1</span></span>
```powershell
PS> Get-AzBlueprint

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
SubscriptionId       : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="f74ca-118">Holen Sie sich die Blaupausendefinitionen innerhalb des aktuellen Abonnements und der Hierarchie der Verwaltungsgruppe des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="f74ca-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="f74ca-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f74ca-119">Example 2</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId"

Name                 : PS-MG-BlueprintDefinition
Id                   : /providers/Microsoft.Management/managementGroups/myManagementGroupId/providers/Microsoft.Blueprint/blueprints/PS-MG-BlueprintDefinition
ManagementGroupId    : myManagementGroupId
Versions             : {1.0, 2.0, 3.0, 4.0}
TimeCreated          : 2019-03-04
TargetScope          : Subscription
Parameters           : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue, [Usergrouporapplicationname]:Contributor_RoleAssignmentName,
                       [Usergrouporapplicationname]:Owner_RoleAssignmentName}
ResourceGroups       : {ResourceGroup, ResourceGroup2}
```

<span data-ttu-id="f74ca-120">Holen Sie sich die Blaupausendefinitionen innerhalb der angegebenen Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f74ca-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="f74ca-121">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f74ca-121">Example 3</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
SubscriptionId       : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="f74ca-122">Holen Sie sich die Blaupausendefinitionen innerhalb des angegebenen Abonnements und der Hierarchie der Verwaltungsgruppe des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="f74ca-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="f74ca-123">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="f74ca-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="f74ca-124">Holen Sie sich die Blaupausendefinition mit dem angegebenen Namen innerhalb des angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="f74ca-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="f74ca-125">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="f74ca-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="f74ca-126">Holen Sie sich die Blaupausendefinition mit dem angegebenen Namen und der angegebenen Version innerhalb der angegebenen Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f74ca-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="f74ca-127">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="f74ca-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="f74ca-128">Holen Sie sich die neueste veröffentlichte Blaupausendefinition mit dem angegebenen Namen innerhalb der angegebenen Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f74ca-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="f74ca-129">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f74ca-129">PARAMETERS</span></span>

### <span data-ttu-id="f74ca-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f74ca-130">-DefaultProfile</span></span>
<span data-ttu-id="f74ca-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f74ca-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f74ca-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="f74ca-132">-LatestPublished</span></span>
<span data-ttu-id="f74ca-133">Die neueste veröffentlichte Blaupausendefinitionsflagge.</span><span class="sxs-lookup"><span data-stu-id="f74ca-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="f74ca-134">Wenn festgelegt, gibt die Ausführung die neueste veröffentlichte Version der Blaupausendefinition zurück.</span><span class="sxs-lookup"><span data-stu-id="f74ca-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="f74ca-135">Standardmäßig ist "false" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f74ca-135">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByManagementGroupNameAndLatestPublished, BySubscriptionNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f74ca-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="f74ca-136">-ManagementGroupId</span></span>
<span data-ttu-id="f74ca-137">Verwaltungsgruppen-ID, in der die Blaupausendefinition gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="f74ca-137">Management Group Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, ByManagementGroupAndName, ByManagementGroupNameAndLatestPublished, ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f74ca-138">-Name</span><span class="sxs-lookup"><span data-stu-id="f74ca-138">-Name</span></span>
<span data-ttu-id="f74ca-139">Name der Blaupausedefinition.</span><span class="sxs-lookup"><span data-stu-id="f74ca-139">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, ByManagementGroupAndName, ByManagementGroupNameAndLatestPublished, BySubscriptionNameAndLatestPublished, BySubscriptionNameAndVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f74ca-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f74ca-140">-SubscriptionId</span></span>
<span data-ttu-id="f74ca-141">Abonnement-ID, in der die Blaupausendefinition gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f74ca-141">Subscription Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndLatestPublished, BySubscriptionNameAndVersion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f74ca-142">-Version</span><span class="sxs-lookup"><span data-stu-id="f74ca-142">-Version</span></span>
<span data-ttu-id="f74ca-143">Veröffentlichte Blaupausendefinitionsversion.</span><span class="sxs-lookup"><span data-stu-id="f74ca-143">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, BySubscriptionNameAndVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f74ca-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f74ca-144">CommonParameters</span></span>
<span data-ttu-id="f74ca-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f74ca-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f74ca-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f74ca-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f74ca-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f74ca-147">INPUTS</span></span>

### <span data-ttu-id="f74ca-148">System.String</span><span class="sxs-lookup"><span data-stu-id="f74ca-148">System.String</span></span>

## <span data-ttu-id="f74ca-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f74ca-149">OUTPUTS</span></span>

### <span data-ttu-id="f74ca-150">System.Object</span><span class="sxs-lookup"><span data-stu-id="f74ca-150">System.Object</span></span>
## <span data-ttu-id="f74ca-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f74ca-151">NOTES</span></span>

## <span data-ttu-id="f74ca-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f74ca-152">RELATED LINKS</span></span>
