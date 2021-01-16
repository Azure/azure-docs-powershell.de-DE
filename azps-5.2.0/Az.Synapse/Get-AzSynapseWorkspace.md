---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: d95892068b92745fa09419d83d3bdb001f0bdead
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294766"
---
# <span data-ttu-id="2493f-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2493f-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="2493f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2493f-102">SYNOPSIS</span></span>
<span data-ttu-id="2493f-103">Ruft einen Synapse Analytics-Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="2493f-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="2493f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2493f-104">SYNTAX</span></span>

### <span data-ttu-id="2493f-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2493f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2493f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2493f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2493f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2493f-107">DESCRIPTION</span></span>
<span data-ttu-id="2493f-108">Das **Cmdlet "Get-AzSynapseWorkspace"** ruft Informationen zu einem Azure Synapse Analytics-Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="2493f-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="2493f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2493f-109">EXAMPLES</span></span>

### <span data-ttu-id="2493f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2493f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="2493f-111">Dieser Befehl ruft alle Azure Synapse Analytics-Arbeitsbereiche unter dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="2493f-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="2493f-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2493f-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="2493f-113">Dieser Befehl ruft alle Azure Synapse Analytics-Arbeitsbereiche unter dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="2493f-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="2493f-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2493f-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="2493f-115">Dieser Befehl ruft den Azure Synapse Analytics-Arbeitsbereich mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="2493f-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="2493f-116">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="2493f-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="2493f-117">Dieser Befehl ruft den Azure Synapse Analytics-Arbeitsbereich mit der angegebenen Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="2493f-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="2493f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2493f-118">PARAMETERS</span></span>

### <span data-ttu-id="2493f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2493f-119">-DefaultProfile</span></span>
<span data-ttu-id="2493f-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2493f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2493f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2493f-121">-Name</span></span>
<span data-ttu-id="2493f-122">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="2493f-122">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2493f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2493f-123">-ResourceGroupName</span></span>
<span data-ttu-id="2493f-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="2493f-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2493f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2493f-125">-ResourceId</span></span>
<span data-ttu-id="2493f-126">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="2493f-126">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2493f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2493f-127">CommonParameters</span></span>
<span data-ttu-id="2493f-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2493f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2493f-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2493f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2493f-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2493f-130">INPUTS</span></span>

### <span data-ttu-id="2493f-131">Keine</span><span class="sxs-lookup"><span data-stu-id="2493f-131">None</span></span>

## <span data-ttu-id="2493f-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2493f-132">OUTPUTS</span></span>

### <span data-ttu-id="2493f-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2493f-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2493f-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2493f-134">NOTES</span></span>

## <span data-ttu-id="2493f-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2493f-135">RELATED LINKS</span></span>
