---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: a17f8e6457cc62799fdef3d3606e04962774fdac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920352"
---
# <span data-ttu-id="c1e2a-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="c1e2a-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="c1e2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1e2a-102">SYNOPSIS</span></span>
<span data-ttu-id="c1e2a-103">Regenerieren Sie einen Zugriffsschlüssel für einen SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="c1e2a-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="c1e2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1e2a-104">SYNTAX</span></span>

### <span data-ttu-id="c1e2a-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c1e2a-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1e2a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1e2a-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1e2a-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1e2a-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1e2a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1e2a-108">DESCRIPTION</span></span>
<span data-ttu-id="c1e2a-109">Regenerieren Sie einen Zugriffsschlüssel für einen SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="c1e2a-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="c1e2a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c1e2a-110">EXAMPLES</span></span>

### <span data-ttu-id="c1e2a-111">Regenerieren des Primärschlüssels</span><span class="sxs-lookup"><span data-stu-id="c1e2a-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="c1e2a-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c1e2a-112">PARAMETERS</span></span>

### <span data-ttu-id="c1e2a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1e2a-113">-DefaultProfile</span></span>
<span data-ttu-id="c1e2a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1e2a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1e2a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1e2a-115">-InputObject</span></span>
<span data-ttu-id="c1e2a-116">Das SignalR-Ressourcenobjekt.</span><span class="sxs-lookup"><span data-stu-id="c1e2a-116">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1e2a-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="c1e2a-117">-KeyType</span></span>
<span data-ttu-id="c1e2a-118">Der Schlüsseltyp, entweder Primär oder Sekundär.</span><span class="sxs-lookup"><span data-stu-id="c1e2a-118">The key type, either Primary or Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e2a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c1e2a-119">-Name</span></span>
<span data-ttu-id="c1e2a-120">Name des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="c1e2a-120">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e2a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1e2a-121">-PassThru</span></span>
<span data-ttu-id="c1e2a-122">Gibt "true" zurück, wenn die Verjüngung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="c1e2a-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="c1e2a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1e2a-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1e2a-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c1e2a-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e2a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1e2a-125">-ResourceId</span></span>
<span data-ttu-id="c1e2a-126">Die Ressourcen-ID des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="c1e2a-126">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1e2a-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c1e2a-127">-Confirm</span></span>
<span data-ttu-id="c1e2a-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1e2a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1e2a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1e2a-129">-WhatIf</span></span>
<span data-ttu-id="c1e2a-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1e2a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1e2a-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1e2a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1e2a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1e2a-132">CommonParameters</span></span>
<span data-ttu-id="c1e2a-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1e2a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1e2a-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1e2a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1e2a-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c1e2a-135">INPUTS</span></span>

### <span data-ttu-id="c1e2a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c1e2a-136">System.String</span></span>
### <span data-ttu-id="c1e2a-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="c1e2a-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="c1e2a-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c1e2a-138">OUTPUTS</span></span>

### <span data-ttu-id="c1e2a-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c1e2a-139">System.Boolean</span></span>
## <span data-ttu-id="c1e2a-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c1e2a-140">NOTES</span></span>

## <span data-ttu-id="c1e2a-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c1e2a-141">RELATED LINKS</span></span>
