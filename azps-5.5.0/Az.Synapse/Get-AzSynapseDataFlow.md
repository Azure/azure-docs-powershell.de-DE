---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 87627738967a5c3174020932e5c9e7b996980ee9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165633"
---
# <span data-ttu-id="a82cf-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="a82cf-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="a82cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a82cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a82cf-103">Ruft Informationen zu Datenflüssen im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="a82cf-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="a82cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a82cf-104">SYNTAX</span></span>

### <span data-ttu-id="a82cf-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a82cf-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a82cf-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="a82cf-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a82cf-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a82cf-107">DESCRIPTION</span></span>
<span data-ttu-id="a82cf-108">Das **Cmdlet "Get-AzSynapseDataFlow"** ruft Informationen zu Datenflüssen im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="a82cf-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="a82cf-109">Wenn Sie den Namen eines Datenflusses angeben, ruft dieses Cmdlet Informationen zu diesem Datenfluss ab.</span><span class="sxs-lookup"><span data-stu-id="a82cf-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="a82cf-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datenflüssen im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="a82cf-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="a82cf-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a82cf-111">EXAMPLES</span></span>

### <span data-ttu-id="a82cf-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a82cf-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a82cf-113">Dieser Befehl ruft Informationen zu allen Datenflüssen im Arbeitsbereich namens "ContosoWorkspace" ab.</span><span class="sxs-lookup"><span data-stu-id="a82cf-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a82cf-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a82cf-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="a82cf-115">Dieser Befehl ruft Informationen über den Datenfluss namens "ContosoDataFlow" im Arbeitsbereich "ContosoWorkspace" ab.</span><span class="sxs-lookup"><span data-stu-id="a82cf-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a82cf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a82cf-116">PARAMETERS</span></span>

### <span data-ttu-id="a82cf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a82cf-117">-DefaultProfile</span></span>
<span data-ttu-id="a82cf-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a82cf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a82cf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a82cf-119">-Name</span></span>
<span data-ttu-id="a82cf-120">Der Datenflussname.</span><span class="sxs-lookup"><span data-stu-id="a82cf-120">The data flow name.</span></span>

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

### <span data-ttu-id="a82cf-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a82cf-121">-WorkspaceName</span></span>
<span data-ttu-id="a82cf-122">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a82cf-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a82cf-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a82cf-123">-WorkspaceObject</span></span>
<span data-ttu-id="a82cf-124">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a82cf-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a82cf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a82cf-125">CommonParameters</span></span>
<span data-ttu-id="a82cf-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a82cf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a82cf-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a82cf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a82cf-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a82cf-128">INPUTS</span></span>

### <span data-ttu-id="a82cf-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a82cf-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a82cf-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a82cf-130">OUTPUTS</span></span>

### <span data-ttu-id="a82cf-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="a82cf-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="a82cf-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a82cf-132">NOTES</span></span>

## <span data-ttu-id="a82cf-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a82cf-133">RELATED LINKS</span></span>
