---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 284974cc2d4cb98519b82c5c5a50e40d323dc354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931587"
---
# <span data-ttu-id="53826-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="53826-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="53826-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53826-102">SYNOPSIS</span></span>
<span data-ttu-id="53826-103">Gibt Informationen zu Triggerläufen zurück.</span><span class="sxs-lookup"><span data-stu-id="53826-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="53826-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53826-104">SYNTAX</span></span>

### <span data-ttu-id="53826-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="53826-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53826-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="53826-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53826-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53826-107">DESCRIPTION</span></span>
<span data-ttu-id="53826-108">Der **Befehl Get-AzSynapseTriggerRun** gibt detaillierte Informationen zu Triggerläufen für den angegebenen Trigger im angegebenen Zeitrahmen zurück.</span><span class="sxs-lookup"><span data-stu-id="53826-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="53826-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="53826-109">EXAMPLES</span></span>

### <span data-ttu-id="53826-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="53826-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="53826-111">Dieser Befehl zeigt Informationen zu den Ausgeführten für ContosoTrigger im Arbeitsbereich ContosoWorkspace an, der zwischen "2018-09-01T21:00" und "2019-09-01T21:00" gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="53826-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="53826-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="53826-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="53826-113">Dieser Befehl zeigt Informationen zu den Ausgeführten für ContosoTrigger im Arbeitsbereich ContosoWorkspace an, der zwischen "2018-09-01T21:00" und "2019-09-01T21:00" über die Pipeline gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="53826-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="53826-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="53826-114">PARAMETERS</span></span>

### <span data-ttu-id="53826-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53826-115">-DefaultProfile</span></span>
<span data-ttu-id="53826-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="53826-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53826-117">-Name</span><span class="sxs-lookup"><span data-stu-id="53826-117">-Name</span></span>
<span data-ttu-id="53826-118">Der Triggername.</span><span class="sxs-lookup"><span data-stu-id="53826-118">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53826-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="53826-119">-RunStartedAfter</span></span>
<span data-ttu-id="53826-120">Die Uhrzeit, zu oder nach der das Ausführungsereignis im Format "ISO 8601" aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="53826-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53826-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="53826-121">-RunStartedBefore</span></span>
<span data-ttu-id="53826-122">Der Zeitpunkt, zu dem oder vor dem das Ausführungsereignis im Format "ISO 8601" aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="53826-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53826-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="53826-123">-WorkspaceName</span></span>
<span data-ttu-id="53826-124">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="53826-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53826-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="53826-125">-WorkspaceObject</span></span>
<span data-ttu-id="53826-126">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="53826-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53826-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53826-127">CommonParameters</span></span>
<span data-ttu-id="53826-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53826-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53826-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53826-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53826-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="53826-130">INPUTS</span></span>

### <span data-ttu-id="53826-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="53826-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="53826-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="53826-132">OUTPUTS</span></span>

### <span data-ttu-id="53826-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="53826-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="53826-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="53826-134">NOTES</span></span>

## <span data-ttu-id="53826-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="53826-135">RELATED LINKS</span></span>
