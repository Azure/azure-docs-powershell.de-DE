---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 70e917c633b2c6ba45fcf0aaf7b3f36af366c150
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651104"
---
# <span data-ttu-id="aa85d-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="aa85d-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="aa85d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa85d-102">SYNOPSIS</span></span>
<span data-ttu-id="aa85d-103">Entfernen der WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="aa85d-103">Remove WAF policy</span></span>

## <span data-ttu-id="aa85d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa85d-104">SYNTAX</span></span>

### <span data-ttu-id="aa85d-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aa85d-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa85d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa85d-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa85d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa85d-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa85d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa85d-108">DESCRIPTION</span></span>
<span data-ttu-id="aa85d-109">Das Cmdlet " **Remove-AzFrontDoorWafPolicy** " entfernt eine WAF-Richtlinie unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aa85d-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="aa85d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa85d-110">EXAMPLES</span></span>

### <span data-ttu-id="aa85d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aa85d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="aa85d-112">Entfernen Sie die WAF-Richtlinie namens $policyName in $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="aa85d-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="aa85d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="aa85d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="aa85d-114">Entfernen Sie alle WAF-Richtlinien in $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="aa85d-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="aa85d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa85d-115">PARAMETERS</span></span>

### <span data-ttu-id="aa85d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa85d-116">-DefaultProfile</span></span>
<span data-ttu-id="aa85d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aa85d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa85d-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aa85d-118">-InputObject</span></span>
<span data-ttu-id="aa85d-119">Das zu löschende WAF-Richtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="aa85d-119">The WAF policy object to delete.</span></span>

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

### <span data-ttu-id="aa85d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="aa85d-120">-Name</span></span>
<span data-ttu-id="aa85d-121">Der Name der zu löschenden WAF-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="aa85d-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="aa85d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa85d-122">-PassThru</span></span>
<span data-ttu-id="aa85d-123">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="aa85d-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="aa85d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa85d-124">-ResourceGroupName</span></span>
<span data-ttu-id="aa85d-125">Die Ressourcengruppe, zu der die WAF-Richtlinie gehört.</span><span class="sxs-lookup"><span data-stu-id="aa85d-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="aa85d-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="aa85d-126">-ResourceId</span></span>
<span data-ttu-id="aa85d-127">Ressourcen-ID der zu löschenden WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="aa85d-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="aa85d-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aa85d-128">-Confirm</span></span>
<span data-ttu-id="aa85d-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa85d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa85d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa85d-130">-WhatIf</span></span>
<span data-ttu-id="aa85d-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa85d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa85d-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa85d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa85d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa85d-133">CommonParameters</span></span>
<span data-ttu-id="aa85d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa85d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa85d-135">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa85d-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa85d-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa85d-136">INPUTS</span></span>

### <span data-ttu-id="aa85d-137">Microsoft. Azure. Commands. Haustür. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="aa85d-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="aa85d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="aa85d-138">System.String</span></span>

## <span data-ttu-id="aa85d-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa85d-139">OUTPUTS</span></span>

### <span data-ttu-id="aa85d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa85d-140">System.Boolean</span></span>

## <span data-ttu-id="aa85d-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa85d-141">NOTES</span></span>

## <span data-ttu-id="aa85d-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa85d-142">RELATED LINKS</span></span>

<span data-ttu-id="aa85d-143">[Neu – AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="aa85d-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>
