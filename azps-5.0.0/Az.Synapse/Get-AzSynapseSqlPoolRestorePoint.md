---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: f9f921368f55b5901657ca4e366927a284302745
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175955"
---
# <span data-ttu-id="0f0d6-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="0f0d6-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="0f0d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f0d6-102">SYNOPSIS</span></span>
<span data-ttu-id="0f0d6-103">Ruft die eindeutigen Wiederherstellungspunkte ab, aus denen ein Synapse Analytics SQL-Pool wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0f0d6-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="0f0d6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f0d6-104">SYNTAX</span></span>

### <span data-ttu-id="0f0d6-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0f0d6-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f0d6-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f0d6-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f0d6-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f0d6-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f0d6-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f0d6-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f0d6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f0d6-109">DESCRIPTION</span></span>
<span data-ttu-id="0f0d6-110">Das Cmdlet " **Get-AzSynapseSqlPoolRestorePoint** " Ruft die eindeutigen Wiederherstellungspunkte ab, aus denen ein Azure Synapse Analytics SQL-Pool wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0f0d6-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="0f0d6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f0d6-111">EXAMPLES</span></span>

### <span data-ttu-id="0f0d6-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0f0d6-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="0f0d6-113">Dieser Befehl gibt alle verfügbaren Wiederherstellungspunkte für den Azure Synapse Analytics SQL-Pool mit dem Namen ContosoSqlPool zurück.</span><span class="sxs-lookup"><span data-stu-id="0f0d6-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="0f0d6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f0d6-114">PARAMETERS</span></span>

### <span data-ttu-id="0f0d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f0d6-115">-DefaultProfile</span></span>
<span data-ttu-id="0f0d6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0f0d6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f0d6-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0f0d6-117">-InputObject</span></span>
<span data-ttu-id="0f0d6-118">SQL-Pool Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="0f0d6-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0f0d6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0f0d6-119">-Name</span></span>
<span data-ttu-id="0f0d6-120">Name des Synapsen-SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="0f0d6-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="0f0d6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f0d6-121">-ResourceGroupName</span></span>
<span data-ttu-id="0f0d6-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0f0d6-122">Resource group name.</span></span>

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

### <span data-ttu-id="0f0d6-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0f0d6-123">-ResourceId</span></span>
<span data-ttu-id="0f0d6-124">Ressourcen-ID des Synapse-SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="0f0d6-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="0f0d6-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0f0d6-125">-WorkspaceName</span></span>
<span data-ttu-id="0f0d6-126">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="0f0d6-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0f0d6-127">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="0f0d6-127">-WorkspaceObject</span></span>
<span data-ttu-id="0f0d6-128">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="0f0d6-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0f0d6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f0d6-129">CommonParameters</span></span>
<span data-ttu-id="0f0d6-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f0d6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f0d6-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f0d6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f0d6-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f0d6-132">INPUTS</span></span>

### <span data-ttu-id="0f0d6-133">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0f0d6-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0f0d6-134">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0f0d6-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="0f0d6-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f0d6-135">OUTPUTS</span></span>

### <span data-ttu-id="0f0d6-136">Microsoft. Azure. Management. Synapse. Models. RestorePoint</span><span class="sxs-lookup"><span data-stu-id="0f0d6-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="0f0d6-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f0d6-137">NOTES</span></span>

## <span data-ttu-id="0f0d6-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f0d6-138">RELATED LINKS</span></span>
