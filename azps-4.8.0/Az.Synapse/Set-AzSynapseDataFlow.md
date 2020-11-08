---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
ms.openlocfilehash: 4147343b01e53050f88429424ca7a9c70aa445c6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173666"
---
# <span data-ttu-id="eec65-101">Set-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="eec65-101">Set-AzSynapseDataFlow</span></span>

## <span data-ttu-id="eec65-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eec65-102">SYNOPSIS</span></span>
<span data-ttu-id="eec65-103">Erstellt oder aktualisiert einen Datenfluss im Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="eec65-103">Creates or updates a data flow in workspace.</span></span>

## <span data-ttu-id="eec65-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eec65-104">SYNTAX</span></span>

### <span data-ttu-id="eec65-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="eec65-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataFlow -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eec65-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="eec65-106">SetByObject</span></span>
```
Set-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eec65-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eec65-107">DESCRIPTION</span></span>
<span data-ttu-id="eec65-108">Das Cmdlet " **Satz-AzSynapseDataFlow** " erstellt einen Datenfluss oder aktualisiert einen vorhandenen Datenfluss im Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="eec65-108">The **Set-AzSynapseDataFlow** cmdlet creates a data flow or updates an existing data flow in workspace.</span></span>

## <span data-ttu-id="eec65-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eec65-109">EXAMPLES</span></span>

### <span data-ttu-id="eec65-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eec65-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow -DefinitionFile "C:\\samples\\DataFlow.json"
```

<span data-ttu-id="eec65-111">Dieser Befehl erstellt einen Datenfluss mit dem Namen ContosoDataFlow im Arbeitsbereich mit dem Namen ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="eec65-111">This command creates a data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="eec65-112">Der Befehl basiert den Datenfluss auf Informationen in der DataFlow.jsDatei.</span><span class="sxs-lookup"><span data-stu-id="eec65-112">The command bases the data flow on information in the DataFlow.json file.</span></span>

## <span data-ttu-id="eec65-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="eec65-113">PARAMETERS</span></span>

### <span data-ttu-id="eec65-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eec65-114">-AsJob</span></span>
<span data-ttu-id="eec65-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="eec65-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eec65-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec65-116">-DefaultProfile</span></span>
<span data-ttu-id="eec65-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eec65-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eec65-118">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="eec65-118">-DefinitionFile</span></span>
<span data-ttu-id="eec65-119">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="eec65-119">The JSON file path.</span></span>

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

### <span data-ttu-id="eec65-120">-Name</span><span class="sxs-lookup"><span data-stu-id="eec65-120">-Name</span></span>
<span data-ttu-id="eec65-121">Der Name des Datenflusses.</span><span class="sxs-lookup"><span data-stu-id="eec65-121">The data flow name.</span></span>

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

### <span data-ttu-id="eec65-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="eec65-122">-WorkspaceName</span></span>
<span data-ttu-id="eec65-123">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="eec65-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="eec65-124">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="eec65-124">-WorkspaceObject</span></span>
<span data-ttu-id="eec65-125">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="eec65-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="eec65-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eec65-126">-Confirm</span></span>
<span data-ttu-id="eec65-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eec65-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eec65-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eec65-128">-WhatIf</span></span>
<span data-ttu-id="eec65-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eec65-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eec65-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eec65-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eec65-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec65-131">CommonParameters</span></span>
<span data-ttu-id="eec65-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eec65-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec65-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eec65-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec65-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eec65-134">INPUTS</span></span>

### <span data-ttu-id="eec65-135">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="eec65-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="eec65-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eec65-136">OUTPUTS</span></span>

### <span data-ttu-id="eec65-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="eec65-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="eec65-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="eec65-138">NOTES</span></span>

## <span data-ttu-id="eec65-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eec65-139">RELATED LINKS</span></span>
