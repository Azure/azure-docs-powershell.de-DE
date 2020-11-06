---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalRKey.md
ms.openlocfilehash: 4b4f3a416ece999641570a33101a3e7ab201ca3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497281"
---
# <span data-ttu-id="25d56-101">New-AzureRmSignalRKey</span><span class="sxs-lookup"><span data-stu-id="25d56-101">New-AzureRmSignalRKey</span></span>

## <span data-ttu-id="25d56-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25d56-102">SYNOPSIS</span></span>
<span data-ttu-id="25d56-103">Regenerieren einer Zugriffstaste für einen Signalisierungs Dienst</span><span class="sxs-lookup"><span data-stu-id="25d56-103">Regenerate an access key for a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25d56-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25d56-104">SYNTAX</span></span>

### <span data-ttu-id="25d56-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="25d56-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25d56-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25d56-106">ResourceIdParameterSet</span></span>
```
New-AzureRmSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25d56-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25d56-107">InputObjectParameterSet</span></span>
```
New-AzureRmSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25d56-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25d56-108">DESCRIPTION</span></span>
<span data-ttu-id="25d56-109">Regenerieren einer Zugriffstaste für einen Signalisierungs Dienst</span><span class="sxs-lookup"><span data-stu-id="25d56-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="25d56-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25d56-110">EXAMPLES</span></span>

### <span data-ttu-id="25d56-111">Erneutes Generieren des Primärschlüssels</span><span class="sxs-lookup"><span data-stu-id="25d56-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzureRmSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="25d56-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="25d56-112">PARAMETERS</span></span>

### <span data-ttu-id="25d56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d56-113">-DefaultProfile</span></span>
<span data-ttu-id="25d56-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25d56-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25d56-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="25d56-115">-InputObject</span></span>
<span data-ttu-id="25d56-116">Das Resource-Objekt des Signals.</span><span class="sxs-lookup"><span data-stu-id="25d56-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="25d56-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="25d56-117">-KeyType</span></span>
<span data-ttu-id="25d56-118">Der Typ des Schlüssels, entweder primär oder sekundär.</span><span class="sxs-lookup"><span data-stu-id="25d56-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="25d56-119">-Name</span><span class="sxs-lookup"><span data-stu-id="25d56-119">-Name</span></span>
<span data-ttu-id="25d56-120">Name des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="25d56-120">SignalR service name.</span></span>

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

### <span data-ttu-id="25d56-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25d56-121">-PassThru</span></span>
<span data-ttu-id="25d56-122">Gibt "true" zurück, wenn die Regenerierung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="25d56-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="25d56-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d56-123">-ResourceGroupName</span></span>
<span data-ttu-id="25d56-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="25d56-124">Resource group name.</span></span>

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

### <span data-ttu-id="25d56-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="25d56-125">-ResourceId</span></span>
<span data-ttu-id="25d56-126">Die Ressourcen-ID des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="25d56-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="25d56-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="25d56-127">-Confirm</span></span>
<span data-ttu-id="25d56-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25d56-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25d56-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25d56-129">-WhatIf</span></span>
<span data-ttu-id="25d56-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25d56-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25d56-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25d56-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25d56-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d56-132">CommonParameters</span></span>
<span data-ttu-id="25d56-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25d56-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d56-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25d56-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d56-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25d56-135">INPUTS</span></span>

### <span data-ttu-id="25d56-136">System. String</span><span class="sxs-lookup"><span data-stu-id="25d56-136">System.String</span></span>
<span data-ttu-id="25d56-137">Parameter: resourcecode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="25d56-137">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="25d56-138">Microsoft. Azure. Commands. signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="25d56-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="25d56-139">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="25d56-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="25d56-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25d56-140">OUTPUTS</span></span>

### <span data-ttu-id="25d56-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25d56-141">System.Boolean</span></span>

## <span data-ttu-id="25d56-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="25d56-142">NOTES</span></span>

## <span data-ttu-id="25d56-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25d56-143">RELATED LINKS</span></span>
