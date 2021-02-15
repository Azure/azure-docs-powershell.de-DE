---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: e04e87067f86f529117512e7443118f308b20547
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173929"
---
# <span data-ttu-id="348e6-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="348e6-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="348e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="348e6-102">SYNOPSIS</span></span>
<span data-ttu-id="348e6-103">Legen Sie die Upstreameinstellungen eines SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="348e6-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="348e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="348e6-104">SYNTAX</span></span>

### <span data-ttu-id="348e6-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="348e6-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="348e6-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="348e6-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="348e6-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="348e6-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="348e6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="348e6-108">DESCRIPTION</span></span>
<span data-ttu-id="348e6-109">Legen Sie die Upstreameinstellungen eines SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="348e6-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="348e6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="348e6-110">EXAMPLES</span></span>

### <span data-ttu-id="348e6-111">Festlegen von zwei geordneten Upstreamvorlagen</span><span class="sxs-lookup"><span data-stu-id="348e6-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="348e6-112">Der folgende JSON stellt die tatsächlichen Vorlagen dar.</span><span class="sxs-lookup"><span data-stu-id="348e6-112">The following JSON represents the actual templates set.</span></span> 

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

### <span data-ttu-id="348e6-113">Löschen aller Upstreameinstellungen</span><span class="sxs-lookup"><span data-stu-id="348e6-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="348e6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="348e6-114">PARAMETERS</span></span>

### <span data-ttu-id="348e6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="348e6-115">-AsJob</span></span>
<span data-ttu-id="348e6-116">Führen Sie das Cmdlet im Hintergrundauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="348e6-116">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="348e6-117">-Clear</span><span class="sxs-lookup"><span data-stu-id="348e6-117">-Clear</span></span>
<span data-ttu-id="348e6-118">Löschen Sie alle Upstreameinstellungen.</span><span class="sxs-lookup"><span data-stu-id="348e6-118">Clear all the upstream settings.</span></span>

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

### <span data-ttu-id="348e6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="348e6-119">-DefaultProfile</span></span>
<span data-ttu-id="348e6-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="348e6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="348e6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="348e6-121">-InputObject</span></span>
<span data-ttu-id="348e6-122">Das SignalR-Ressourcenobjekt.</span><span class="sxs-lookup"><span data-stu-id="348e6-122">The SignalR resource object.</span></span>

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

### <span data-ttu-id="348e6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="348e6-123">-Name</span></span>
<span data-ttu-id="348e6-124">Der Name des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="348e6-124">The SignalR service name.</span></span>

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

### <span data-ttu-id="348e6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="348e6-125">-ResourceGroupName</span></span>
<span data-ttu-id="348e6-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="348e6-126">The resource group name.</span></span>
<span data-ttu-id="348e6-127">Die Standardeinstellung wird verwendet, wenn sie nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="348e6-127">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="348e6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="348e6-128">-ResourceId</span></span>
<span data-ttu-id="348e6-129">Die Ressourcen-ID des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="348e6-129">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="348e6-130">-Template</span><span class="sxs-lookup"><span data-stu-id="348e6-130">-Template</span></span>
<span data-ttu-id="348e6-131">Vorlagenelement(en) für Upstreameinstellungen.</span><span class="sxs-lookup"><span data-stu-id="348e6-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="348e6-132">Erforderlicher Schlüssel: UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="348e6-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="348e6-133">Optionale Schlüssel: HubPattern, EventPattern, CategoryPattern.</span><span class="sxs-lookup"><span data-stu-id="348e6-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="348e6-134">Beispiel für die Verwendung der Plattformsyntax zum Übergeben von Vorlagenparametern: @{UrlTemplate=' http://host-connections1.com ', HubPattern= 'chat'; EventPattern='broadcast' },@{UrlTemplate=' http://host-connections2.com '}</span><span class="sxs-lookup"><span data-stu-id="348e6-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

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

### <span data-ttu-id="348e6-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="348e6-135">-Confirm</span></span>
<span data-ttu-id="348e6-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="348e6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="348e6-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="348e6-137">-WhatIf</span></span>
<span data-ttu-id="348e6-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="348e6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="348e6-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="348e6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="348e6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="348e6-140">CommonParameters</span></span>
<span data-ttu-id="348e6-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="348e6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="348e6-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="348e6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="348e6-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="348e6-143">INPUTS</span></span>

### <span data-ttu-id="348e6-144">System.String</span><span class="sxs-lookup"><span data-stu-id="348e6-144">System.String</span></span>

## <span data-ttu-id="348e6-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="348e6-145">OUTPUTS</span></span>

### <span data-ttu-id="348e6-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span><span class="sxs-lookup"><span data-stu-id="348e6-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="348e6-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="348e6-147">NOTES</span></span>

## <span data-ttu-id="348e6-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="348e6-148">RELATED LINKS</span></span>

[<span data-ttu-id="348e6-149">So wird's ausgeführt: Verwenden der Plattform zum Übergeben von Parametern an Befehle in PowerShell</span><span class="sxs-lookup"><span data-stu-id="348e6-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)
