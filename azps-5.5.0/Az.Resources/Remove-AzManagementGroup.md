---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: ce2ccd21d7adecdf9602d29837295ad2ca65c952
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169105"
---
# <span data-ttu-id="5be0b-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5be0b-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="5be0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5be0b-102">SYNOPSIS</span></span>
<span data-ttu-id="5be0b-103">Entfernt eine Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5be0b-103">Removes a Management Group</span></span>

## <span data-ttu-id="5be0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5be0b-104">SYNTAX</span></span>

### <span data-ttu-id="5be0b-105">GroupOperations (Standard)</span><span class="sxs-lookup"><span data-stu-id="5be0b-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5be0b-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="5be0b-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5be0b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5be0b-107">DESCRIPTION</span></span>
<span data-ttu-id="5be0b-108">Das **Cmdlet "Remove-AzManagementGroup"** löscht eine Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="5be0b-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="5be0b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5be0b-109">EXAMPLES</span></span>

### <span data-ttu-id="5be0b-110">Beispiel 1: Entfernen einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5be0b-110">Example 1: Remove a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="5be0b-111">Beispiel 2: Entfernen einer Verwaltungsgruppe durch Hinzufügen eines PSManagementGroup-Objekts</span><span class="sxs-lookup"><span data-stu-id="5be0b-111">Example 2: Remove a Management Group by piping PSManagementGroup Object</span></span>
```powershell
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="5be0b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5be0b-112">PARAMETERS</span></span>

### <span data-ttu-id="5be0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5be0b-113">-DefaultProfile</span></span>
<span data-ttu-id="5be0b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5be0b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5be0b-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="5be0b-115">-GroupName</span></span>
<span data-ttu-id="5be0b-116">Management Group Id</span><span class="sxs-lookup"><span data-stu-id="5be0b-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5be0b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5be0b-117">-InputObject</span></span>
<span data-ttu-id="5be0b-118">Eingabeobjekt aus dem Aufruf von "Get"</span><span class="sxs-lookup"><span data-stu-id="5be0b-118">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5be0b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5be0b-119">-PassThru</span></span>
<span data-ttu-id="5be0b-120">Rückgabe `true` bei erfolgreicher Ausführung</span><span class="sxs-lookup"><span data-stu-id="5be0b-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="5be0b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5be0b-121">-Confirm</span></span>
<span data-ttu-id="5be0b-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5be0b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5be0b-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5be0b-123">-WhatIf</span></span>
<span data-ttu-id="5be0b-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5be0b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5be0b-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5be0b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5be0b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5be0b-126">CommonParameters</span></span>
<span data-ttu-id="5be0b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5be0b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5be0b-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5be0b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5be0b-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5be0b-129">INPUTS</span></span>

### <span data-ttu-id="5be0b-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5be0b-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="5be0b-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5be0b-131">OUTPUTS</span></span>

### <span data-ttu-id="5be0b-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5be0b-132">System.Boolean</span></span>

## <span data-ttu-id="5be0b-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5be0b-133">NOTES</span></span>

## <span data-ttu-id="5be0b-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5be0b-134">RELATED LINKS</span></span>
