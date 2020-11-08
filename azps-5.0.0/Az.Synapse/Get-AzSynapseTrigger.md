---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
ms.openlocfilehash: 9e39d6458ca330909e500a45532d0a9d66f404af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178123"
---
# <span data-ttu-id="d4953-101">Get-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="d4953-101">Get-AzSynapseTrigger</span></span>

## <span data-ttu-id="d4953-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4953-102">SYNOPSIS</span></span>
<span data-ttu-id="d4953-103">Ruft Informationen zu Triggern in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="d4953-103">Gets information about triggers in a workspace.</span></span>

## <span data-ttu-id="d4953-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4953-104">SYNTAX</span></span>

### <span data-ttu-id="d4953-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4953-105">GetByName (Default)</span></span>
```
Get-AzSynapseTrigger -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4953-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="d4953-106">GetByObject</span></span>
```
Get-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4953-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4953-107">DESCRIPTION</span></span>
<span data-ttu-id="d4953-108">Das Cmdlet " **Get-AzSynapseTrigger** " Ruft Informationen zu Triggern in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="d4953-108">The **Get-AzSynapseTrigger** cmdlet gets information about triggers in a workspace.</span></span> <span data-ttu-id="d4953-109">Wenn Sie den Namen eines Triggers angeben, ruft das Cmdlet Informationen zu diesem Trigger ab.</span><span class="sxs-lookup"><span data-stu-id="d4953-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="d4953-110">Wenn Sie keinen Namen angeben, ruft das Cmdlet Informationen zu allen Triggern im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="d4953-110">If you do not specify a name, the cmdlet gets information about all triggers in the workspace.</span></span>

## <span data-ttu-id="d4953-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4953-111">EXAMPLES</span></span>

### <span data-ttu-id="d4953-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d4953-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="d4953-113">Ruft eine Liste aller Trigger ab, die im Arbeitsbereichs-ContosoWorkspace erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="d4953-113">Gets a list of all triggers that have been created in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="d4953-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d4953-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="d4953-115">Ruft einen einzelnen Trigger namens ContosoTrigger im Arbeitsbereich ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="d4953-115">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="d4953-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d4953-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="d4953-117">Ruft einen einzelnen Trigger mit dem Namen ContosoTrigger im Arbeitsbereich ContosoWorkspace through-Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="d4953-117">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d4953-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4953-118">PARAMETERS</span></span>

### <span data-ttu-id="d4953-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4953-119">-DefaultProfile</span></span>
<span data-ttu-id="d4953-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4953-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4953-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d4953-121">-Name</span></span>
<span data-ttu-id="d4953-122">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="d4953-122">The trigger name.</span></span>

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

### <span data-ttu-id="d4953-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d4953-123">-WorkspaceName</span></span>
<span data-ttu-id="d4953-124">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="d4953-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d4953-125">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="d4953-125">-WorkspaceObject</span></span>
<span data-ttu-id="d4953-126">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="d4953-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d4953-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4953-127">CommonParameters</span></span>
<span data-ttu-id="d4953-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4953-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4953-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4953-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4953-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4953-130">INPUTS</span></span>

### <span data-ttu-id="d4953-131">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d4953-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d4953-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4953-132">OUTPUTS</span></span>

### <span data-ttu-id="d4953-133">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="d4953-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="d4953-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4953-134">NOTES</span></span>

## <span data-ttu-id="d4953-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4953-135">RELATED LINKS</span></span>
