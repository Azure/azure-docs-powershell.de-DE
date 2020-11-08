---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: d2471320a27b1af96dba6b5e2b552a01ff5b50e3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173664"
---
# <span data-ttu-id="af590-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="af590-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="af590-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="af590-102">SYNOPSIS</span></span>
<span data-ttu-id="af590-103">Erstellt oder aktualisiert ein DataSet im Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="af590-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="af590-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="af590-104">SYNTAX</span></span>

### <span data-ttu-id="af590-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="af590-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af590-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="af590-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af590-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af590-107">DESCRIPTION</span></span>
<span data-ttu-id="af590-108">Das Cmdlet " **Satz-AzSynapseDataset** " erstellt ein DataSet oder aktualisiert ein vorhandenes Dataset im Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="af590-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="af590-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="af590-109">EXAMPLES</span></span>

### <span data-ttu-id="af590-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="af590-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="af590-111">Dieser Befehl erstellt ein DataSet mit dem Namen ContosoDataset im Arbeitsbereich mit dem Namen ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="af590-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="af590-112">Der Befehl unterstützt das Dataset auf Informationen in der Dataset.jsfür die Datei.</span><span class="sxs-lookup"><span data-stu-id="af590-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="af590-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="af590-113">PARAMETERS</span></span>

### <span data-ttu-id="af590-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af590-114">-AsJob</span></span>
<span data-ttu-id="af590-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="af590-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af590-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af590-116">-DefaultProfile</span></span>
<span data-ttu-id="af590-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="af590-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af590-118">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="af590-118">-DefinitionFile</span></span>
<span data-ttu-id="af590-119">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="af590-119">The JSON file path.</span></span>

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

### <span data-ttu-id="af590-120">-Name</span><span class="sxs-lookup"><span data-stu-id="af590-120">-Name</span></span>
<span data-ttu-id="af590-121">Der Name des Datasets.</span><span class="sxs-lookup"><span data-stu-id="af590-121">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af590-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="af590-122">-WorkspaceName</span></span>
<span data-ttu-id="af590-123">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="af590-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="af590-124">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="af590-124">-WorkspaceObject</span></span>
<span data-ttu-id="af590-125">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="af590-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="af590-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="af590-126">-Confirm</span></span>
<span data-ttu-id="af590-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="af590-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af590-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af590-128">-WhatIf</span></span>
<span data-ttu-id="af590-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af590-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af590-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="af590-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af590-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af590-131">CommonParameters</span></span>
<span data-ttu-id="af590-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af590-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af590-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af590-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af590-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="af590-134">INPUTS</span></span>

### <span data-ttu-id="af590-135">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="af590-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="af590-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="af590-136">OUTPUTS</span></span>

### <span data-ttu-id="af590-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="af590-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="af590-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="af590-138">NOTES</span></span>

## <span data-ttu-id="af590-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="af590-139">RELATED LINKS</span></span>
