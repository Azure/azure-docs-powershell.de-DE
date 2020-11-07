---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
ms.openlocfilehash: 8eae5034080bd1035cfe7e8331ca015820688e63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662175"
---
# <span data-ttu-id="3bf76-101">Remove-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="3bf76-101">Remove-AzureRmFrontDoor</span></span>

## <span data-ttu-id="3bf76-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3bf76-102">SYNOPSIS</span></span>
<span data-ttu-id="3bf76-103">Entfernen des Front-Load-Balancer</span><span class="sxs-lookup"><span data-stu-id="3bf76-103">Remove Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bf76-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bf76-104">SYNTAX</span></span>

### <span data-ttu-id="3bf76-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3bf76-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bf76-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bf76-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bf76-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bf76-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bf76-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3bf76-108">DESCRIPTION</span></span>
<span data-ttu-id="3bf76-109">Mit dem Cmdlet **Remove-AzureRmFrontDoor** wird ein Front-Door Load Balancer unter dem aktuellen Abonnement entfernt</span><span class="sxs-lookup"><span data-stu-id="3bf76-109">The **Remove-AzureRmFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="3bf76-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3bf76-110">EXAMPLES</span></span>

### <span data-ttu-id="3bf76-111">Beispiel 1: Entfernen Sie "frontdoor1" in der Ressourcengruppe "RG1" unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3bf76-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="3bf76-112">Entfernen Sie "frontdoor1" in der Ressourcengruppe "RG1" unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3bf76-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="3bf76-113">Beispiel 2: Entfernen Sie alle FrontDoors in der Ressourcengruppe "RG1" unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3bf76-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="3bf76-114">Entfernen Sie alle FrontDoors in der Ressourcengruppe "RG1" unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3bf76-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="3bf76-115">Beispiel 3: Entfernen aller FrontDoors unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3bf76-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor | Remove-AzureRmFrontDoor
```

<span data-ttu-id="3bf76-116">Entfernen Sie alle FrontDoors unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3bf76-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="3bf76-117">Beispiel 4: Entfernen Sie alle FrontDoors mit dem Namen "frontdoor1" unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3bf76-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="3bf76-118">Entfernen Sie alle FrontDoors mit dem Namen "frontdoor1" unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3bf76-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="3bf76-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bf76-119">PARAMETERS</span></span>

### <span data-ttu-id="3bf76-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bf76-120">-DefaultProfile</span></span>
<span data-ttu-id="3bf76-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3bf76-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bf76-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3bf76-122">-InputObject</span></span>
<span data-ttu-id="3bf76-123">Das zu löschende Haustür Objekt.</span><span class="sxs-lookup"><span data-stu-id="3bf76-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="3bf76-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3bf76-124">-Name</span></span>
<span data-ttu-id="3bf76-125">Der Name der zu löschenden Haustür.</span><span class="sxs-lookup"><span data-stu-id="3bf76-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="3bf76-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bf76-126">-PassThru</span></span>
<span data-ttu-id="3bf76-127">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="3bf76-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="3bf76-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bf76-128">-ResourceGroupName</span></span>
<span data-ttu-id="3bf76-129">Die Ressourcengruppe, zu der die Haustür gehört.</span><span class="sxs-lookup"><span data-stu-id="3bf76-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="3bf76-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3bf76-130">-ResourceId</span></span>
<span data-ttu-id="3bf76-131">Ressourcen-ID der zu löschenden Haustür</span><span class="sxs-lookup"><span data-stu-id="3bf76-131">Resource Id of the Front Door to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bf76-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3bf76-132">-Confirm</span></span>
<span data-ttu-id="3bf76-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3bf76-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bf76-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bf76-134">-WhatIf</span></span>
<span data-ttu-id="3bf76-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3bf76-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bf76-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3bf76-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bf76-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bf76-137">CommonParameters</span></span>
<span data-ttu-id="3bf76-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bf76-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bf76-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bf76-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bf76-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3bf76-140">INPUTS</span></span>

### <span data-ttu-id="3bf76-141">Microsoft. Azure. Commands. Haustür. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="3bf76-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="3bf76-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3bf76-142">System.String</span></span>

### <span data-ttu-id="3bf76-143">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="3bf76-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3bf76-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3bf76-144">OUTPUTS</span></span>

### <span data-ttu-id="3bf76-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3bf76-145">System.Boolean</span></span>

## <span data-ttu-id="3bf76-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="3bf76-146">NOTES</span></span>

## <span data-ttu-id="3bf76-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3bf76-147">RELATED LINKS</span></span>

<span data-ttu-id="3bf76-148">[Neu – AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="3bf76-148">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span></span>
