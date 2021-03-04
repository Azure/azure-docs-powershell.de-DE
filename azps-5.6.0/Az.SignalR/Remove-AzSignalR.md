---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 067dd93f28a5019de96f146a237fe131a9717bfc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920347"
---
# <span data-ttu-id="828a4-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="828a4-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="828a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="828a4-102">SYNOPSIS</span></span>
<span data-ttu-id="828a4-103">Entfernen Sie einen SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="828a4-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="828a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="828a4-104">SYNTAX</span></span>

### <span data-ttu-id="828a4-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="828a4-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="828a4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="828a4-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="828a4-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="828a4-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="828a4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="828a4-108">DESCRIPTION</span></span>
<span data-ttu-id="828a4-109">Entfernen Sie einen SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="828a4-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="828a4-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="828a4-110">EXAMPLES</span></span>

### <span data-ttu-id="828a4-111">Entfernen eines SignalR-Diensts</span><span class="sxs-lookup"><span data-stu-id="828a4-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="828a4-112">Entfernen aller SignalR-Dienste aus dem Rohr</span><span class="sxs-lookup"><span data-stu-id="828a4-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="828a4-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="828a4-113">PARAMETERS</span></span>

### <span data-ttu-id="828a4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="828a4-114">-AsJob</span></span>
<span data-ttu-id="828a4-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="828a4-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="828a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="828a4-116">-DefaultProfile</span></span>
<span data-ttu-id="828a4-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="828a4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="828a4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="828a4-118">-InputObject</span></span>
<span data-ttu-id="828a4-119">Das SignalR-Ressourcenobjekt.</span><span class="sxs-lookup"><span data-stu-id="828a4-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="828a4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="828a4-120">-Name</span></span>
<span data-ttu-id="828a4-121">Name des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="828a4-121">SignalR service name.</span></span>

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

### <span data-ttu-id="828a4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="828a4-122">-PassThru</span></span>
<span data-ttu-id="828a4-123">Gibt "true" zurück, wenn die Entfernung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="828a4-123">Returns true if the removal was completed successfully.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="828a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="828a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="828a4-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="828a4-125">Resource group name.</span></span>

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

### <span data-ttu-id="828a4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="828a4-126">-ResourceId</span></span>
<span data-ttu-id="828a4-127">Die Ressourcen-ID des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="828a4-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="828a4-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="828a4-128">-Confirm</span></span>
<span data-ttu-id="828a4-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="828a4-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="828a4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="828a4-130">-WhatIf</span></span>
<span data-ttu-id="828a4-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="828a4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="828a4-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="828a4-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="828a4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="828a4-133">CommonParameters</span></span>
<span data-ttu-id="828a4-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="828a4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="828a4-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="828a4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="828a4-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="828a4-136">INPUTS</span></span>

### <span data-ttu-id="828a4-137">System.String</span><span class="sxs-lookup"><span data-stu-id="828a4-137">System.String</span></span>
### <span data-ttu-id="828a4-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="828a4-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="828a4-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="828a4-139">OUTPUTS</span></span>

### <span data-ttu-id="828a4-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="828a4-140">System.Boolean</span></span>
## <span data-ttu-id="828a4-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="828a4-141">NOTES</span></span>

## <span data-ttu-id="828a4-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="828a4-142">RELATED LINKS</span></span>
