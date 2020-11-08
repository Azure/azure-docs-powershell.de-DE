---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
ms.openlocfilehash: 635c1e064dbc081a5207f5c912c14166b2b01e17
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176366"
---
# <span data-ttu-id="077f6-101">Set-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="077f6-101">Set-AzSynapseLinkedService</span></span>

## <span data-ttu-id="077f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="077f6-102">SYNOPSIS</span></span>
<span data-ttu-id="077f6-103">Verknüpft einen Datenspeicher oder einen clouddienst mit einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="077f6-103">Links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="077f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="077f6-104">SYNTAX</span></span>

### <span data-ttu-id="077f6-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="077f6-105">SetByName (Default)</span></span>
```
Set-AzSynapseLinkedService -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="077f6-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="077f6-106">SetByObject</span></span>
```
Set-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="077f6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="077f6-107">DESCRIPTION</span></span>
<span data-ttu-id="077f6-108">Das Cmdlet " **Satz-AzSynapseLinkedService** " verknüpft einen Datenspeicher oder einen clouddienst mit einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="077f6-108">The **Set-AzSynapseLinkedService** cmdlet links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="077f6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="077f6-109">EXAMPLES</span></span>

### <span data-ttu-id="077f6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="077f6-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="077f6-111">Dieser Befehl erstellt einen verknüpften Dienst mit dem Namen ContosoLinkedService im Arbeitsbereich mit dem Namen ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="077f6-111">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="077f6-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="077f6-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseLinkedService -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="077f6-113">Dieser Befehl erstellt einen verknüpften Dienst mit dem Namen ContosoLinkedService im Arbeitsbereich mit dem Namen ContosoWorkspace through Pipeline.</span><span class="sxs-lookup"><span data-stu-id="077f6-113">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="077f6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="077f6-114">PARAMETERS</span></span>

### <span data-ttu-id="077f6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="077f6-115">-AsJob</span></span>
<span data-ttu-id="077f6-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="077f6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="077f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="077f6-117">-DefaultProfile</span></span>
<span data-ttu-id="077f6-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="077f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="077f6-119">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="077f6-119">-DefinitionFile</span></span>
<span data-ttu-id="077f6-120">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="077f6-120">The JSON file path.</span></span>

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

### <span data-ttu-id="077f6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="077f6-121">-Name</span></span>
<span data-ttu-id="077f6-122">Der Name des verknüpften Diensts.</span><span class="sxs-lookup"><span data-stu-id="077f6-122">The linked service name.</span></span>

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

### <span data-ttu-id="077f6-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="077f6-123">-WorkspaceName</span></span>
<span data-ttu-id="077f6-124">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="077f6-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="077f6-125">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="077f6-125">-WorkspaceObject</span></span>
<span data-ttu-id="077f6-126">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="077f6-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="077f6-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="077f6-127">-Confirm</span></span>
<span data-ttu-id="077f6-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="077f6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="077f6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="077f6-129">-WhatIf</span></span>
<span data-ttu-id="077f6-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="077f6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="077f6-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="077f6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="077f6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="077f6-132">CommonParameters</span></span>
<span data-ttu-id="077f6-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="077f6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="077f6-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="077f6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="077f6-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="077f6-135">INPUTS</span></span>

### <span data-ttu-id="077f6-136">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="077f6-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="077f6-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="077f6-137">OUTPUTS</span></span>

### <span data-ttu-id="077f6-138">Microsoft. Azure. Commands. Synapse. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="077f6-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="077f6-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="077f6-139">NOTES</span></span>

## <span data-ttu-id="077f6-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="077f6-140">RELATED LINKS</span></span>
