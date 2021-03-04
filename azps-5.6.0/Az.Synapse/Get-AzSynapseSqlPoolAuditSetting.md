---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: dea94d89bfd5384d8ec614259a5bb342cd9d186b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950440"
---
# <span data-ttu-id="df429-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="df429-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="df429-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df429-102">SYNOPSIS</span></span>
<span data-ttu-id="df429-103">Ruft die Überwachungseinstellungen eines Azure Synapse Analytics-SQL ab.</span><span class="sxs-lookup"><span data-stu-id="df429-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="df429-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df429-104">SYNTAX</span></span>

### <span data-ttu-id="df429-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="df429-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df429-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df429-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df429-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df429-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df429-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df429-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df429-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df429-109">DESCRIPTION</span></span>
<span data-ttu-id="df429-110">Das **Get-AzSynapseSqlPoolAuditSetting-Cmdlet** ruft die Überwachungseinstellungen eines Azure Synapse Analytics-SQL ab.</span><span class="sxs-lookup"><span data-stu-id="df429-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="df429-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="df429-111">EXAMPLES</span></span>

### <span data-ttu-id="df429-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="df429-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="df429-113">Mit diesem Befehl werden die Überwachungseinstellungen eines SQL ContosoSqlPool im Arbeitsbereich ContosoWorkspace aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="df429-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="df429-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="df429-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="df429-115">Mit diesem Befehl werden die Überwachungseinstellungen eines SQL ContosoSqlPool im Arbeitsbereich ContosoWorkspace über die Pipeline aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="df429-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="df429-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="df429-116">PARAMETERS</span></span>

### <span data-ttu-id="df429-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df429-117">-DefaultProfile</span></span>
<span data-ttu-id="df429-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df429-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df429-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df429-119">-InputObject</span></span>
<span data-ttu-id="df429-120">SQL -Pooleingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="df429-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="df429-121">-Name</span><span class="sxs-lookup"><span data-stu-id="df429-121">-Name</span></span>
<span data-ttu-id="df429-122">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="df429-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="df429-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df429-123">-ResourceGroupName</span></span>
<span data-ttu-id="df429-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="df429-124">Resource group name.</span></span>

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

### <span data-ttu-id="df429-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df429-125">-ResourceId</span></span>
<span data-ttu-id="df429-126">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="df429-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="df429-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="df429-127">-WorkspaceName</span></span>
<span data-ttu-id="df429-128">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="df429-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="df429-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="df429-129">-WorkspaceObject</span></span>
<span data-ttu-id="df429-130">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="df429-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="df429-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df429-131">CommonParameters</span></span>
<span data-ttu-id="df429-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df429-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df429-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df429-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df429-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="df429-134">INPUTS</span></span>

### <span data-ttu-id="df429-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="df429-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="df429-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="df429-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="df429-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="df429-137">OUTPUTS</span></span>

### <span data-ttu-id="df429-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="df429-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="df429-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="df429-139">NOTES</span></span>

## <span data-ttu-id="df429-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="df429-140">RELATED LINKS</span></span>
