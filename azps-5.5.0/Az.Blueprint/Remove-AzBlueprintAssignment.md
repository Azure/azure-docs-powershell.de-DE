---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 40452c250b58edf4d1e45f54c953dee8c433c436
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149169"
---
# <span data-ttu-id="01680-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="01680-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="01680-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01680-102">SYNOPSIS</span></span>
<span data-ttu-id="01680-103">Entfernen Sie eine Blaupausenaufgabe aus einem Abonnement oder einer Managementgruppe.</span><span class="sxs-lookup"><span data-stu-id="01680-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="01680-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01680-104">SYNTAX</span></span>

### <span data-ttu-id="01680-105">BySubscriptionAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="01680-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01680-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="01680-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01680-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="01680-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01680-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01680-108">DESCRIPTION</span></span>
<span data-ttu-id="01680-109">Entfernen Sie eine Blaupause, die einem Abonnement zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="01680-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="01680-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01680-110">EXAMPLES</span></span>

### <span data-ttu-id="01680-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="01680-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="01680-112">Entfernen Sie die mit dem Namen angegebene Blaupausenzuweisung aus dem angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="01680-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="01680-113">Das Cmdlet fordert vor dem Ausführen des Befehls zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="01680-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="01680-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01680-114">PARAMETERS</span></span>

### <span data-ttu-id="01680-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01680-115">-DefaultProfile</span></span>
<span data-ttu-id="01680-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01680-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01680-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01680-117">-InputObject</span></span>
<span data-ttu-id="01680-118">Aufgabenobjekt "Entwurf"</span><span class="sxs-lookup"><span data-stu-id="01680-118">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01680-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="01680-119">-ManagementGroupId</span></span>
<span data-ttu-id="01680-120">Die ID der Verwaltungsgruppe, in der die Blaupausenzuweisung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="01680-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01680-121">-Name</span><span class="sxs-lookup"><span data-stu-id="01680-121">-Name</span></span>
<span data-ttu-id="01680-122">Name der Blaupause.</span><span class="sxs-lookup"><span data-stu-id="01680-122">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01680-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01680-123">-PassThru</span></span>
<span data-ttu-id="01680-124">Wenn dies festgelegt ist, gibt das Cmdlet ein Objekt zurück, das die entfernte "Blueprint"-Zuweisung darstellt.</span><span class="sxs-lookup"><span data-stu-id="01680-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="01680-125">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="01680-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="01680-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="01680-126">-SubscriptionId</span></span>
<span data-ttu-id="01680-127">Abonnement-ID, für die die Blaupausenzuweisung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="01680-127">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01680-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01680-128">-Confirm</span></span>
<span data-ttu-id="01680-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01680-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01680-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="01680-130">-WhatIf</span></span>
<span data-ttu-id="01680-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01680-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01680-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01680-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01680-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01680-133">CommonParameters</span></span>
<span data-ttu-id="01680-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01680-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01680-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01680-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01680-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01680-136">INPUTS</span></span>

### <span data-ttu-id="01680-137">System.String</span><span class="sxs-lookup"><span data-stu-id="01680-137">System.String</span></span>

### <span data-ttu-id="01680-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span><span class="sxs-lookup"><span data-stu-id="01680-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="01680-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01680-139">OUTPUTS</span></span>

### <span data-ttu-id="01680-140">System.Object</span><span class="sxs-lookup"><span data-stu-id="01680-140">System.Object</span></span>
## <span data-ttu-id="01680-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="01680-141">NOTES</span></span>

## <span data-ttu-id="01680-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="01680-142">RELATED LINKS</span></span>
