---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
ms.openlocfilehash: 1e05754245b4179d02c144538473fa586531f95c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946391"
---
# <span data-ttu-id="970e1-101">Set-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="970e1-101">Set-AzSynapseLinkedService</span></span>

## <span data-ttu-id="970e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="970e1-102">SYNOPSIS</span></span>
<span data-ttu-id="970e1-103">Verknüpft einen Datenspeicher oder einen Clouddienst mit einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="970e1-103">Links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="970e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="970e1-104">SYNTAX</span></span>

### <span data-ttu-id="970e1-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="970e1-105">SetByName (Default)</span></span>
```
Set-AzSynapseLinkedService -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="970e1-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="970e1-106">SetByObject</span></span>
```
Set-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="970e1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="970e1-107">DESCRIPTION</span></span>
<span data-ttu-id="970e1-108">Das **Cmdlet Set-AzSynapseLinkedService** verknüpft einen Datenspeicher oder einen Clouddienst mit dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="970e1-108">The **Set-AzSynapseLinkedService** cmdlet links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="970e1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="970e1-109">EXAMPLES</span></span>

### <span data-ttu-id="970e1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="970e1-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="970e1-111">Mit diesem Befehl wird ein verknüpfter Dienst namens ContosoLinkedService im Arbeitsbereich namens ContosoWorkspace erstellt.</span><span class="sxs-lookup"><span data-stu-id="970e1-111">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="970e1-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="970e1-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseLinkedService -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="970e1-113">Mit diesem Befehl wird ein verknüpfter Dienst namens ContosoLinkedService im Arbeitsbereich namens ContosoWorkspace über pipeline erstellt.</span><span class="sxs-lookup"><span data-stu-id="970e1-113">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="970e1-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="970e1-114">PARAMETERS</span></span>

### <span data-ttu-id="970e1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="970e1-115">-AsJob</span></span>
<span data-ttu-id="970e1-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="970e1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="970e1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="970e1-117">-DefaultProfile</span></span>
<span data-ttu-id="970e1-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="970e1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="970e1-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="970e1-119">-DefinitionFile</span></span>
<span data-ttu-id="970e1-120">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="970e1-120">The JSON file path.</span></span>

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

### <span data-ttu-id="970e1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="970e1-121">-Name</span></span>
<span data-ttu-id="970e1-122">Der name des verknüpften Diensts.</span><span class="sxs-lookup"><span data-stu-id="970e1-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="970e1-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="970e1-123">-WorkspaceName</span></span>
<span data-ttu-id="970e1-124">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="970e1-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="970e1-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="970e1-125">-WorkspaceObject</span></span>
<span data-ttu-id="970e1-126">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="970e1-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="970e1-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="970e1-127">-Confirm</span></span>
<span data-ttu-id="970e1-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="970e1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="970e1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="970e1-129">-WhatIf</span></span>
<span data-ttu-id="970e1-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="970e1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="970e1-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="970e1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="970e1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="970e1-132">CommonParameters</span></span>
<span data-ttu-id="970e1-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="970e1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="970e1-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="970e1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="970e1-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="970e1-135">INPUTS</span></span>

### <span data-ttu-id="970e1-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="970e1-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="970e1-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="970e1-137">OUTPUTS</span></span>

### <span data-ttu-id="970e1-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="970e1-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="970e1-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="970e1-139">NOTES</span></span>

## <span data-ttu-id="970e1-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="970e1-140">RELATED LINKS</span></span>
