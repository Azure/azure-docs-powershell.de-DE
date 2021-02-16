---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
ms.openlocfilehash: 635c1e064dbc081a5207f5c912c14166b2b01e17
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156017"
---
# <span data-ttu-id="fbab7-101">Set-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="fbab7-101">Set-AzSynapseLinkedService</span></span>

## <span data-ttu-id="fbab7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbab7-102">SYNOPSIS</span></span>
<span data-ttu-id="fbab7-103">Verknüpft einen Datenspeicher oder einen Clouddienst mit einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="fbab7-103">Links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="fbab7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbab7-104">SYNTAX</span></span>

### <span data-ttu-id="fbab7-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fbab7-105">SetByName (Default)</span></span>
```
Set-AzSynapseLinkedService -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbab7-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="fbab7-106">SetByObject</span></span>
```
Set-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbab7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbab7-107">DESCRIPTION</span></span>
<span data-ttu-id="fbab7-108">Das **Cmdlet "Set-AzSynapseLinkedService"** verknüpft einen Datenspeicher oder einen Clouddienst mit einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="fbab7-108">The **Set-AzSynapseLinkedService** cmdlet links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="fbab7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fbab7-109">EXAMPLES</span></span>

### <span data-ttu-id="fbab7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fbab7-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="fbab7-111">Mit diesem Befehl wird ein verknüpfter Dienst namens "ContosoLinkedService" im Arbeitsbereich "ContosoWorkspace" erstellt.</span><span class="sxs-lookup"><span data-stu-id="fbab7-111">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="fbab7-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fbab7-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseLinkedService -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="fbab7-113">Mit diesem Befehl wird im Arbeitsbereich mit dem Namen "ContosoWorkspace" über die Pipeline ein verknüpfter Dienst namens "ContosoLinkedService" erstellt.</span><span class="sxs-lookup"><span data-stu-id="fbab7-113">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="fbab7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbab7-114">PARAMETERS</span></span>

### <span data-ttu-id="fbab7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbab7-115">-AsJob</span></span>
<span data-ttu-id="fbab7-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fbab7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fbab7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbab7-117">-DefaultProfile</span></span>
<span data-ttu-id="fbab7-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbab7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbab7-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="fbab7-119">-DefinitionFile</span></span>
<span data-ttu-id="fbab7-120">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="fbab7-120">The JSON file path.</span></span>

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

### <span data-ttu-id="fbab7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fbab7-121">-Name</span></span>
<span data-ttu-id="fbab7-122">Der Name des verknüpften Diensts.</span><span class="sxs-lookup"><span data-stu-id="fbab7-122">The linked service name.</span></span>

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

### <span data-ttu-id="fbab7-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fbab7-123">-WorkspaceName</span></span>
<span data-ttu-id="fbab7-124">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="fbab7-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fbab7-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fbab7-125">-WorkspaceObject</span></span>
<span data-ttu-id="fbab7-126">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="fbab7-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fbab7-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbab7-127">-Confirm</span></span>
<span data-ttu-id="fbab7-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fbab7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbab7-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fbab7-129">-WhatIf</span></span>
<span data-ttu-id="fbab7-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fbab7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbab7-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fbab7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbab7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbab7-132">CommonParameters</span></span>
<span data-ttu-id="fbab7-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbab7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbab7-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbab7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbab7-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fbab7-135">INPUTS</span></span>

### <span data-ttu-id="fbab7-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fbab7-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="fbab7-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fbab7-137">OUTPUTS</span></span>

### <span data-ttu-id="fbab7-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="fbab7-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="fbab7-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fbab7-139">NOTES</span></span>

## <span data-ttu-id="fbab7-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fbab7-140">RELATED LINKS</span></span>
