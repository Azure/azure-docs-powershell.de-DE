---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 4bb121563c0fe7a635caeffe982502bff3468495
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824668"
---
# <span data-ttu-id="d2581-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="d2581-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="d2581-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2581-102">SYNOPSIS</span></span>
<span data-ttu-id="d2581-103">Regenerieren einer Zugriffstaste für einen Signalisierungs Dienst</span><span class="sxs-lookup"><span data-stu-id="d2581-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="d2581-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2581-104">SYNTAX</span></span>

### <span data-ttu-id="d2581-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d2581-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2581-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2581-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2581-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2581-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2581-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2581-108">DESCRIPTION</span></span>
<span data-ttu-id="d2581-109">Regenerieren einer Zugriffstaste für einen Signalisierungs Dienst</span><span class="sxs-lookup"><span data-stu-id="d2581-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="d2581-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2581-110">EXAMPLES</span></span>

### <span data-ttu-id="d2581-111">Erneutes Generieren des Primärschlüssels</span><span class="sxs-lookup"><span data-stu-id="d2581-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="d2581-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2581-112">PARAMETERS</span></span>

### <span data-ttu-id="d2581-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2581-113">-DefaultProfile</span></span>
<span data-ttu-id="d2581-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2581-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2581-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d2581-115">-InputObject</span></span>
<span data-ttu-id="d2581-116">Das Resource-Objekt des Signals.</span><span class="sxs-lookup"><span data-stu-id="d2581-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="d2581-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="d2581-117">-KeyType</span></span>
<span data-ttu-id="d2581-118">Der Typ des Schlüssels, entweder primär oder sekundär.</span><span class="sxs-lookup"><span data-stu-id="d2581-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="d2581-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d2581-119">-Name</span></span>
<span data-ttu-id="d2581-120">Name des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="d2581-120">SignalR service name.</span></span>

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

### <span data-ttu-id="d2581-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2581-121">-PassThru</span></span>
<span data-ttu-id="d2581-122">Gibt "true" zurück, wenn die Regenerierung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="d2581-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="d2581-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2581-123">-ResourceGroupName</span></span>
<span data-ttu-id="d2581-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d2581-124">Resource group name.</span></span>

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

### <span data-ttu-id="d2581-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d2581-125">-ResourceId</span></span>
<span data-ttu-id="d2581-126">Die Ressourcen-ID des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="d2581-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="d2581-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d2581-127">-Confirm</span></span>
<span data-ttu-id="d2581-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2581-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2581-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2581-129">-WhatIf</span></span>
<span data-ttu-id="d2581-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2581-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2581-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2581-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2581-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2581-132">CommonParameters</span></span>
<span data-ttu-id="d2581-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2581-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2581-134">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2581-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2581-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2581-135">INPUTS</span></span>

### <span data-ttu-id="d2581-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d2581-136">System.String</span></span>
### <span data-ttu-id="d2581-137">Microsoft. Azure. Commands. signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="d2581-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="d2581-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2581-138">OUTPUTS</span></span>

### <span data-ttu-id="d2581-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2581-139">System.Boolean</span></span>
## <span data-ttu-id="d2581-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2581-140">NOTES</span></span>

## <span data-ttu-id="d2581-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2581-141">RELATED LINKS</span></span>
