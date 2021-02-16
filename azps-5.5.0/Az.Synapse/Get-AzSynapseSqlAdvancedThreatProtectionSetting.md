---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8c17825dca186f4edf856a2de2ef76082253c39e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173596"
---
# <span data-ttu-id="69038-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="69038-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="69038-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69038-102">SYNOPSIS</span></span>
<span data-ttu-id="69038-103">Ruft die erweiterten Threat Protection-Einstellungen für einen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="69038-103">Gets the advanced threat protection settings for a workspace.</span></span>

## <span data-ttu-id="69038-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69038-104">SYNTAX</span></span>

### <span data-ttu-id="69038-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="69038-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69038-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69038-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69038-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69038-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69038-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69038-108">DESCRIPTION</span></span>
<span data-ttu-id="69038-109">Das **Cmdlet "Get-AzSynapseSqlAdvancedThreatProtectionSetting"** ruft die erweiterten Threat Protection-Einstellungen eines Azure Synapse Analytics Workspace ab.</span><span class="sxs-lookup"><span data-stu-id="69038-109">The **Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="69038-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="69038-110">EXAMPLES</span></span>

### <span data-ttu-id="69038-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="69038-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="69038-112">Dieser Befehl ruft die erweiterten Threat Protection-Einstellungen für einen Arbeitsbereich namens ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="69038-112">This command gets the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="69038-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69038-113">PARAMETERS</span></span>

### <span data-ttu-id="69038-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69038-114">-DefaultProfile</span></span>
<span data-ttu-id="69038-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="69038-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69038-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69038-116">-InputObject</span></span>
<span data-ttu-id="69038-117">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="69038-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="69038-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69038-118">-ResourceGroupName</span></span>
<span data-ttu-id="69038-119">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="69038-119">Resource group name.</span></span>

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

### <span data-ttu-id="69038-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69038-120">-ResourceId</span></span>
<span data-ttu-id="69038-121">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="69038-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="69038-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="69038-122">-WorkspaceName</span></span>
<span data-ttu-id="69038-123">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="69038-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="69038-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69038-124">CommonParameters</span></span>
<span data-ttu-id="69038-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69038-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69038-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69038-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69038-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="69038-127">INPUTS</span></span>

### <span data-ttu-id="69038-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="69038-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="69038-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="69038-129">OUTPUTS</span></span>

### <span data-ttu-id="69038-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="69038-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="69038-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="69038-131">NOTES</span></span>

## <span data-ttu-id="69038-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="69038-132">RELATED LINKS</span></span>
