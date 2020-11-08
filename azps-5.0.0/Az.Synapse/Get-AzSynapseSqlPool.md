---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: d37012ee5188b6dea15968aee8659387e06a87f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176816"
---
# <span data-ttu-id="3a92c-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="3a92c-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="3a92c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a92c-102">SYNOPSIS</span></span>
<span data-ttu-id="3a92c-103">Ruft einen Synapse Analytics SQL-Pool ab.</span><span class="sxs-lookup"><span data-stu-id="3a92c-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="3a92c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a92c-104">SYNTAX</span></span>

### <span data-ttu-id="3a92c-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3a92c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a92c-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a92c-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a92c-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a92c-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a92c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a92c-108">DESCRIPTION</span></span>
<span data-ttu-id="3a92c-109">Das Cmdlet " **Get-AzSynapseSqlPool** " Ruft Informationen zu einem Azure Synapse Analytics SQL-Pool ab.</span><span class="sxs-lookup"><span data-stu-id="3a92c-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="3a92c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a92c-110">EXAMPLES</span></span>

### <span data-ttu-id="3a92c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3a92c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="3a92c-112">Dieser Befehl ruft alle SQL-Pools unter einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="3a92c-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="3a92c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3a92c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="3a92c-114">Dieser Befehl ruft den SQL-Pool unter Workspace ContosoWorkspace mit dem Namen ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="3a92c-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="3a92c-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3a92c-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="3a92c-116">Dieser Befehl ruft alle SQL-Pools unter einem Arbeitsbereich durch Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="3a92c-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="3a92c-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="3a92c-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="3a92c-118">Mit diesem Befehl wird der SQL-Pool mit der angegebenen Ressourcen-ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3a92c-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="3a92c-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a92c-119">PARAMETERS</span></span>

### <span data-ttu-id="3a92c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a92c-120">-DefaultProfile</span></span>
<span data-ttu-id="3a92c-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3a92c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a92c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3a92c-122">-Name</span></span>
<span data-ttu-id="3a92c-123">Name des Synapsen-SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="3a92c-123">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a92c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a92c-124">-ResourceGroupName</span></span>
<span data-ttu-id="3a92c-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3a92c-125">Resource group name.</span></span>

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

### <span data-ttu-id="3a92c-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3a92c-126">-ResourceId</span></span>
<span data-ttu-id="3a92c-127">Ressourcen-ID des Synapse-SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="3a92c-127">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="3a92c-128">-Version</span><span class="sxs-lookup"><span data-stu-id="3a92c-128">-Version</span></span>
<span data-ttu-id="3a92c-129">[Diese Funktion befindet sich in einer limitierten Vorschau, die anfänglich nur für bestimmte Abonnements zugänglich ist.] Version des Synapse SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="3a92c-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="3a92c-130">Beispiel: 2 oder 3.</span><span class="sxs-lookup"><span data-stu-id="3a92c-130">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="3a92c-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3a92c-131">-WorkspaceName</span></span>
<span data-ttu-id="3a92c-132">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="3a92c-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3a92c-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="3a92c-133">-WorkspaceObject</span></span>
<span data-ttu-id="3a92c-134">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="3a92c-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3a92c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a92c-135">CommonParameters</span></span>
<span data-ttu-id="3a92c-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a92c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a92c-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a92c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a92c-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a92c-138">INPUTS</span></span>

### <span data-ttu-id="3a92c-139">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3a92c-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3a92c-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a92c-140">OUTPUTS</span></span>

### <span data-ttu-id="3a92c-141">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="3a92c-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="3a92c-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a92c-142">NOTES</span></span>

## <span data-ttu-id="3a92c-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a92c-143">RELATED LINKS</span></span>
