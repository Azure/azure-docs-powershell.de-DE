---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 89df3c19b34ee7175e6fe65269f8df5f218a49f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166086"
---
# <span data-ttu-id="7757e-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="7757e-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="7757e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7757e-102">SYNOPSIS</span></span>
<span data-ttu-id="7757e-103">Entfernen Sie einen Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="7757e-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="7757e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7757e-104">SYNTAX</span></span>

### <span data-ttu-id="7757e-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7757e-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7757e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7757e-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7757e-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7757e-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7757e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7757e-108">DESCRIPTION</span></span>
<span data-ttu-id="7757e-109">Entfernen Sie einen Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="7757e-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="7757e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7757e-110">EXAMPLES</span></span>

### <span data-ttu-id="7757e-111">Entfernen eines Signalisierungs Diensts</span><span class="sxs-lookup"><span data-stu-id="7757e-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="7757e-112">Entfernen aller Signalisierungs Dienste vom Kanal</span><span class="sxs-lookup"><span data-stu-id="7757e-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="7757e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7757e-113">PARAMETERS</span></span>

### <span data-ttu-id="7757e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7757e-114">-AsJob</span></span>
<span data-ttu-id="7757e-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7757e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7757e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7757e-116">-DefaultProfile</span></span>
<span data-ttu-id="7757e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7757e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7757e-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7757e-118">-InputObject</span></span>
<span data-ttu-id="7757e-119">Das Resource-Objekt des Signals.</span><span class="sxs-lookup"><span data-stu-id="7757e-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="7757e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7757e-120">-Name</span></span>
<span data-ttu-id="7757e-121">Name des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="7757e-121">SignalR service name.</span></span>

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

### <span data-ttu-id="7757e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7757e-122">-PassThru</span></span>
<span data-ttu-id="7757e-123">Gibt "true" zurück, wenn die Entfernung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="7757e-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="7757e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7757e-124">-ResourceGroupName</span></span>
<span data-ttu-id="7757e-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7757e-125">Resource group name.</span></span>

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

### <span data-ttu-id="7757e-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7757e-126">-ResourceId</span></span>
<span data-ttu-id="7757e-127">Die Ressourcen-ID des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="7757e-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="7757e-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7757e-128">-Confirm</span></span>
<span data-ttu-id="7757e-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7757e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7757e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7757e-130">-WhatIf</span></span>
<span data-ttu-id="7757e-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7757e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7757e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7757e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7757e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7757e-133">CommonParameters</span></span>
<span data-ttu-id="7757e-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7757e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7757e-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7757e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7757e-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7757e-136">INPUTS</span></span>

### <span data-ttu-id="7757e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7757e-137">System.String</span></span>
### <span data-ttu-id="7757e-138">Microsoft. Azure. Commands. signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="7757e-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="7757e-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7757e-139">OUTPUTS</span></span>

### <span data-ttu-id="7757e-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7757e-140">System.Boolean</span></span>
## <span data-ttu-id="7757e-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="7757e-141">NOTES</span></span>

## <span data-ttu-id="7757e-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7757e-142">RELATED LINKS</span></span>
