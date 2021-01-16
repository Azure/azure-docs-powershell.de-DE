---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 89df3c19b34ee7175e6fe65269f8df5f218a49f3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357173"
---
# <span data-ttu-id="39c27-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="39c27-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="39c27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39c27-102">SYNOPSIS</span></span>
<span data-ttu-id="39c27-103">Entfernen Sie einen SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="39c27-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="39c27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39c27-104">SYNTAX</span></span>

### <span data-ttu-id="39c27-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="39c27-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39c27-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39c27-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39c27-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39c27-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39c27-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39c27-108">DESCRIPTION</span></span>
<span data-ttu-id="39c27-109">Entfernen Sie einen SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="39c27-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="39c27-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39c27-110">EXAMPLES</span></span>

### <span data-ttu-id="39c27-111">Entfernen eines SignalR-Diensts</span><span class="sxs-lookup"><span data-stu-id="39c27-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="39c27-112">Entfernen des sämtlichen SignalR-Diensts vom Pipe</span><span class="sxs-lookup"><span data-stu-id="39c27-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="39c27-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39c27-113">PARAMETERS</span></span>

### <span data-ttu-id="39c27-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39c27-114">-AsJob</span></span>
<span data-ttu-id="39c27-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="39c27-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39c27-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c27-116">-DefaultProfile</span></span>
<span data-ttu-id="39c27-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39c27-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39c27-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39c27-118">-InputObject</span></span>
<span data-ttu-id="39c27-119">Das SignalR-Ressourcenobjekt.</span><span class="sxs-lookup"><span data-stu-id="39c27-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="39c27-120">-Name</span><span class="sxs-lookup"><span data-stu-id="39c27-120">-Name</span></span>
<span data-ttu-id="39c27-121">Name des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="39c27-121">SignalR service name.</span></span>

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

### <span data-ttu-id="39c27-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39c27-122">-PassThru</span></span>
<span data-ttu-id="39c27-123">Gibt "true" zurück, wenn das Entfernen erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="39c27-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="39c27-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39c27-124">-ResourceGroupName</span></span>
<span data-ttu-id="39c27-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="39c27-125">Resource group name.</span></span>

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

### <span data-ttu-id="39c27-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39c27-126">-ResourceId</span></span>
<span data-ttu-id="39c27-127">Die Ressourcen-ID des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="39c27-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="39c27-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39c27-128">-Confirm</span></span>
<span data-ttu-id="39c27-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39c27-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39c27-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="39c27-130">-WhatIf</span></span>
<span data-ttu-id="39c27-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39c27-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39c27-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39c27-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39c27-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c27-133">CommonParameters</span></span>
<span data-ttu-id="39c27-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39c27-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c27-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39c27-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c27-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39c27-136">INPUTS</span></span>

### <span data-ttu-id="39c27-137">System.String</span><span class="sxs-lookup"><span data-stu-id="39c27-137">System.String</span></span>
### <span data-ttu-id="39c27-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="39c27-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="39c27-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39c27-139">OUTPUTS</span></span>

### <span data-ttu-id="39c27-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="39c27-140">System.Boolean</span></span>
## <span data-ttu-id="39c27-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="39c27-141">NOTES</span></span>

## <span data-ttu-id="39c27-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="39c27-142">RELATED LINKS</span></span>
