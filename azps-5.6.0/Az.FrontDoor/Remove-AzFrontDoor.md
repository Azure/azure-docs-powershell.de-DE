---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: 79307a12fbcf5be02d9ea356f41398f76e292379
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950240"
---
# <span data-ttu-id="a94b6-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="a94b6-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="a94b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a94b6-102">SYNOPSIS</span></span>
<span data-ttu-id="a94b6-103">Entfernen des Lastenausgleichs für die Eingangstür</span><span class="sxs-lookup"><span data-stu-id="a94b6-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="a94b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a94b6-104">SYNTAX</span></span>

### <span data-ttu-id="a94b6-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a94b6-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a94b6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a94b6-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a94b6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a94b6-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a94b6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a94b6-108">DESCRIPTION</span></span>
<span data-ttu-id="a94b6-109">Das **Cmdlet Remove-AzFrontDoor** entfernt einen Lastenausgleich für die Eingangstür unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a94b6-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="a94b6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a94b6-110">EXAMPLES</span></span>

### <span data-ttu-id="a94b6-111">Beispiel 1: Entfernen Sie "frontdoor1" in der Ressourcengruppe "rg1" unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a94b6-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="a94b6-112">Entfernen Sie "frontdoor1" in der Ressourcengruppe "rg1" unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a94b6-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="a94b6-113">Beispiel 2: Entfernen Sie alle FrontDoors in der Ressourcengruppe "rg1" unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a94b6-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="a94b6-114">Entfernen Sie alle FrontDoors in der Ressourcengruppe "rg1" unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a94b6-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="a94b6-115">Beispiel 3: Entfernen Aller FrontDoors unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a94b6-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="a94b6-116">Entfernen Sie alle FrontDoors unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a94b6-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="a94b6-117">Beispiel 4: Entfernen Sie alle FrontDoors mit dem Namen "frontdoor1" unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a94b6-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="a94b6-118">Entfernen Sie alle FrontDoors mit dem Namen "frontdoor1" unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a94b6-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="a94b6-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a94b6-119">PARAMETERS</span></span>

### <span data-ttu-id="a94b6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a94b6-120">-DefaultProfile</span></span>
<span data-ttu-id="a94b6-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a94b6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a94b6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a94b6-122">-InputObject</span></span>
<span data-ttu-id="a94b6-123">Das zu löschende Front Door-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a94b6-123">The Front Door object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a94b6-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a94b6-124">-Name</span></span>
<span data-ttu-id="a94b6-125">Der Name der zu löschende Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="a94b6-125">The name of the Front Door to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94b6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a94b6-126">-PassThru</span></span>
<span data-ttu-id="a94b6-127">Rückgabeobjekt (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="a94b6-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="a94b6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a94b6-128">-ResourceGroupName</span></span>
<span data-ttu-id="a94b6-129">Die Ressourcengruppe, zu der die Eingangstür gehört.</span><span class="sxs-lookup"><span data-stu-id="a94b6-129">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94b6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a94b6-130">-ResourceId</span></span>
<span data-ttu-id="a94b6-131">Ressourcen-ID der zu löschende Eingangstür</span><span class="sxs-lookup"><span data-stu-id="a94b6-131">Resource Id of the Front Door to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a94b6-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a94b6-132">-Confirm</span></span>
<span data-ttu-id="a94b6-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a94b6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a94b6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a94b6-134">-WhatIf</span></span>
<span data-ttu-id="a94b6-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a94b6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a94b6-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a94b6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a94b6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a94b6-137">CommonParameters</span></span>
<span data-ttu-id="a94b6-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a94b6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a94b6-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a94b6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a94b6-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a94b6-140">INPUTS</span></span>

### <span data-ttu-id="a94b6-141">Microsoft.Azure.Commands.Frontdoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="a94b6-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="a94b6-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a94b6-142">System.String</span></span>

## <span data-ttu-id="a94b6-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a94b6-143">OUTPUTS</span></span>

### <span data-ttu-id="a94b6-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a94b6-144">System.Boolean</span></span>

## <span data-ttu-id="a94b6-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a94b6-145">NOTES</span></span>

## <span data-ttu-id="a94b6-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a94b6-146">RELATED LINKS</span></span>

<span data-ttu-id="a94b6-147">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="a94b6-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>