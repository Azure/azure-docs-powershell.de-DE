---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: f8a50a7e9686a3e40f517992e6c4de9912e8671b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925168"
---
# <span data-ttu-id="2168c-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="2168c-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="2168c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2168c-102">SYNOPSIS</span></span>
<span data-ttu-id="2168c-103">Entfernen sie eine Blaupausenzuordnung aus einem Abonnement oder einer Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2168c-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="2168c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2168c-104">SYNTAX</span></span>

### <span data-ttu-id="2168c-105">BySubscriptionAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2168c-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2168c-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="2168c-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2168c-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="2168c-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2168c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2168c-108">DESCRIPTION</span></span>
<span data-ttu-id="2168c-109">Entfernen Sie eine Blaupause, die einem Abonnement zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="2168c-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="2168c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2168c-110">EXAMPLES</span></span>

### <span data-ttu-id="2168c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2168c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="2168c-112">Entfernen Sie die vom Namen angegebene Blaupausenzuordnung aus dem angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2168c-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="2168c-113">Das Cmdlet wird zur Bestätigung aufgefordert, bevor der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2168c-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="2168c-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2168c-114">PARAMETERS</span></span>

### <span data-ttu-id="2168c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2168c-115">-DefaultProfile</span></span>
<span data-ttu-id="2168c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2168c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2168c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2168c-117">-InputObject</span></span>
<span data-ttu-id="2168c-118">Objekt für die Blaupausenzuordnung.</span><span class="sxs-lookup"><span data-stu-id="2168c-118">Blueprint assignment object.</span></span>

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

### <span data-ttu-id="2168c-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="2168c-119">-ManagementGroupId</span></span>
<span data-ttu-id="2168c-120">Die ID der Verwaltungsgruppe, in der die Blaupausenzuordnung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="2168c-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

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

### <span data-ttu-id="2168c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2168c-121">-Name</span></span>
<span data-ttu-id="2168c-122">Name der Blaupausenzuordnung.</span><span class="sxs-lookup"><span data-stu-id="2168c-122">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="2168c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2168c-123">-PassThru</span></span>
<span data-ttu-id="2168c-124">Wenn festgelegt, gibt das Cmdlet ein Objekt zurück, das die entfernte Blaupausenzuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="2168c-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="2168c-125">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="2168c-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2168c-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2168c-126">-SubscriptionId</span></span>
<span data-ttu-id="2168c-127">Abonnement-ID, für die die Blaupausenzuordnung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2168c-127">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="2168c-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2168c-128">-Confirm</span></span>
<span data-ttu-id="2168c-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2168c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2168c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2168c-130">-WhatIf</span></span>
<span data-ttu-id="2168c-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2168c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2168c-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2168c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2168c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2168c-133">CommonParameters</span></span>
<span data-ttu-id="2168c-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2168c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2168c-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2168c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2168c-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2168c-136">INPUTS</span></span>

### <span data-ttu-id="2168c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2168c-137">System.String</span></span>

### <span data-ttu-id="2168c-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span><span class="sxs-lookup"><span data-stu-id="2168c-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="2168c-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2168c-139">OUTPUTS</span></span>

### <span data-ttu-id="2168c-140">System.Object</span><span class="sxs-lookup"><span data-stu-id="2168c-140">System.Object</span></span>
## <span data-ttu-id="2168c-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2168c-141">NOTES</span></span>

## <span data-ttu-id="2168c-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2168c-142">RELATED LINKS</span></span>
