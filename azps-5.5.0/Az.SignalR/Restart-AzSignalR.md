---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: ea5de8ddd36d315381d4f60ee0fa1ce7dc49adc2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173932"
---
# <span data-ttu-id="e9343-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="e9343-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="e9343-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9343-102">SYNOPSIS</span></span>
<span data-ttu-id="e9343-103">Starten Sie einen SignalR-Dienst neu.</span><span class="sxs-lookup"><span data-stu-id="e9343-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="e9343-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9343-104">SYNTAX</span></span>

### <span data-ttu-id="e9343-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9343-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9343-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9343-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9343-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9343-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9343-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9343-108">DESCRIPTION</span></span>
<span data-ttu-id="e9343-109">Starten Sie einen SignalR-Dienst neu.</span><span class="sxs-lookup"><span data-stu-id="e9343-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="e9343-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e9343-110">EXAMPLES</span></span>

### <span data-ttu-id="e9343-111">Neustarten eines bestimmten SignalR-Diensts</span><span class="sxs-lookup"><span data-stu-id="e9343-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="e9343-112">Die Standardressourcengruppe kann von \` Set-AzDefault -ResourceGroupName myResourceGroup festgelegt \` werden.</span><span class="sxs-lookup"><span data-stu-id="e9343-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="e9343-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9343-113">PARAMETERS</span></span>

### <span data-ttu-id="e9343-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9343-114">-AsJob</span></span>
<span data-ttu-id="e9343-115">Führen Sie das Cmdlet im Hintergrundauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="e9343-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="e9343-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9343-116">-DefaultProfile</span></span>
<span data-ttu-id="e9343-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9343-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9343-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9343-118">-InputObject</span></span>
<span data-ttu-id="e9343-119">Das SignalR-Ressourcenobjekt.</span><span class="sxs-lookup"><span data-stu-id="e9343-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="e9343-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e9343-120">-Name</span></span>
<span data-ttu-id="e9343-121">Der Name des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="e9343-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="e9343-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9343-122">-PassThru</span></span>
<span data-ttu-id="e9343-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="e9343-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="e9343-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9343-124">-ResourceGroupName</span></span>
<span data-ttu-id="e9343-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e9343-125">The resource group name.</span></span>
<span data-ttu-id="e9343-126">Die Standardeinstellung wird verwendet, wenn sie nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e9343-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="e9343-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9343-127">-ResourceId</span></span>
<span data-ttu-id="e9343-128">Die Ressourcen-ID des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="e9343-128">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="e9343-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9343-129">-Confirm</span></span>
<span data-ttu-id="e9343-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e9343-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9343-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e9343-131">-WhatIf</span></span>
<span data-ttu-id="e9343-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9343-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9343-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e9343-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9343-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9343-134">CommonParameters</span></span>
<span data-ttu-id="e9343-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9343-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9343-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9343-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9343-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e9343-137">INPUTS</span></span>

### <span data-ttu-id="e9343-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e9343-138">System.String</span></span>

### <span data-ttu-id="e9343-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="e9343-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="e9343-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e9343-140">OUTPUTS</span></span>

### <span data-ttu-id="e9343-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e9343-141">System.Boolean</span></span>

## <span data-ttu-id="e9343-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e9343-142">NOTES</span></span>

## <span data-ttu-id="e9343-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e9343-143">RELATED LINKS</span></span>
