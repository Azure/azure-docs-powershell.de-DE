---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: 133afe9b64fd9161bb7d39fadf6349803f9e2282
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995411"
---
# <span data-ttu-id="f3f30-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="f3f30-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="f3f30-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3f30-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f30-103">Entfernen des Front-Load-Balancer</span><span class="sxs-lookup"><span data-stu-id="f3f30-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="f3f30-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3f30-104">SYNTAX</span></span>

### <span data-ttu-id="f3f30-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f3f30-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3f30-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3f30-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3f30-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3f30-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3f30-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3f30-108">DESCRIPTION</span></span>
<span data-ttu-id="f3f30-109">Mit dem Cmdlet **Remove-AzFrontDoor** wird ein Front-Door Load Balancer unter dem aktuellen Abonnement entfernt</span><span class="sxs-lookup"><span data-stu-id="f3f30-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="f3f30-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3f30-110">EXAMPLES</span></span>

### <span data-ttu-id="f3f30-111">Beispiel 1: Entfernen Sie "frontdoor1" in der Ressourcengruppe "RG1" unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3f30-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="f3f30-112">Entfernen Sie "frontdoor1" in der Ressourcengruppe "RG1" unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3f30-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="f3f30-113">Beispiel 2: Entfernen Sie alle FrontDoors in der Ressourcengruppe "RG1" unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3f30-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="f3f30-114">Entfernen Sie alle FrontDoors in der Ressourcengruppe "RG1" unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3f30-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="f3f30-115">Beispiel 3: Entfernen aller FrontDoors unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3f30-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="f3f30-116">Entfernen Sie alle FrontDoors unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3f30-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="f3f30-117">Beispiel 4: Entfernen Sie alle FrontDoors mit dem Namen "frontdoor1" unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3f30-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="f3f30-118">Entfernen Sie alle FrontDoors mit dem Namen "frontdoor1" unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3f30-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="f3f30-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3f30-119">PARAMETERS</span></span>

### <span data-ttu-id="f3f30-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f30-120">-DefaultProfile</span></span>
<span data-ttu-id="f3f30-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3f30-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3f30-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f3f30-122">-InputObject</span></span>
<span data-ttu-id="f3f30-123">Das zu löschende Haustür Objekt.</span><span class="sxs-lookup"><span data-stu-id="f3f30-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="f3f30-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f3f30-124">-Name</span></span>
<span data-ttu-id="f3f30-125">Der Name der zu löschenden Haustür.</span><span class="sxs-lookup"><span data-stu-id="f3f30-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="f3f30-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3f30-126">-PassThru</span></span>
<span data-ttu-id="f3f30-127">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="f3f30-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="f3f30-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3f30-128">-ResourceGroupName</span></span>
<span data-ttu-id="f3f30-129">Die Ressourcengruppe, zu der die Haustür gehört.</span><span class="sxs-lookup"><span data-stu-id="f3f30-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="f3f30-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f3f30-130">-ResourceId</span></span>
<span data-ttu-id="f3f30-131">Ressourcen-ID der zu löschenden Haustür</span><span class="sxs-lookup"><span data-stu-id="f3f30-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="f3f30-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f3f30-132">-Confirm</span></span>
<span data-ttu-id="f3f30-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f3f30-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3f30-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3f30-134">-WhatIf</span></span>
<span data-ttu-id="f3f30-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f3f30-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3f30-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3f30-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3f30-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f30-137">CommonParameters</span></span>
<span data-ttu-id="f3f30-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3f30-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f30-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3f30-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f30-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3f30-140">INPUTS</span></span>

### <span data-ttu-id="f3f30-141">Microsoft. Azure. Commands. Haustür. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="f3f30-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="f3f30-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f3f30-142">System.String</span></span>

## <span data-ttu-id="f3f30-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3f30-143">OUTPUTS</span></span>

### <span data-ttu-id="f3f30-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f3f30-144">System.Boolean</span></span>

## <span data-ttu-id="f3f30-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3f30-145">NOTES</span></span>

## <span data-ttu-id="f3f30-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3f30-146">RELATED LINKS</span></span>

<span data-ttu-id="f3f30-147">[Neu – AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="f3f30-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>