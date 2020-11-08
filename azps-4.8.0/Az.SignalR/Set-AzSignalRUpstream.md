---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: e04e87067f86f529117512e7443118f308b20547
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010473"
---
# <span data-ttu-id="5b2ef-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="5b2ef-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="5b2ef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b2ef-102">SYNOPSIS</span></span>
<span data-ttu-id="5b2ef-103">Festlegen der Upstream-Einstellungen eines Signalisierungs Diensts</span><span class="sxs-lookup"><span data-stu-id="5b2ef-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="5b2ef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b2ef-104">SYNTAX</span></span>

### <span data-ttu-id="5b2ef-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b2ef-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b2ef-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b2ef-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b2ef-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b2ef-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b2ef-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b2ef-108">DESCRIPTION</span></span>
<span data-ttu-id="5b2ef-109">Festlegen der Upstream-Einstellungen eines Signalisierungs Diensts</span><span class="sxs-lookup"><span data-stu-id="5b2ef-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="5b2ef-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b2ef-110">EXAMPLES</span></span>

### <span data-ttu-id="5b2ef-111">Einrichten von zwei geordneten Upstream-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="5b2ef-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="5b2ef-112">Die folgende JSON steht für den tatsächlichen Vorlagensatz.</span><span class="sxs-lookup"><span data-stu-id="5b2ef-112">The following JSON represents the actual templates set.</span></span> 

 `
{
    "hubPattern": "chat",
    "eventPattern": "broadcast",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections1.com"
},
{
    "hubPattern": "*",
    "eventPattern": "*",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections2.com"
}
`

### <span data-ttu-id="5b2ef-113">Alle Upstream-Einstellungen löschen</span><span class="sxs-lookup"><span data-stu-id="5b2ef-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="5b2ef-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b2ef-114">PARAMETERS</span></span>

### <span data-ttu-id="5b2ef-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b2ef-115">-AsJob</span></span>
<span data-ttu-id="5b2ef-116">Führen Sie das Cmdlet im Hintergrund Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="5b2ef-116">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="5b2ef-117">-Clear</span><span class="sxs-lookup"><span data-stu-id="5b2ef-117">-Clear</span></span>
<span data-ttu-id="5b2ef-118">Deaktivieren Sie alle Upstream-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="5b2ef-118">Clear all the upstream settings.</span></span>

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

### <span data-ttu-id="5b2ef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b2ef-119">-DefaultProfile</span></span>
<span data-ttu-id="5b2ef-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5b2ef-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b2ef-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5b2ef-121">-InputObject</span></span>
<span data-ttu-id="5b2ef-122">Das Resource-Objekt des Signals.</span><span class="sxs-lookup"><span data-stu-id="5b2ef-122">The SignalR resource object.</span></span>

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

### <span data-ttu-id="5b2ef-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5b2ef-123">-Name</span></span>
<span data-ttu-id="5b2ef-124">Der Name des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="5b2ef-124">The SignalR service name.</span></span>

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

### <span data-ttu-id="5b2ef-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b2ef-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b2ef-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5b2ef-126">The resource group name.</span></span>
<span data-ttu-id="5b2ef-127">Wenn nicht angegeben, wird der Standardwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b2ef-127">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="5b2ef-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5b2ef-128">-ResourceId</span></span>
<span data-ttu-id="5b2ef-129">Die Ressourcen-ID des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="5b2ef-129">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="5b2ef-130">-Vorlage</span><span class="sxs-lookup"><span data-stu-id="5b2ef-130">-Template</span></span>
<span data-ttu-id="5b2ef-131">Vorlagenelement (e) für Upstream-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="5b2ef-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="5b2ef-132">Erforderlicher Schlüssel: UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="5b2ef-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="5b2ef-133">Optionale Schlüssel: HubPattern, EventPattern, CategoryPattern.</span><span class="sxs-lookup"><span data-stu-id="5b2ef-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="5b2ef-134">Beispiel für die Verwendung der splatting-Syntax zum Übergeben von Vorlagenparameter: @ {UrlTemplate = ' http://host-connections1.com ', HubPattern = ' Chat '; EventPattern = ' Broadcast '}, @ {UrlTemplate = ' http://host-connections2.com '}</span><span class="sxs-lookup"><span data-stu-id="5b2ef-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2ef-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5b2ef-135">-Confirm</span></span>
<span data-ttu-id="5b2ef-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b2ef-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b2ef-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b2ef-137">-WhatIf</span></span>
<span data-ttu-id="5b2ef-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b2ef-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b2ef-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b2ef-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b2ef-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b2ef-140">CommonParameters</span></span>
<span data-ttu-id="5b2ef-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b2ef-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b2ef-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b2ef-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b2ef-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b2ef-143">INPUTS</span></span>

### <span data-ttu-id="5b2ef-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5b2ef-144">System.String</span></span>

## <span data-ttu-id="5b2ef-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b2ef-145">OUTPUTS</span></span>

### <span data-ttu-id="5b2ef-146">Microsoft. Azure. Commands. signalr. Models. PSServerlessUpstreamSettings</span><span class="sxs-lookup"><span data-stu-id="5b2ef-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="5b2ef-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b2ef-147">NOTES</span></span>

## <span data-ttu-id="5b2ef-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b2ef-148">RELATED LINKS</span></span>

[<span data-ttu-id="5b2ef-149">Verwenden von splatting zum Übergeben von Parametern an Befehle in PowerShell</span><span class="sxs-lookup"><span data-stu-id="5b2ef-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)
