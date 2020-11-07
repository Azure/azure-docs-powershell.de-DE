---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: cd4cb9f7137d0e6cdd91222c278b6e59c04d7e3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652351"
---
# <span data-ttu-id="f8f1a-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="f8f1a-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="f8f1a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f1a-103">Besorgen Sie sich eine oder mehrere Blueprint-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="f8f1a-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="f8f1a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8f1a-104">SYNTAX</span></span>

### <span data-ttu-id="f8f1a-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8f1a-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8f1a-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="f8f1a-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8f1a-107">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="f8f1a-107">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8f1a-108">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="f8f1a-108">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8f1a-109">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="f8f1a-109">ManagementGroupScope</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8f1a-110">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="f8f1a-110">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8f1a-111">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="f8f1a-111">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8f1a-112">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="f8f1a-112">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8f1a-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8f1a-113">DESCRIPTION</span></span>
<span data-ttu-id="f8f1a-114">Besorgen Sie sich eine oder mehrere Blueprint-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="f8f1a-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="f8f1a-115">Blueprint-Definitionen sind im Verwaltungsgruppen-oder Abonnement Bereich vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f8f1a-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="f8f1a-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8f1a-116">EXAMPLES</span></span>

### <span data-ttu-id="f8f1a-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8f1a-117">Example 1</span></span>
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

<span data-ttu-id="f8f1a-118">Rufen Sie die Blueprint-Definitionen innerhalb des aktuellen Abonnements und der Verwaltungsgruppen Hierarchie des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="f8f1a-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="f8f1a-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f8f1a-119">Example 2</span></span>
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

<span data-ttu-id="f8f1a-120">Rufen Sie die Blueprint-Definitionen innerhalb der angegebenen Verwaltungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="f8f1a-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="f8f1a-121">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f8f1a-121">Example 3</span></span>
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

<span data-ttu-id="f8f1a-122">Rufen Sie die Blueprint-Definitionen innerhalb des angegebenen Abonnements und der Verwaltungsgruppen Hierarchie des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="f8f1a-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="f8f1a-123">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="f8f1a-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="f8f1a-124">Rufen Sie die Blueprint-Definition mit dem angegebenen Namen innerhalb des angegebenen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="f8f1a-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="f8f1a-125">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="f8f1a-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="f8f1a-126">Rufen Sie die Blueprint-Definition mit dem angegebenen Namen und der Version innerhalb der angegebenen Verwaltungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="f8f1a-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="f8f1a-127">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="f8f1a-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="f8f1a-128">Rufen Sie die neueste veröffentlichte Blueprint-Definition mit dem angegebenen Namen in der angegebenen Verwaltungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="f8f1a-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="f8f1a-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8f1a-129">PARAMETERS</span></span>

### <span data-ttu-id="f8f1a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8f1a-130">-DefaultProfile</span></span>
<span data-ttu-id="f8f1a-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8f1a-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8f1a-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="f8f1a-132">-LatestPublished</span></span>
<span data-ttu-id="f8f1a-133">Das neueste veröffentlichte Blueprint-Definitions Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="f8f1a-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="f8f1a-134">Wenn Sie festzulegen, gibt die Ausführung die neueste veröffentlichte Version der Blueprint-Definition zurück.</span><span class="sxs-lookup"><span data-stu-id="f8f1a-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="f8f1a-135">Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="f8f1a-135">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySubscriptionNameAndLatestPublished, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f1a-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="f8f1a-136">-ManagementGroupId</span></span>
<span data-ttu-id="f8f1a-137">Verwaltungsgruppen-ID, in der die Blueprint-Definition gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f8f1a-137">Management Group Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8f1a-138">-Name</span><span class="sxs-lookup"><span data-stu-id="f8f1a-138">-Name</span></span>
<span data-ttu-id="f8f1a-139">Blueprint-Definitionsname</span><span class="sxs-lookup"><span data-stu-id="f8f1a-139">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8f1a-140">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f8f1a-140">-SubscriptionId</span></span>
<span data-ttu-id="f8f1a-141">Abonnement-ID, in der die Blueprint-Definition gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f8f1a-141">Subscription Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8f1a-142">-Version</span><span class="sxs-lookup"><span data-stu-id="f8f1a-142">-Version</span></span>
<span data-ttu-id="f8f1a-143">Veröffentlichte Blueprint-Definitionsversion.</span><span class="sxs-lookup"><span data-stu-id="f8f1a-143">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionNameAndVersion, ByManagementGroupNameAndVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8f1a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f1a-144">CommonParameters</span></span>
<span data-ttu-id="f8f1a-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8f1a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f1a-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8f1a-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f1a-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8f1a-147">INPUTS</span></span>

### <span data-ttu-id="f8f1a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="f8f1a-148">System.String</span></span>

## <span data-ttu-id="f8f1a-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8f1a-149">OUTPUTS</span></span>

### <span data-ttu-id="f8f1a-150">System. Object</span><span class="sxs-lookup"><span data-stu-id="f8f1a-150">System.Object</span></span>
## <span data-ttu-id="f8f1a-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8f1a-151">NOTES</span></span>

## <span data-ttu-id="f8f1a-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8f1a-152">RELATED LINKS</span></span>
