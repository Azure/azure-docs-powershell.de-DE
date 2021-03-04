---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: cf32bea3942c89b408592778657e5ecffae2acd8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950464"
---
# <span data-ttu-id="587e7-101">Get-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="587e7-101">Get-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="587e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="587e7-102">SYNOPSIS</span></span>
<span data-ttu-id="587e7-103">Ruft die Überwachungseinstellungen eines Azure Synapse Analytics-Arbeitsbereichs ab.</span><span class="sxs-lookup"><span data-stu-id="587e7-103">Gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="587e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="587e7-104">SYNTAX</span></span>

### <span data-ttu-id="587e7-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="587e7-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="587e7-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="587e7-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="587e7-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="587e7-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="587e7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="587e7-108">DESCRIPTION</span></span>
<span data-ttu-id="587e7-109">Das **Get-AzSynapseSqlAuditSetting-Cmdlet** ruft die Überwachungseinstellungen eines Azure Synapse Analytics-Arbeitsbereichs ab.</span><span class="sxs-lookup"><span data-stu-id="587e7-109">The **Get-AzSynapseSqlAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="587e7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="587e7-110">EXAMPLES</span></span>

### <span data-ttu-id="587e7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="587e7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="587e7-112">Ruft die Überwachungseinstellungen eines Arbeitsbereichs namens ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="587e7-112">Gets the auditing settings of a workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="587e7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="587e7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAuditSetting
```

<span data-ttu-id="587e7-114">Ruft die Überwachungseinstellungen eines Arbeitsbereichs namens ContosoWorkspace über die Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="587e7-114">Gets the auditing settings of a workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="587e7-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="587e7-115">PARAMETERS</span></span>

### <span data-ttu-id="587e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="587e7-116">-DefaultProfile</span></span>
<span data-ttu-id="587e7-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="587e7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="587e7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="587e7-118">-InputObject</span></span>
<span data-ttu-id="587e7-119">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="587e7-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="587e7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="587e7-120">-ResourceGroupName</span></span>
<span data-ttu-id="587e7-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="587e7-121">Resource group name.</span></span>

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

### <span data-ttu-id="587e7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="587e7-122">-ResourceId</span></span>
<span data-ttu-id="587e7-123">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="587e7-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="587e7-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="587e7-124">-WorkspaceName</span></span>
<span data-ttu-id="587e7-125">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="587e7-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="587e7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="587e7-126">CommonParameters</span></span>
<span data-ttu-id="587e7-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="587e7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="587e7-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="587e7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="587e7-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="587e7-129">INPUTS</span></span>

### <span data-ttu-id="587e7-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="587e7-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="587e7-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="587e7-131">OUTPUTS</span></span>

### <span data-ttu-id="587e7-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="587e7-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="587e7-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="587e7-133">NOTES</span></span>

## <span data-ttu-id="587e7-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="587e7-134">RELATED LINKS</span></span>
