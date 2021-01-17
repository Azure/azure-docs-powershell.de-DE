---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: ab383b1fb46759c2369d94d4bb57284ba59cf671
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471044"
---
# <span data-ttu-id="5b47a-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="5b47a-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="5b47a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b47a-102">SYNOPSIS</span></span>
<span data-ttu-id="5b47a-103">Erhalten Sie eine oder mehrere Blaupausendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5b47a-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="5b47a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b47a-104">SYNTAX</span></span>

### <span data-ttu-id="5b47a-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b47a-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b47a-106">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="5b47a-106">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b47a-107">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="5b47a-107">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b47a-108">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="5b47a-108">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b47a-109">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="5b47a-109">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b47a-110">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="5b47a-110">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b47a-111">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="5b47a-111">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b47a-112">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="5b47a-112">ManagementGroupScope</span></span>
```
Get-AzBlueprint -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b47a-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b47a-113">DESCRIPTION</span></span>
<span data-ttu-id="5b47a-114">Erhalten Sie eine oder mehrere Blaupausendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5b47a-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="5b47a-115">Entwurfsdefinitionen sind in der Verwaltungsgruppe oder im Abonnementbereich vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5b47a-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="5b47a-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5b47a-116">EXAMPLES</span></span>

### <span data-ttu-id="5b47a-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5b47a-117">Example 1</span></span>
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

<span data-ttu-id="5b47a-118">Erhalten Sie die Blaupausendefinitionen innerhalb des aktuellen Abonnements und der Verwaltungsgruppenhierarchie des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="5b47a-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="5b47a-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5b47a-119">Example 2</span></span>
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

<span data-ttu-id="5b47a-120">Erhalten Sie die Blaupausendefinitionen innerhalb der angegebenen Managementgruppe.</span><span class="sxs-lookup"><span data-stu-id="5b47a-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="5b47a-121">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5b47a-121">Example 3</span></span>
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

<span data-ttu-id="5b47a-122">Erhalten Sie die Blaupausendefinitionen innerhalb des angegebenen Abonnements und der Verwaltungsgruppenhierarchie des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="5b47a-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="5b47a-123">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="5b47a-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="5b47a-124">Erhalten Sie die Blaupausendefinition mit dem angegebenen Namen innerhalb des angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="5b47a-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="5b47a-125">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="5b47a-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="5b47a-126">Erhalten Sie die Blaupausendefinition mit dem angegebenen Namen und der version innerhalb der angegebenen Managementgruppe.</span><span class="sxs-lookup"><span data-stu-id="5b47a-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="5b47a-127">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="5b47a-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="5b47a-128">Holen Sie sich die neueste veröffentlichte Entwurfsdefinition mit dem angegebenen Namen in der angegebenen Managementgruppe.</span><span class="sxs-lookup"><span data-stu-id="5b47a-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="5b47a-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b47a-129">PARAMETERS</span></span>

### <span data-ttu-id="5b47a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b47a-130">-DefaultProfile</span></span>
<span data-ttu-id="5b47a-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b47a-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b47a-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="5b47a-132">-LatestPublished</span></span>
<span data-ttu-id="5b47a-133">Die neueste veröffentlichte Blaupausendefinitionsflagge.</span><span class="sxs-lookup"><span data-stu-id="5b47a-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="5b47a-134">Wenn dies festgelegt ist, gibt die Ausführung die neueste Version der Blaupausendefinition zurück.</span><span class="sxs-lookup"><span data-stu-id="5b47a-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="5b47a-135">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="5b47a-135">Defaults to false.</span></span>

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

### <span data-ttu-id="5b47a-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="5b47a-136">-ManagementGroupId</span></span>
<span data-ttu-id="5b47a-137">ID der Managementgruppe, in der die Blaupausendefinition gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="5b47a-137">Management Group Id where the blueprint definition is saved.</span></span>

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

### <span data-ttu-id="5b47a-138">-Name</span><span class="sxs-lookup"><span data-stu-id="5b47a-138">-Name</span></span>
<span data-ttu-id="5b47a-139">Name der Blaupause.</span><span class="sxs-lookup"><span data-stu-id="5b47a-139">Blueprint definition name.</span></span>

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

### <span data-ttu-id="5b47a-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b47a-140">-SubscriptionId</span></span>
<span data-ttu-id="5b47a-141">Abonnement-ID, in der die Entwurfsdefinition gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="5b47a-141">Subscription Id where the blueprint definition is saved.</span></span>

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

### <span data-ttu-id="5b47a-142">-Version</span><span class="sxs-lookup"><span data-stu-id="5b47a-142">-Version</span></span>
<span data-ttu-id="5b47a-143">Veröffentlichte Entwurfsdefinitionsversion.</span><span class="sxs-lookup"><span data-stu-id="5b47a-143">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="5b47a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b47a-144">CommonParameters</span></span>
<span data-ttu-id="5b47a-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b47a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b47a-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b47a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b47a-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5b47a-147">INPUTS</span></span>

### <span data-ttu-id="5b47a-148">System.String</span><span class="sxs-lookup"><span data-stu-id="5b47a-148">System.String</span></span>

## <span data-ttu-id="5b47a-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5b47a-149">OUTPUTS</span></span>

### <span data-ttu-id="5b47a-150">System.Object</span><span class="sxs-lookup"><span data-stu-id="5b47a-150">System.Object</span></span>
## <span data-ttu-id="5b47a-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5b47a-151">NOTES</span></span>

## <span data-ttu-id="5b47a-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5b47a-152">RELATED LINKS</span></span>
