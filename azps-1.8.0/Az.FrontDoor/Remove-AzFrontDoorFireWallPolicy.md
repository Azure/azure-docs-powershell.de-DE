---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: f081d403a47f457c48320238436d72ca4ebd15fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820007"
---
# <span data-ttu-id="83ebc-101">Remove-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="83ebc-101">Remove-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="83ebc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="83ebc-103">Entfernen der WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="83ebc-103">Remove WAF policy</span></span>

## <span data-ttu-id="83ebc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83ebc-104">SYNTAX</span></span>

### <span data-ttu-id="83ebc-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="83ebc-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83ebc-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83ebc-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorFireWallPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83ebc-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="83ebc-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorFireWallPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83ebc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83ebc-108">DESCRIPTION</span></span>
<span data-ttu-id="83ebc-109">Das Cmdlet " **Remove-AzFrontDoorFireWallPolicy** " entfernt eine WAF-Richtlinie unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83ebc-109">The **Remove-AzFrontDoorFireWallPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="83ebc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83ebc-110">EXAMPLES</span></span>

### <span data-ttu-id="83ebc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="83ebc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="83ebc-112">Entfernen Sie die WAF-Richtlinie namens $policyName in $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="83ebc-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="83ebc-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="83ebc-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorFireWallPolicy
```

<span data-ttu-id="83ebc-114">Entfernen Sie alle WAF-Richtlinien in $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="83ebc-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="83ebc-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="83ebc-115">PARAMETERS</span></span>

### <span data-ttu-id="83ebc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83ebc-116">-DefaultProfile</span></span>
<span data-ttu-id="83ebc-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83ebc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83ebc-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="83ebc-118">-InputObject</span></span>
<span data-ttu-id="83ebc-119">Das zu löschende WAF-Richtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="83ebc-119">The WAF policy object to delete.</span></span>

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

### <span data-ttu-id="83ebc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="83ebc-120">-Name</span></span>
<span data-ttu-id="83ebc-121">Der Name der zu löschenden WAF-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="83ebc-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="83ebc-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83ebc-122">-PassThru</span></span>
<span data-ttu-id="83ebc-123">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="83ebc-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="83ebc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83ebc-124">-ResourceGroupName</span></span>
<span data-ttu-id="83ebc-125">Die Ressourcengruppe, zu der die WAF-Richtlinie gehört.</span><span class="sxs-lookup"><span data-stu-id="83ebc-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="83ebc-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="83ebc-126">-ResourceId</span></span>
<span data-ttu-id="83ebc-127">Ressourcen-ID der zu löschenden WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="83ebc-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="83ebc-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="83ebc-128">-Confirm</span></span>
<span data-ttu-id="83ebc-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83ebc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83ebc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83ebc-130">-WhatIf</span></span>
<span data-ttu-id="83ebc-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83ebc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83ebc-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83ebc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83ebc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ebc-133">CommonParameters</span></span>
<span data-ttu-id="83ebc-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83ebc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ebc-135">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83ebc-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ebc-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83ebc-136">INPUTS</span></span>

### <span data-ttu-id="83ebc-137">Microsoft. Azure. Commands. Haustür. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="83ebc-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="83ebc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="83ebc-138">System.String</span></span>

## <span data-ttu-id="83ebc-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83ebc-139">OUTPUTS</span></span>

### <span data-ttu-id="83ebc-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83ebc-140">System.Boolean</span></span>

## <span data-ttu-id="83ebc-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="83ebc-141">NOTES</span></span>

## <span data-ttu-id="83ebc-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83ebc-142">RELATED LINKS</span></span>

<span data-ttu-id="83ebc-143">[Neu – AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="83ebc-143">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)</span></span>
