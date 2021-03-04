---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
ms.openlocfilehash: 4686941a744532ad8d6f48e079e8120b6d6b3a53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935520"
---
# <span data-ttu-id="1c790-101">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c790-101">Get-AzManagementGroup</span></span>

## <span data-ttu-id="1c790-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c790-102">SYNOPSIS</span></span>
<span data-ttu-id="1c790-103">Ruft Verwaltungsgruppen ab</span><span class="sxs-lookup"><span data-stu-id="1c790-103">Gets Management Group(s)</span></span>

## <span data-ttu-id="1c790-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c790-104">SYNTAX</span></span>

### <span data-ttu-id="1c790-105">ListOperation (Standard)</span><span class="sxs-lookup"><span data-stu-id="1c790-105">ListOperation (Default)</span></span>
```
Get-AzManagementGroup [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c790-106">GetOperation</span><span class="sxs-lookup"><span data-stu-id="1c790-106">GetOperation</span></span>
```
Get-AzManagementGroup [-GroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-Expand] [-Recurse]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c790-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c790-107">DESCRIPTION</span></span>
<span data-ttu-id="1c790-108">Das Get-AzManagementGroup cmdlet Ruft alle oder eine bestimmte Verwaltungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="1c790-108">The Get-AzManagementGroup cmdlet Gets all or a specific Management Group.</span></span>

## <span data-ttu-id="1c790-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1c790-109">EXAMPLES</span></span>

### <span data-ttu-id="1c790-110">Beispiel 1: Alle Verwaltungsgruppen erhalten</span><span class="sxs-lookup"><span data-stu-id="1c790-110">Example 1: Get all Management Groups</span></span>
```
PS C:\> Get-AzManagementGroup

Id          : /providers/Microsoft.Management/managementGroups/TestGroup
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroup
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupDisplayName

Id          : /providers/Microsoft.Management/managementGroups/TestGroupChild
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroupChild
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupChildDisplayName
```

### <span data-ttu-id="1c790-111">Beispiel 2: Erhalten einer bestimmten Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="1c790-111">Example 2: Get specific Management Group</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName TestGroup

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="1c790-112">Beispiel 3: Erhalten einer bestimmten Verwaltungsgruppe und der ersten Hierarchieebene</span><span class="sxs-lookup"><span data-stu-id="1c790-112">Example 3: Get specific Management Group and first level of hierarchy</span></span>
```
PS C:\> $reponse = Get-AzManagementGroup -GroupName TestGroupParent -Expand
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    :
```

<span data-ttu-id="1c790-113">Mit der Kennzeichnung kann man durch das Array `Expand` navigieren und Details für jedes Untergeordnete `Children` erhalten.</span><span class="sxs-lookup"><span data-stu-id="1c790-113">With the `Expand` flag, one can navigate through the `Children` array and get details for each child.</span></span> <span data-ttu-id="1c790-114">Geben Sie beispielsweise `Children[0]` Details für die Gruppe mit dem Anzeigenamen `TestGroup1DisplayName` an.</span><span class="sxs-lookup"><span data-stu-id="1c790-114">For example, `Children[0]` will give details for the group with display name `TestGroup1DisplayName`.</span></span>

### <span data-ttu-id="1c790-115">Beispiel 4: Erhalten einer bestimmten Verwaltungsgruppe und aller Hierarchieebenen</span><span class="sxs-lookup"><span data-stu-id="1c790-115">Example 4: Get specific Management Group and all levels of hierarchy</span></span>
```
PS C:\> $response = Get-AzManagementGroup -GroupName TestGroupParent -Expand -Recurse
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    : {TestRecurseChild}

PS C:\> $response.Children[0].Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestRecurseChild
Name        : TestRecurseChild
DisplayName : TestRecurseChild
Children    :
```

## <span data-ttu-id="1c790-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1c790-116">PARAMETERS</span></span>

### <span data-ttu-id="1c790-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c790-117">-DefaultProfile</span></span>
<span data-ttu-id="1c790-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c790-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c790-119">-Erweitern</span><span class="sxs-lookup"><span data-stu-id="1c790-119">-Expand</span></span>
<span data-ttu-id="1c790-120">Erweitern der Ausgabe, um die Kinder der Verwaltungsgruppe auflisten</span><span class="sxs-lookup"><span data-stu-id="1c790-120">Expand the output to list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c790-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="1c790-121">-GroupName</span></span>
<span data-ttu-id="1c790-122">Verwaltungsgruppen-ID</span><span class="sxs-lookup"><span data-stu-id="1c790-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperation
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c790-123">-Rekursieren</span><span class="sxs-lookup"><span data-stu-id="1c790-123">-Recurse</span></span>
<span data-ttu-id="1c790-124">Rekursiv auflisten der Kinder der Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="1c790-124">Recursively list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c790-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1c790-125">-Confirm</span></span>
<span data-ttu-id="1c790-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c790-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c790-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c790-127">-WhatIf</span></span>
<span data-ttu-id="1c790-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c790-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c790-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c790-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c790-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c790-130">CommonParameters</span></span>
<span data-ttu-id="1c790-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c790-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c790-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c790-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c790-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1c790-133">INPUTS</span></span>

### <span data-ttu-id="1c790-134">Keine</span><span class="sxs-lookup"><span data-stu-id="1c790-134">None</span></span>

## <span data-ttu-id="1c790-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1c790-135">OUTPUTS</span></span>

### <span data-ttu-id="1c790-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span><span class="sxs-lookup"><span data-stu-id="1c790-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span></span>

### <span data-ttu-id="1c790-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c790-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="1c790-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1c790-138">NOTES</span></span>

## <span data-ttu-id="1c790-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1c790-139">RELATED LINKS</span></span>
