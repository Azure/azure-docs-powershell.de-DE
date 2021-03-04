---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
ms.openlocfilehash: 4254a301e599dac542a099b9c4f2ebace8929ab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919104"
---
# <span data-ttu-id="6df7a-101">Set-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="6df7a-101">Set-AzSynapseDataFlow</span></span>

## <span data-ttu-id="6df7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6df7a-102">SYNOPSIS</span></span>
<span data-ttu-id="6df7a-103">Erstellt oder aktualisiert einen Datenfluss im Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="6df7a-103">Creates or updates a data flow in workspace.</span></span>

## <span data-ttu-id="6df7a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6df7a-104">SYNTAX</span></span>

### <span data-ttu-id="6df7a-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6df7a-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataFlow -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6df7a-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="6df7a-106">SetByObject</span></span>
```
Set-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6df7a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6df7a-107">DESCRIPTION</span></span>
<span data-ttu-id="6df7a-108">Das **Cmdlet Set-AzSynapseDataFlow** erstellt einen Datenfluss oder aktualisiert einen vorhandenen Datenfluss im Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="6df7a-108">The **Set-AzSynapseDataFlow** cmdlet creates a data flow or updates an existing data flow in workspace.</span></span>

## <span data-ttu-id="6df7a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6df7a-109">EXAMPLES</span></span>

### <span data-ttu-id="6df7a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6df7a-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow -DefinitionFile "C:\\samples\\DataFlow.json"
```

<span data-ttu-id="6df7a-111">Mit diesem Befehl wird ein Datenfluss namens ContosoDataFlow im Arbeitsbereich namens ContosoWorkspace erstellt.</span><span class="sxs-lookup"><span data-stu-id="6df7a-111">This command creates a data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="6df7a-112">Mit dem Befehl wird der Datenfluss auf Informationen in der Datei DataFlow.jsgespeichert.</span><span class="sxs-lookup"><span data-stu-id="6df7a-112">The command bases the data flow on information in the DataFlow.json file.</span></span>

## <span data-ttu-id="6df7a-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6df7a-113">PARAMETERS</span></span>

### <span data-ttu-id="6df7a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6df7a-114">-AsJob</span></span>
<span data-ttu-id="6df7a-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6df7a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6df7a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6df7a-116">-DefaultProfile</span></span>
<span data-ttu-id="6df7a-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6df7a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6df7a-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="6df7a-118">-DefinitionFile</span></span>
<span data-ttu-id="6df7a-119">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="6df7a-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df7a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6df7a-120">-Name</span></span>
<span data-ttu-id="6df7a-121">Der Name des Datenflusses.</span><span class="sxs-lookup"><span data-stu-id="6df7a-121">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df7a-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6df7a-122">-WorkspaceName</span></span>
<span data-ttu-id="6df7a-123">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="6df7a-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df7a-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6df7a-124">-WorkspaceObject</span></span>
<span data-ttu-id="6df7a-125">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6df7a-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6df7a-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6df7a-126">-Confirm</span></span>
<span data-ttu-id="6df7a-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6df7a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6df7a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6df7a-128">-WhatIf</span></span>
<span data-ttu-id="6df7a-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6df7a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6df7a-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6df7a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6df7a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df7a-131">CommonParameters</span></span>
<span data-ttu-id="6df7a-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6df7a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df7a-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6df7a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df7a-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6df7a-134">INPUTS</span></span>

### <span data-ttu-id="6df7a-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6df7a-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6df7a-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6df7a-136">OUTPUTS</span></span>

### <span data-ttu-id="6df7a-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="6df7a-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="6df7a-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6df7a-138">NOTES</span></span>

## <span data-ttu-id="6df7a-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6df7a-139">RELATED LINKS</span></span>
