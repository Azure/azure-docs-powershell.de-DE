---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 89df3c19b34ee7175e6fe65269f8df5f218a49f3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996026"
---
# <span data-ttu-id="3b0b1-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="3b0b1-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="3b0b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b0b1-102">SYNOPSIS</span></span>
<span data-ttu-id="3b0b1-103">Entfernen Sie einen Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="3b0b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b0b1-104">SYNTAX</span></span>

### <span data-ttu-id="3b0b1-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3b0b1-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b0b1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b0b1-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b0b1-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b0b1-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b0b1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b0b1-108">DESCRIPTION</span></span>
<span data-ttu-id="3b0b1-109">Entfernen Sie einen Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="3b0b1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b0b1-110">EXAMPLES</span></span>

### <span data-ttu-id="3b0b1-111">Entfernen eines Signalisierungs Diensts</span><span class="sxs-lookup"><span data-stu-id="3b0b1-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="3b0b1-112">Entfernen aller Signalisierungs Dienste vom Kanal</span><span class="sxs-lookup"><span data-stu-id="3b0b1-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="3b0b1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b0b1-113">PARAMETERS</span></span>

### <span data-ttu-id="3b0b1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b0b1-114">-AsJob</span></span>
<span data-ttu-id="3b0b1-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3b0b1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b0b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b0b1-116">-DefaultProfile</span></span>
<span data-ttu-id="3b0b1-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b0b1-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3b0b1-118">-InputObject</span></span>
<span data-ttu-id="3b0b1-119">Das Resource-Objekt des Signals.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="3b0b1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3b0b1-120">-Name</span></span>
<span data-ttu-id="3b0b1-121">Name des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-121">SignalR service name.</span></span>

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

### <span data-ttu-id="3b0b1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b0b1-122">-PassThru</span></span>
<span data-ttu-id="3b0b1-123">Gibt "true" zurück, wenn die Entfernung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="3b0b1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b0b1-124">-ResourceGroupName</span></span>
<span data-ttu-id="3b0b1-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-125">Resource group name.</span></span>

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

### <span data-ttu-id="3b0b1-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3b0b1-126">-ResourceId</span></span>
<span data-ttu-id="3b0b1-127">Die Ressourcen-ID des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="3b0b1-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3b0b1-128">-Confirm</span></span>
<span data-ttu-id="3b0b1-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b0b1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b0b1-130">-WhatIf</span></span>
<span data-ttu-id="3b0b1-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b0b1-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b0b1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b0b1-133">CommonParameters</span></span>
<span data-ttu-id="3b0b1-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b0b1-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b0b1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b0b1-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b0b1-136">INPUTS</span></span>

### <span data-ttu-id="3b0b1-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3b0b1-137">System.String</span></span>
### <span data-ttu-id="3b0b1-138">Microsoft. Azure. Commands. signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="3b0b1-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="3b0b1-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b0b1-139">OUTPUTS</span></span>

### <span data-ttu-id="3b0b1-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b0b1-140">System.Boolean</span></span>
## <span data-ttu-id="3b0b1-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b0b1-141">NOTES</span></span>

## <span data-ttu-id="3b0b1-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b0b1-142">RELATED LINKS</span></span>
