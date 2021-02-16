---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 592c35a3407bd42846e8c24786716a73d5729c9a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162849"
---
# <span data-ttu-id="78fac-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="78fac-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="78fac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78fac-102">SYNOPSIS</span></span>
<span data-ttu-id="78fac-103">Ruft die Überwachungseinstellungen eines Azure Synapse Analytics SQL ab.</span><span class="sxs-lookup"><span data-stu-id="78fac-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="78fac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78fac-104">SYNTAX</span></span>

### <span data-ttu-id="78fac-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="78fac-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78fac-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78fac-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78fac-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78fac-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78fac-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78fac-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78fac-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78fac-109">DESCRIPTION</span></span>
<span data-ttu-id="78fac-110">Das **Cmdlet "Get-AzSynapseSqlPoolAuditSetting"** ruft die Überwachungseinstellungen eines Azure Synapse Analytics SQL ab.</span><span class="sxs-lookup"><span data-stu-id="78fac-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="78fac-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="78fac-111">EXAMPLES</span></span>

### <span data-ttu-id="78fac-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="78fac-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="78fac-113">Dieser Befehl ruft die Überwachungseinstellungen eines SQL "ContosoSqlPool" im Arbeitsbereich "ContosoWorkspace" ab.</span><span class="sxs-lookup"><span data-stu-id="78fac-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="78fac-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="78fac-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="78fac-115">Dieser Befehl ruft die Überwachungseinstellungen eines SQL "ContosoSqlPool" im Arbeitsbereich "ContosoWorkspace" über die Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="78fac-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="78fac-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78fac-116">PARAMETERS</span></span>

### <span data-ttu-id="78fac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78fac-117">-DefaultProfile</span></span>
<span data-ttu-id="78fac-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78fac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78fac-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78fac-119">-InputObject</span></span>
<span data-ttu-id="78fac-120">SQL pool-Eingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="78fac-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="78fac-121">-Name</span><span class="sxs-lookup"><span data-stu-id="78fac-121">-Name</span></span>
<span data-ttu-id="78fac-122">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="78fac-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="78fac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78fac-123">-ResourceGroupName</span></span>
<span data-ttu-id="78fac-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="78fac-124">Resource group name.</span></span>

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

### <span data-ttu-id="78fac-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78fac-125">-ResourceId</span></span>
<span data-ttu-id="78fac-126">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="78fac-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="78fac-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="78fac-127">-WorkspaceName</span></span>
<span data-ttu-id="78fac-128">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="78fac-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="78fac-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="78fac-129">-WorkspaceObject</span></span>
<span data-ttu-id="78fac-130">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="78fac-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="78fac-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78fac-131">CommonParameters</span></span>
<span data-ttu-id="78fac-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78fac-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78fac-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78fac-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78fac-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="78fac-134">INPUTS</span></span>

### <span data-ttu-id="78fac-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="78fac-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="78fac-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="78fac-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="78fac-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="78fac-137">OUTPUTS</span></span>

### <span data-ttu-id="78fac-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="78fac-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="78fac-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="78fac-139">NOTES</span></span>

## <span data-ttu-id="78fac-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="78fac-140">RELATED LINKS</span></span>
