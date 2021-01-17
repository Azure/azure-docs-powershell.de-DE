---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 592c35a3407bd42846e8c24786716a73d5729c9a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359385"
---
# <span data-ttu-id="6a08e-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="6a08e-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="6a08e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a08e-102">SYNOPSIS</span></span>
<span data-ttu-id="6a08e-103">Ruft die Überwachungseinstellungen eines Azure Synapse Analytics SQL ab.</span><span class="sxs-lookup"><span data-stu-id="6a08e-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6a08e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a08e-104">SYNTAX</span></span>

### <span data-ttu-id="6a08e-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6a08e-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a08e-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a08e-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a08e-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a08e-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a08e-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a08e-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a08e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a08e-109">DESCRIPTION</span></span>
<span data-ttu-id="6a08e-110">Das **Cmdlet "Get-AzSynapseSqlPoolAuditSetting"** ruft die Überwachungseinstellungen eines Azure Synapse Analytics SQL ab.</span><span class="sxs-lookup"><span data-stu-id="6a08e-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6a08e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6a08e-111">EXAMPLES</span></span>

### <span data-ttu-id="6a08e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6a08e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="6a08e-113">Dieser Befehl ruft die Überwachungseinstellungen eines SQL "ContosoSqlPool" im Arbeitsbereich "ContosoWorkspace" ab.</span><span class="sxs-lookup"><span data-stu-id="6a08e-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="6a08e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6a08e-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="6a08e-115">Dieser Befehl ruft die Überwachungseinstellungen eines SQL "ContosoSqlPool" im Arbeitsbereich "ContosoWorkspace" über die Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="6a08e-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="6a08e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a08e-116">PARAMETERS</span></span>

### <span data-ttu-id="6a08e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a08e-117">-DefaultProfile</span></span>
<span data-ttu-id="6a08e-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a08e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a08e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a08e-119">-InputObject</span></span>
<span data-ttu-id="6a08e-120">SQL pool-Eingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6a08e-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6a08e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6a08e-121">-Name</span></span>
<span data-ttu-id="6a08e-122">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="6a08e-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="6a08e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a08e-123">-ResourceGroupName</span></span>
<span data-ttu-id="6a08e-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="6a08e-124">Resource group name.</span></span>

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

### <span data-ttu-id="6a08e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a08e-125">-ResourceId</span></span>
<span data-ttu-id="6a08e-126">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="6a08e-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="6a08e-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6a08e-127">-WorkspaceName</span></span>
<span data-ttu-id="6a08e-128">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="6a08e-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6a08e-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6a08e-129">-WorkspaceObject</span></span>
<span data-ttu-id="6a08e-130">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6a08e-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6a08e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a08e-131">CommonParameters</span></span>
<span data-ttu-id="6a08e-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a08e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a08e-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a08e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a08e-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6a08e-134">INPUTS</span></span>

### <span data-ttu-id="6a08e-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6a08e-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6a08e-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6a08e-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="6a08e-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6a08e-137">OUTPUTS</span></span>

### <span data-ttu-id="6a08e-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="6a08e-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="6a08e-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6a08e-139">NOTES</span></span>

## <span data-ttu-id="6a08e-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6a08e-140">RELATED LINKS</span></span>
