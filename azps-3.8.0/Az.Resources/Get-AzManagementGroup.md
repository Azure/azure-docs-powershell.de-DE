---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
ms.openlocfilehash: 9f06901a9b2a5d476d4c4a3f8365132b8fc223ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846787"
---
# <span data-ttu-id="e8b49-101">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e8b49-101">Get-AzManagementGroup</span></span>

## <span data-ttu-id="e8b49-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8b49-102">SYNOPSIS</span></span>
<span data-ttu-id="e8b49-103">Ruft Verwaltungsgruppe (n) ab.</span><span class="sxs-lookup"><span data-stu-id="e8b49-103">Gets Management Group(s)</span></span>

## <span data-ttu-id="e8b49-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8b49-104">SYNTAX</span></span>

### <span data-ttu-id="e8b49-105">ListOperation (Standard)</span><span class="sxs-lookup"><span data-stu-id="e8b49-105">ListOperation (Default)</span></span>
```
Get-AzManagementGroup [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8b49-106">Getoperation</span><span class="sxs-lookup"><span data-stu-id="e8b49-106">GetOperation</span></span>
```
Get-AzManagementGroup [-GroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-Expand] [-Recurse]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8b49-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8b49-107">DESCRIPTION</span></span>
<span data-ttu-id="e8b49-108">Das Get-AzManagementGroup-Cmdlet ruft alle oder eine bestimmte Verwaltungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e8b49-108">The Get-AzManagementGroup cmdlet Gets all or a specific Management Group.</span></span>

## <span data-ttu-id="e8b49-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8b49-109">EXAMPLES</span></span>

### <span data-ttu-id="e8b49-110">Beispiel 1: Abrufen aller Verwaltungsgruppen</span><span class="sxs-lookup"><span data-stu-id="e8b49-110">Example 1: Get all Management Groups</span></span>
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

### <span data-ttu-id="e8b49-111">Beispiel 2: Abrufen einer bestimmten Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="e8b49-111">Example 2: Get specific Management Group</span></span>
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

### <span data-ttu-id="e8b49-112">Beispiel 3: Abrufen einer bestimmten Verwaltungsgruppe und der ersten Hierarchieebene</span><span class="sxs-lookup"><span data-stu-id="e8b49-112">Example 3: Get specific Management Group and first level of hierarchy</span></span>
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

<span data-ttu-id="e8b49-113">Mit dem `Expand` Flag kann man durch das Array navigieren `Children` und Details für jedes Kind abrufen.</span><span class="sxs-lookup"><span data-stu-id="e8b49-113">With the `Expand` flag, one can navigate through the `Children` array and get details for each child.</span></span> <span data-ttu-id="e8b49-114">Gibt beispielsweise `Children[0]` Details für die Gruppe mit dem Anzeigenamen an `TestGroup1DisplayName` .</span><span class="sxs-lookup"><span data-stu-id="e8b49-114">For example, `Children[0]` will give details for the group with display name `TestGroup1DisplayName`.</span></span>

### <span data-ttu-id="e8b49-115">Beispiel 4: Abrufen einer bestimmten Verwaltungsgruppe und aller Hierarchieebenen</span><span class="sxs-lookup"><span data-stu-id="e8b49-115">Example 4: Get specific Management Group and all levels of hierarchy</span></span>
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

## <span data-ttu-id="e8b49-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8b49-116">PARAMETERS</span></span>

### <span data-ttu-id="e8b49-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8b49-117">-DefaultProfile</span></span>
<span data-ttu-id="e8b49-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e8b49-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8b49-119">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="e8b49-119">-Expand</span></span>
<span data-ttu-id="e8b49-120">Erweitern der Ausgabe, um die untergeordneten Elemente der Verwaltungsgruppe aufzulisten</span><span class="sxs-lookup"><span data-stu-id="e8b49-120">Expand the output to list the children of the management group</span></span>

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

### <span data-ttu-id="e8b49-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="e8b49-121">-GroupName</span></span>
<span data-ttu-id="e8b49-122">Verwaltungsgruppen-ID</span><span class="sxs-lookup"><span data-stu-id="e8b49-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b49-123">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="e8b49-123">-Recurse</span></span>
<span data-ttu-id="e8b49-124">Rekursives Auflisten der untergeordneten Elemente der Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="e8b49-124">Recursively list the children of the management group</span></span>

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

### <span data-ttu-id="e8b49-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e8b49-125">-Confirm</span></span>
<span data-ttu-id="e8b49-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e8b49-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8b49-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8b49-127">-WhatIf</span></span>
<span data-ttu-id="e8b49-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8b49-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8b49-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8b49-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8b49-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8b49-130">CommonParameters</span></span>
<span data-ttu-id="e8b49-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8b49-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8b49-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8b49-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8b49-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8b49-133">INPUTS</span></span>

### <span data-ttu-id="e8b49-134">Keine</span><span class="sxs-lookup"><span data-stu-id="e8b49-134">None</span></span>

## <span data-ttu-id="e8b49-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8b49-135">OUTPUTS</span></span>

### <span data-ttu-id="e8b49-136">Microsoft. Azure. Commands. resources. Models. ManagementGroups. PSManagementGroupInfo</span><span class="sxs-lookup"><span data-stu-id="e8b49-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span></span>

### <span data-ttu-id="e8b49-137">Microsoft. Azure. Commands. resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e8b49-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="e8b49-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8b49-138">NOTES</span></span>

## <span data-ttu-id="e8b49-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8b49-139">RELATED LINKS</span></span>
