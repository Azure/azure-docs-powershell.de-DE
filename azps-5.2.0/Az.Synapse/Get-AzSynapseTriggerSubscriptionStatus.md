---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: b18a308b94bdb486945186c67c3a905bcb0408d3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359301"
---
# <span data-ttu-id="b69bc-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="b69bc-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="b69bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b69bc-102">SYNOPSIS</span></span>
<span data-ttu-id="b69bc-103">Den Status des Abonnements für den Ereignistrigger für die angegebenen Externen Dienstereignisse erhalten.</span><span class="sxs-lookup"><span data-stu-id="b69bc-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="b69bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b69bc-104">SYNTAX</span></span>

### <span data-ttu-id="b69bc-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b69bc-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b69bc-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="b69bc-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b69bc-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="b69bc-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b69bc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b69bc-108">DESCRIPTION</span></span>
<span data-ttu-id="b69bc-109">Das **Cmdlet "Get-AzSynapseTriggerSubscriptionStatus"** ruft den Status des Abonnements für den Ereignistrigger für die angegebenen externen Dienstereignisse ab.</span><span class="sxs-lookup"><span data-stu-id="b69bc-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="b69bc-110">Der Trigger kann erst gestartet werden, wenn der zurückgegebene Status "Aktiviert" ist.</span><span class="sxs-lookup"><span data-stu-id="b69bc-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="b69bc-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b69bc-111">EXAMPLES</span></span>

### <span data-ttu-id="b69bc-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b69bc-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="b69bc-113">Mit diesem Befehl wird der Status der Abonnementunterschrift für den Trigger "ContosoTrigger" für die externen Dienstereignisse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b69bc-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="b69bc-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b69bc-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="b69bc-115">Mit diesem Befehl wird der Status des Triggers "ContosoTrigger" für die externen Dienstereignisse über die Pipeline angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b69bc-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="b69bc-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b69bc-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="b69bc-117">Mit diesem Befehl wird der Status des Triggers "ContosoTrigger" für die externen Dienstereignisse über die Pipeline angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b69bc-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="b69bc-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b69bc-118">PARAMETERS</span></span>

### <span data-ttu-id="b69bc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b69bc-119">-DefaultProfile</span></span>
<span data-ttu-id="b69bc-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b69bc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b69bc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b69bc-121">-InputObject</span></span>
<span data-ttu-id="b69bc-122">Das Triggerobjekt.</span><span class="sxs-lookup"><span data-stu-id="b69bc-122">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b69bc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b69bc-123">-Name</span></span>
<span data-ttu-id="b69bc-124">Der Auslösername.</span><span class="sxs-lookup"><span data-stu-id="b69bc-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, GetByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b69bc-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b69bc-125">-WorkspaceName</span></span>
<span data-ttu-id="b69bc-126">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="b69bc-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b69bc-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b69bc-127">-WorkspaceObject</span></span>
<span data-ttu-id="b69bc-128">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b69bc-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b69bc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b69bc-129">CommonParameters</span></span>
<span data-ttu-id="b69bc-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b69bc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b69bc-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b69bc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b69bc-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b69bc-132">INPUTS</span></span>

### <span data-ttu-id="b69bc-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b69bc-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b69bc-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="b69bc-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="b69bc-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b69bc-135">OUTPUTS</span></span>

### <span data-ttu-id="b69bc-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span><span class="sxs-lookup"><span data-stu-id="b69bc-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="b69bc-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b69bc-137">NOTES</span></span>

## <span data-ttu-id="b69bc-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b69bc-138">RELATED LINKS</span></span>
