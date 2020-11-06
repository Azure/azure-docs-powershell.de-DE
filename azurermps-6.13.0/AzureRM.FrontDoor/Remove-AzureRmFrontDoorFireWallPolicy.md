---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 4dda510402b9395db24507f22d90da0f1fb6a44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476053"
---
# <span data-ttu-id="5af6b-101">Remove-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="5af6b-101">Remove-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="5af6b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5af6b-102">SYNOPSIS</span></span>
<span data-ttu-id="5af6b-103">Entfernen der WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="5af6b-103">Remove WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5af6b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5af6b-104">SYNTAX</span></span>

### <span data-ttu-id="5af6b-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5af6b-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5af6b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5af6b-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5af6b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5af6b-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5af6b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5af6b-108">DESCRIPTION</span></span>
<span data-ttu-id="5af6b-109">Das Cmdlet " **Remove-AzureRmFrontDoor** " entfernt eine WAF-Richtlinie unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5af6b-109">The **Remove-AzureRmFrontDoor** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="5af6b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5af6b-110">EXAMPLES</span></span>

### <span data-ttu-id="5af6b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5af6b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup
```

<span data-ttu-id="5af6b-112">Entfernen Sie die WAF-Richtlinie namens $Name in $resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5af6b-112">Remove the WAF policy called $name in $resourceGroup.</span></span>

### <span data-ttu-id="5af6b-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5af6b-113">Example 2</span></span>
```powershell
PS C:\> Get--AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Remove-AzureRmFrontDoorFireWallPolicy
```

<span data-ttu-id="5af6b-114">Entfernen Sie alle WAF-Richtlinien in $resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5af6b-114">Remove all WAF policy in $resourceGroup.</span></span>

## <span data-ttu-id="5af6b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5af6b-115">PARAMETERS</span></span>

### <span data-ttu-id="5af6b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5af6b-116">-DefaultProfile</span></span>
<span data-ttu-id="5af6b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5af6b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5af6b-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5af6b-118">-InputObject</span></span>
<span data-ttu-id="5af6b-119">Das zu löschende WAF-Richtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="5af6b-119">The WAF policy object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5af6b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5af6b-120">-Name</span></span>
<span data-ttu-id="5af6b-121">Der Name der zu löschenden WAF-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="5af6b-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="5af6b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5af6b-122">-PassThru</span></span>
<span data-ttu-id="5af6b-123">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="5af6b-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="5af6b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5af6b-124">-ResourceGroupName</span></span>
<span data-ttu-id="5af6b-125">Die Ressourcengruppe, zu der die WAF-Richtlinie gehört.</span><span class="sxs-lookup"><span data-stu-id="5af6b-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="5af6b-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5af6b-126">-ResourceId</span></span>
<span data-ttu-id="5af6b-127">Ressourcen-ID der zu löschenden WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="5af6b-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="5af6b-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5af6b-128">-Confirm</span></span>
<span data-ttu-id="5af6b-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5af6b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5af6b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5af6b-130">-WhatIf</span></span>
<span data-ttu-id="5af6b-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5af6b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5af6b-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5af6b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5af6b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5af6b-133">CommonParameters</span></span>
<span data-ttu-id="5af6b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5af6b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5af6b-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5af6b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5af6b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5af6b-136">INPUTS</span></span>

### <span data-ttu-id="5af6b-137">Microsoft. Azure. Commands. Haustür. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="5af6b-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="5af6b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5af6b-138">System.String</span></span>

### <span data-ttu-id="5af6b-139">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="5af6b-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5af6b-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5af6b-140">OUTPUTS</span></span>

### <span data-ttu-id="5af6b-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5af6b-141">System.Boolean</span></span>

## <span data-ttu-id="5af6b-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="5af6b-142">NOTES</span></span>

## <span data-ttu-id="5af6b-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5af6b-143">RELATED LINKS</span></span>

<span data-ttu-id="5af6b-144">[Neu – AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="5af6b-144">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span></span>
