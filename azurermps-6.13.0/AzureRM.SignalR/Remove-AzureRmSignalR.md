---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Remove-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Remove-AzureRmSignalR.md
ms.openlocfilehash: 5fcf62e592ed1e842c3dc6f4be21462170c4f83b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497277"
---
# <span data-ttu-id="6c63c-101">Remove-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="6c63c-101">Remove-AzureRmSignalR</span></span>

## <span data-ttu-id="6c63c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c63c-102">SYNOPSIS</span></span>
<span data-ttu-id="6c63c-103">Entfernen Sie einen Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="6c63c-103">Remove a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c63c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c63c-104">SYNTAX</span></span>

### <span data-ttu-id="6c63c-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6c63c-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c63c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c63c-106">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c63c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c63c-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c63c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c63c-108">DESCRIPTION</span></span>
<span data-ttu-id="6c63c-109">Entfernen Sie einen Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="6c63c-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="6c63c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c63c-110">EXAMPLES</span></span>

### <span data-ttu-id="6c63c-111">Entfernen eines Signalisierungs Diensts</span><span class="sxs-lookup"><span data-stu-id="6c63c-111">Remove a SignalR service</span></span>
```powershell
PS C:\> Remove-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="6c63c-112">Entfernen aller Signalisierungs Dienste vom Kanal</span><span class="sxs-lookup"><span data-stu-id="6c63c-112">Remove all SignalR service from pipe</span></span>
```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup | Remove-AzureRmSignalR
```

## <span data-ttu-id="6c63c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c63c-113">PARAMETERS</span></span>

### <span data-ttu-id="6c63c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c63c-114">-AsJob</span></span>
<span data-ttu-id="6c63c-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6c63c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c63c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c63c-116">-DefaultProfile</span></span>
<span data-ttu-id="6c63c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6c63c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c63c-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6c63c-118">-InputObject</span></span>
<span data-ttu-id="6c63c-119">Das Resource-Objekt des Signals.</span><span class="sxs-lookup"><span data-stu-id="6c63c-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="6c63c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6c63c-120">-Name</span></span>
<span data-ttu-id="6c63c-121">Name des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="6c63c-121">SignalR service name.</span></span>

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

### <span data-ttu-id="6c63c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c63c-122">-PassThru</span></span>
<span data-ttu-id="6c63c-123">Gibt "true" zurück, wenn die Entfernung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="6c63c-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="6c63c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c63c-124">-ResourceGroupName</span></span>
<span data-ttu-id="6c63c-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6c63c-125">Resource group name.</span></span>

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

### <span data-ttu-id="6c63c-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6c63c-126">-ResourceId</span></span>
<span data-ttu-id="6c63c-127">Die Ressourcen-ID des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="6c63c-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="6c63c-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6c63c-128">-Confirm</span></span>
<span data-ttu-id="6c63c-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c63c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c63c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c63c-130">-WhatIf</span></span>
<span data-ttu-id="6c63c-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c63c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c63c-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c63c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c63c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c63c-133">CommonParameters</span></span>
<span data-ttu-id="6c63c-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c63c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c63c-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c63c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c63c-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c63c-136">INPUTS</span></span>

### <span data-ttu-id="6c63c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6c63c-137">System.String</span></span>
<span data-ttu-id="6c63c-138">Parameter: resourcecode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6c63c-138">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="6c63c-139">Microsoft. Azure. Commands. signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="6c63c-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="6c63c-140">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6c63c-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6c63c-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c63c-141">OUTPUTS</span></span>

### <span data-ttu-id="6c63c-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6c63c-142">System.Boolean</span></span>

## <span data-ttu-id="6c63c-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c63c-143">NOTES</span></span>

## <span data-ttu-id="6c63c-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c63c-144">RELATED LINKS</span></span>
