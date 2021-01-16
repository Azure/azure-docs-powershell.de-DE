---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
ms.openlocfilehash: 07272df9b1892373d23b89447f1c21a5a4fb53c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300507"
---
# <span data-ttu-id="083cd-101">New-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="083cd-101">New-AzManagementGroup</span></span>

## <span data-ttu-id="083cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="083cd-102">SYNOPSIS</span></span>
<span data-ttu-id="083cd-103">Erstellt eine Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="083cd-103">Creates a Management Group</span></span>

## <span data-ttu-id="083cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="083cd-104">SYNTAX</span></span>

### <span data-ttu-id="083cd-105">GroupOperations (Standard)</span><span class="sxs-lookup"><span data-stu-id="083cd-105">GroupOperations (Default)</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="083cd-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="083cd-106">ParentGroupObject</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="083cd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="083cd-107">DESCRIPTION</span></span>
<span data-ttu-id="083cd-108">Das **Cmdlet "New-AzManagementGroup"** erstellt eine Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="083cd-108">The **New-AzManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="083cd-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="083cd-109">EXAMPLES</span></span>

### <span data-ttu-id="083cd-110">Beispiel 1: Erstellen einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="083cd-110">Example 1: Create a Management Group</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="083cd-111">Erstellen einer neuen Gruppe mit `DisplayName` und `ParentId` festlegen auf `null`</span><span class="sxs-lookup"><span data-stu-id="083cd-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="083cd-112">Dies ist identisch mit dem übergeordneten Element der Gruppe, und das übergeordnete Element der Gruppe `DisplayName` `GroupName` ist der Mandant.</span><span class="sxs-lookup"><span data-stu-id="083cd-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="083cd-113">Beispiel 2: Erstellen einer Verwaltungsgruppe mit einem Anzeigenamen</span><span class="sxs-lookup"><span data-stu-id="083cd-113">Example 2: Create a Management Group with a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="083cd-114">In diesem Fall ist das übergeordnete Element der Gruppe der Mandant und wird auf `DisplayName` den angegebenen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="083cd-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="083cd-115">Beispiel 3: Erstellen einer Verwaltungsgruppe mit einem übergeordneten Element und einem Anzeigenamen</span><span class="sxs-lookup"><span data-stu-id="083cd-115">Example 3: Create a Management Group with a parent and a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="083cd-116">Beispiel 4: Erstellen einer Verwaltungsgruppe mit einem übergeordneten Element (mithilfe eines übergeordneten Objekts)</span><span class="sxs-lookup"><span data-stu-id="083cd-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

## <span data-ttu-id="083cd-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="083cd-117">PARAMETERS</span></span>

### <span data-ttu-id="083cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="083cd-118">-DefaultProfile</span></span>
<span data-ttu-id="083cd-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="083cd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="083cd-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="083cd-120">-DisplayName</span></span>
<span data-ttu-id="083cd-121">Anzeigename der Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="083cd-121">Display Name of the management group</span></span>

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

### <span data-ttu-id="083cd-122">-GroupName</span><span class="sxs-lookup"><span data-stu-id="083cd-122">-GroupName</span></span>
<span data-ttu-id="083cd-123">Management Group Id</span><span class="sxs-lookup"><span data-stu-id="083cd-123">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083cd-124">-ParentId</span><span class="sxs-lookup"><span data-stu-id="083cd-124">-ParentId</span></span>
<span data-ttu-id="083cd-125">Übergeordnete ID der Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="083cd-125">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083cd-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="083cd-126">-ParentObject</span></span>
<span data-ttu-id="083cd-127">Übergeordnetes Objekt</span><span class="sxs-lookup"><span data-stu-id="083cd-127">Parent Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083cd-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="083cd-128">-Confirm</span></span>
<span data-ttu-id="083cd-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="083cd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="083cd-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="083cd-130">-WhatIf</span></span>
<span data-ttu-id="083cd-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="083cd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="083cd-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="083cd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="083cd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="083cd-133">CommonParameters</span></span>
<span data-ttu-id="083cd-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="083cd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="083cd-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="083cd-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="083cd-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="083cd-136">INPUTS</span></span>

### <span data-ttu-id="083cd-137">Keine</span><span class="sxs-lookup"><span data-stu-id="083cd-137">None</span></span>

## <span data-ttu-id="083cd-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="083cd-138">OUTPUTS</span></span>

### <span data-ttu-id="083cd-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="083cd-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="083cd-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="083cd-140">NOTES</span></span>

## <span data-ttu-id="083cd-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="083cd-141">RELATED LINKS</span></span>

[<span data-ttu-id="083cd-142">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="083cd-142">Remove-AzManagementGroup</span></span>](./Remove-AzManagementGroup.md)

[<span data-ttu-id="083cd-143">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="083cd-143">Update-AzManagementGroup</span></span>](./Update-AzManagementGroup.md)

[<span data-ttu-id="083cd-144">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="083cd-144">Get-AzManagementGroup</span></span>](./Get-AzManagementGroup.md)