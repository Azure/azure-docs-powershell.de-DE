---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: f9f921368f55b5901657ca4e366927a284302745
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359357"
---
# <span data-ttu-id="f4f0a-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="f4f0a-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="f4f0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f0a-103">Ruft die unterschiedlichen Wiederherstellungspunkte ab, aus denen ein Synapse Analytics SQL wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f4f0a-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="f4f0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4f0a-104">SYNTAX</span></span>

### <span data-ttu-id="f4f0a-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4f0a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4f0a-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4f0a-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4f0a-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4f0a-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4f0a-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4f0a-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4f0a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4f0a-109">DESCRIPTION</span></span>
<span data-ttu-id="f4f0a-110">Das **Cmdlet "Get-AzSynapseSqlPoolRestorePoint"** ruft die unterschiedlichen Wiederherstellungspunkte ab, aus der ein Azure Synapse Analytics SQL wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f4f0a-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="f4f0a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4f0a-111">EXAMPLES</span></span>

### <span data-ttu-id="f4f0a-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4f0a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="f4f0a-113">Dieser Befehl gibt alle verfügbaren Wiederherstellungspunkte für den Azure Synapse Analytics SQL "ContosoSqlPool" zurück.</span><span class="sxs-lookup"><span data-stu-id="f4f0a-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="f4f0a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4f0a-114">PARAMETERS</span></span>

### <span data-ttu-id="f4f0a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f0a-115">-DefaultProfile</span></span>
<span data-ttu-id="f4f0a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4f0a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4f0a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4f0a-117">-InputObject</span></span>
<span data-ttu-id="f4f0a-118">SQL pool-Eingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f4f0a-118">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4f0a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f4f0a-119">-Name</span></span>
<span data-ttu-id="f4f0a-120">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="f4f0a-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f0a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4f0a-121">-ResourceGroupName</span></span>
<span data-ttu-id="f4f0a-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="f4f0a-122">Resource group name.</span></span>

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

### <span data-ttu-id="f4f0a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4f0a-123">-ResourceId</span></span>
<span data-ttu-id="f4f0a-124">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="f4f0a-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="f4f0a-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f4f0a-125">-WorkspaceName</span></span>
<span data-ttu-id="f4f0a-126">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="f4f0a-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f4f0a-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f4f0a-127">-WorkspaceObject</span></span>
<span data-ttu-id="f4f0a-128">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f4f0a-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f4f0a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f0a-129">CommonParameters</span></span>
<span data-ttu-id="f4f0a-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4f0a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f0a-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4f0a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f0a-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4f0a-132">INPUTS</span></span>

### <span data-ttu-id="f4f0a-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f4f0a-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f4f0a-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f4f0a-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="f4f0a-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4f0a-135">OUTPUTS</span></span>

### <span data-ttu-id="f4f0a-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span><span class="sxs-lookup"><span data-stu-id="f4f0a-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="f4f0a-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f4f0a-137">NOTES</span></span>

## <span data-ttu-id="f4f0a-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f4f0a-138">RELATED LINKS</span></span>
