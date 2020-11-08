---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 0d6d3bb99062177e1d75c4ab496562782cf142c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165424"
---
# <span data-ttu-id="b6b8d-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="b6b8d-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="b6b8d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b8d-103">Gibt Informationen zu Trigger-Läufen zurück.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="b6b8d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6b8d-104">SYNTAX</span></span>

### <span data-ttu-id="b6b8d-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b6b8d-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6b8d-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="b6b8d-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6b8d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6b8d-107">DESCRIPTION</span></span>
<span data-ttu-id="b6b8d-108">Der Befehl " **Get-AzSynapseTriggerRun** " gibt detaillierte Informationen zu Trigger-Läufen für den angegebenen Trigger im angegebenen Zeitrahmen zurück.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="b6b8d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6b8d-109">EXAMPLES</span></span>

### <span data-ttu-id="b6b8d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b6b8d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="b6b8d-111">Dieser Befehl zeigt Informationen zu den Läufen für ContosoTrigger im Arbeitsbereich ContosoWorkspace, der zwischen "2018-09-01T21:00" und "2019-09-01T21:00" gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="b6b8d-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b6b8d-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="b6b8d-113">Dieser Befehl zeigt Informationen zu den Läufen für ContosoTrigger im Arbeitsbereich ContosoWorkspace, der zwischen "2018-09-01T21:00" und "2019-09-01T21:00" durch Pipeline gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="b6b8d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6b8d-114">PARAMETERS</span></span>

### <span data-ttu-id="b6b8d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b8d-115">-DefaultProfile</span></span>
<span data-ttu-id="b6b8d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6b8d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b6b8d-117">-Name</span></span>
<span data-ttu-id="b6b8d-118">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-118">The trigger name.</span></span>

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

### <span data-ttu-id="b6b8d-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="b6b8d-119">-RunStartedAfter</span></span>
<span data-ttu-id="b6b8d-120">Die Zeit, zu der oder nach der das Run-Ereignis im Format "ISO 8601" aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="b6b8d-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="b6b8d-121">-RunStartedBefore</span></span>
<span data-ttu-id="b6b8d-122">Die Zeitspanne, zu der das Run-Ereignis im Format "ISO 8601" aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="b6b8d-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b6b8d-123">-WorkspaceName</span></span>
<span data-ttu-id="b6b8d-124">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="b6b8d-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b6b8d-125">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="b6b8d-125">-WorkspaceObject</span></span>
<span data-ttu-id="b6b8d-126">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b6b8d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b8d-127">CommonParameters</span></span>
<span data-ttu-id="b6b8d-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b8d-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6b8d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b8d-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6b8d-130">INPUTS</span></span>

### <span data-ttu-id="b6b8d-131">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b6b8d-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b6b8d-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6b8d-132">OUTPUTS</span></span>

### <span data-ttu-id="b6b8d-133">Microsoft. Azure. Commands. Synapse. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="b6b8d-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="b6b8d-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6b8d-134">NOTES</span></span>

## <span data-ttu-id="b6b8d-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6b8d-135">RELATED LINKS</span></span>
