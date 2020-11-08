---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 87627738967a5c3174020932e5c9e7b996980ee9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176707"
---
# <span data-ttu-id="fd586-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="fd586-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="fd586-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd586-102">SYNOPSIS</span></span>
<span data-ttu-id="fd586-103">Ruft Informationen zu Datenflüssen im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="fd586-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="fd586-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd586-104">SYNTAX</span></span>

### <span data-ttu-id="fd586-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd586-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fd586-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="fd586-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd586-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd586-107">DESCRIPTION</span></span>
<span data-ttu-id="fd586-108">Das Cmdlet " **Get-AzSynapseDataFlow** " Ruft Informationen zu Datenflüssen im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="fd586-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="fd586-109">Wenn Sie den Namen eines Datenflusses angeben, ruft dieses Cmdlet Informationen zu diesem Datenfluss ab.</span><span class="sxs-lookup"><span data-stu-id="fd586-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="fd586-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datenflüssen im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="fd586-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="fd586-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd586-111">EXAMPLES</span></span>

### <span data-ttu-id="fd586-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fd586-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="fd586-113">Dieser Befehl ruft Informationen zu allen Datenflüssen im Arbeitsbereich mit dem Namen ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="fd586-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="fd586-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fd586-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="fd586-115">Dieser Befehl ruft Informationen über den Datenfluss mit dem Namen ContosoDataFlow im Arbeitsbereich mit dem Namen ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="fd586-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="fd586-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd586-116">PARAMETERS</span></span>

### <span data-ttu-id="fd586-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd586-117">-DefaultProfile</span></span>
<span data-ttu-id="fd586-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fd586-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd586-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fd586-119">-Name</span></span>
<span data-ttu-id="fd586-120">Der Name des Datenflusses.</span><span class="sxs-lookup"><span data-stu-id="fd586-120">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd586-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fd586-121">-WorkspaceName</span></span>
<span data-ttu-id="fd586-122">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="fd586-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fd586-123">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="fd586-123">-WorkspaceObject</span></span>
<span data-ttu-id="fd586-124">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="fd586-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fd586-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd586-125">CommonParameters</span></span>
<span data-ttu-id="fd586-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd586-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd586-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd586-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd586-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd586-128">INPUTS</span></span>

### <span data-ttu-id="fd586-129">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fd586-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="fd586-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd586-130">OUTPUTS</span></span>

### <span data-ttu-id="fd586-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="fd586-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="fd586-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd586-132">NOTES</span></span>

## <span data-ttu-id="fd586-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd586-133">RELATED LINKS</span></span>
