---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: 8199b14cf7b41eb99bb17f1692e762a07e127f26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173577"
---
# <span data-ttu-id="52429-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="52429-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="52429-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52429-102">SYNOPSIS</span></span>
<span data-ttu-id="52429-103">Ruft einen Synapse Analytics SQL ab.</span><span class="sxs-lookup"><span data-stu-id="52429-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="52429-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52429-104">SYNTAX</span></span>

### <span data-ttu-id="52429-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="52429-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52429-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52429-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52429-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52429-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52429-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52429-108">DESCRIPTION</span></span>
<span data-ttu-id="52429-109">Das **Cmdlet "Get-AzSynapseSqlPool"** ruft Informationen zu einem Azure Synapse Analytics SQL ab.</span><span class="sxs-lookup"><span data-stu-id="52429-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="52429-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="52429-110">EXAMPLES</span></span>

### <span data-ttu-id="52429-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="52429-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="52429-112">Dieser Befehl ruft alle SQL unter einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="52429-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="52429-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="52429-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="52429-114">Dieser Befehl ruft den SQL unter dem Arbeitsbereich "ContosoWorkspace" mit dem Namen "ContosoSqlPool" ab.</span><span class="sxs-lookup"><span data-stu-id="52429-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="52429-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="52429-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="52429-116">Mit diesem Befehl werden alle SQL über die Pipeline unter einem Arbeitsbereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="52429-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="52429-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="52429-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="52429-118">Dieser Befehl ruft den SQL mit der angegebenen Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="52429-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="52429-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52429-119">PARAMETERS</span></span>

### <span data-ttu-id="52429-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52429-120">-DefaultProfile</span></span>
<span data-ttu-id="52429-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52429-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52429-122">-Name</span><span class="sxs-lookup"><span data-stu-id="52429-122">-Name</span></span>
<span data-ttu-id="52429-123">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="52429-123">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SqlPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52429-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52429-124">-ResourceGroupName</span></span>
<span data-ttu-id="52429-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="52429-125">Resource group name.</span></span>

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

### <span data-ttu-id="52429-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52429-126">-ResourceId</span></span>
<span data-ttu-id="52429-127">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="52429-127">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="52429-128">-Version</span><span class="sxs-lookup"><span data-stu-id="52429-128">-Version</span></span>
<span data-ttu-id="52429-129">[Dieses Feature ist in einer eingeschränkten Vorschau verfügbar und kann anfänglich nur für bestimmte Abonnements verwendet werden.] Version des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="52429-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="52429-130">Beispiel: 2 oder 3.</span><span class="sxs-lookup"><span data-stu-id="52429-130">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52429-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="52429-131">-WorkspaceName</span></span>
<span data-ttu-id="52429-132">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="52429-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52429-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="52429-133">-WorkspaceObject</span></span>
<span data-ttu-id="52429-134">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="52429-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52429-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52429-135">CommonParameters</span></span>
<span data-ttu-id="52429-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52429-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52429-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52429-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52429-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="52429-138">INPUTS</span></span>

### <span data-ttu-id="52429-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="52429-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="52429-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="52429-140">OUTPUTS</span></span>

### <span data-ttu-id="52429-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="52429-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="52429-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="52429-142">NOTES</span></span>

## <span data-ttu-id="52429-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="52429-143">RELATED LINKS</span></span>
