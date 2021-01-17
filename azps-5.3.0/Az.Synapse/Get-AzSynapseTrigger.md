---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
ms.openlocfilehash: 9e39d6458ca330909e500a45532d0a9d66f404af
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383745"
---
# <span data-ttu-id="c6985-101">Get-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="c6985-101">Get-AzSynapseTrigger</span></span>

## <span data-ttu-id="c6985-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6985-102">SYNOPSIS</span></span>
<span data-ttu-id="c6985-103">Ruft Informationen zu Triggern in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="c6985-103">Gets information about triggers in a workspace.</span></span>

## <span data-ttu-id="c6985-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6985-104">SYNTAX</span></span>

### <span data-ttu-id="c6985-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c6985-105">GetByName (Default)</span></span>
```
Get-AzSynapseTrigger -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6985-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="c6985-106">GetByObject</span></span>
```
Get-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6985-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6985-107">DESCRIPTION</span></span>
<span data-ttu-id="c6985-108">Das **Cmdlet "Get-AzSynapseTrigger"** ruft Informationen zu Triggern in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="c6985-108">The **Get-AzSynapseTrigger** cmdlet gets information about triggers in a workspace.</span></span> <span data-ttu-id="c6985-109">Wenn Sie den Namen eines Triggers angeben, ruft das Cmdlet Informationen zu diesem Trigger ab.</span><span class="sxs-lookup"><span data-stu-id="c6985-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="c6985-110">Wenn Sie keinen Namen angeben, ruft das Cmdlet Informationen zu allen Triggern im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="c6985-110">If you do not specify a name, the cmdlet gets information about all triggers in the workspace.</span></span>

## <span data-ttu-id="c6985-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c6985-111">EXAMPLES</span></span>

### <span data-ttu-id="c6985-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c6985-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="c6985-113">Ruft eine Liste aller Trigger ab, die im Arbeitsbereich "ContosoWorkspace" erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="c6985-113">Gets a list of all triggers that have been created in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="c6985-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c6985-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="c6985-115">Ruft einen einzelnen Trigger namens "ContosoTrigger" im Arbeitsbereich "ContosoWorkspace" ab.</span><span class="sxs-lookup"><span data-stu-id="c6985-115">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="c6985-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c6985-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="c6985-117">Ruft einen einzelnen Trigger namens "ContosoTrigger" im Arbeitsbereich "ContosoWorkspace" über die Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="c6985-117">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="c6985-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6985-118">PARAMETERS</span></span>

### <span data-ttu-id="c6985-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6985-119">-DefaultProfile</span></span>
<span data-ttu-id="c6985-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6985-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6985-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c6985-121">-Name</span></span>
<span data-ttu-id="c6985-122">Der Auslösername.</span><span class="sxs-lookup"><span data-stu-id="c6985-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6985-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c6985-123">-WorkspaceName</span></span>
<span data-ttu-id="c6985-124">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="c6985-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c6985-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c6985-125">-WorkspaceObject</span></span>
<span data-ttu-id="c6985-126">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c6985-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c6985-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6985-127">CommonParameters</span></span>
<span data-ttu-id="c6985-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6985-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6985-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6985-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6985-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c6985-130">INPUTS</span></span>

### <span data-ttu-id="c6985-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c6985-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c6985-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c6985-132">OUTPUTS</span></span>

### <span data-ttu-id="c6985-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="c6985-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="c6985-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c6985-134">NOTES</span></span>

## <span data-ttu-id="c6985-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c6985-135">RELATED LINKS</span></span>
