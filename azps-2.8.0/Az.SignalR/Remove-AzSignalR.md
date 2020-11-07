---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 075c8e7604ab800e8f1065ff4d025b105d8effc3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823124"
---
# <span data-ttu-id="d4e43-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="d4e43-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="d4e43-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4e43-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e43-103">Entfernen Sie einen Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="d4e43-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="d4e43-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4e43-104">SYNTAX</span></span>

### <span data-ttu-id="d4e43-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4e43-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e43-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4e43-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e43-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4e43-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4e43-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4e43-108">DESCRIPTION</span></span>
<span data-ttu-id="d4e43-109">Entfernen Sie einen Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="d4e43-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="d4e43-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4e43-110">EXAMPLES</span></span>

### <span data-ttu-id="d4e43-111">Entfernen eines Signalisierungs Diensts</span><span class="sxs-lookup"><span data-stu-id="d4e43-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="d4e43-112">Entfernen aller Signalisierungs Dienste vom Kanal</span><span class="sxs-lookup"><span data-stu-id="d4e43-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="d4e43-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4e43-113">PARAMETERS</span></span>

### <span data-ttu-id="d4e43-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4e43-114">-AsJob</span></span>
<span data-ttu-id="d4e43-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d4e43-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4e43-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e43-116">-DefaultProfile</span></span>
<span data-ttu-id="d4e43-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4e43-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4e43-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d4e43-118">-InputObject</span></span>
<span data-ttu-id="d4e43-119">Das Resource-Objekt des Signals.</span><span class="sxs-lookup"><span data-stu-id="d4e43-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="d4e43-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d4e43-120">-Name</span></span>
<span data-ttu-id="d4e43-121">Name des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="d4e43-121">SignalR service name.</span></span>

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

### <span data-ttu-id="d4e43-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4e43-122">-PassThru</span></span>
<span data-ttu-id="d4e43-123">Gibt "true" zurück, wenn die Entfernung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="d4e43-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="d4e43-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e43-124">-ResourceGroupName</span></span>
<span data-ttu-id="d4e43-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d4e43-125">Resource group name.</span></span>

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

### <span data-ttu-id="d4e43-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d4e43-126">-ResourceId</span></span>
<span data-ttu-id="d4e43-127">Die Ressourcen-ID des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="d4e43-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="d4e43-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4e43-128">-Confirm</span></span>
<span data-ttu-id="d4e43-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4e43-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4e43-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4e43-130">-WhatIf</span></span>
<span data-ttu-id="d4e43-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4e43-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4e43-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4e43-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4e43-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e43-133">CommonParameters</span></span>
<span data-ttu-id="d4e43-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4e43-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e43-135">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4e43-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e43-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4e43-136">INPUTS</span></span>

### <span data-ttu-id="d4e43-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d4e43-137">System.String</span></span>
### <span data-ttu-id="d4e43-138">Microsoft. Azure. Commands. signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="d4e43-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="d4e43-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4e43-139">OUTPUTS</span></span>

### <span data-ttu-id="d4e43-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4e43-140">System.Boolean</span></span>
## <span data-ttu-id="d4e43-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4e43-141">NOTES</span></span>

## <span data-ttu-id="d4e43-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4e43-142">RELATED LINKS</span></span>
