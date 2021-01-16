---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8c17825dca186f4edf856a2de2ef76082253c39e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383913"
---
# <span data-ttu-id="e9b51-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="e9b51-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="e9b51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9b51-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b51-103">Ruft die erweiterten Threat Protection-Einstellungen für einen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="e9b51-103">Gets the advanced threat protection settings for a workspace.</span></span>

## <span data-ttu-id="e9b51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9b51-104">SYNTAX</span></span>

### <span data-ttu-id="e9b51-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9b51-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9b51-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9b51-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9b51-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9b51-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9b51-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9b51-108">DESCRIPTION</span></span>
<span data-ttu-id="e9b51-109">Das **Cmdlet "Get-AzSynapseSqlAdvancedThreatProtectionSetting"** ruft die erweiterten Threat Protection-Einstellungen eines Azure Synapse Analytics Workspace ab.</span><span class="sxs-lookup"><span data-stu-id="e9b51-109">The **Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="e9b51-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e9b51-110">EXAMPLES</span></span>

### <span data-ttu-id="e9b51-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e9b51-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="e9b51-112">Dieser Befehl ruft die erweiterten Threat Protection-Einstellungen für einen Arbeitsbereich namens ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="e9b51-112">This command gets the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="e9b51-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9b51-113">PARAMETERS</span></span>

### <span data-ttu-id="e9b51-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b51-114">-DefaultProfile</span></span>
<span data-ttu-id="e9b51-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9b51-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9b51-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9b51-116">-InputObject</span></span>
<span data-ttu-id="e9b51-117">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e9b51-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e9b51-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9b51-118">-ResourceGroupName</span></span>
<span data-ttu-id="e9b51-119">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="e9b51-119">Resource group name.</span></span>

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

### <span data-ttu-id="e9b51-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9b51-120">-ResourceId</span></span>
<span data-ttu-id="e9b51-121">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="e9b51-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="e9b51-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e9b51-122">-WorkspaceName</span></span>
<span data-ttu-id="e9b51-123">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="e9b51-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e9b51-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b51-124">CommonParameters</span></span>
<span data-ttu-id="e9b51-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9b51-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b51-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9b51-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b51-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e9b51-127">INPUTS</span></span>

### <span data-ttu-id="e9b51-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e9b51-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e9b51-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e9b51-129">OUTPUTS</span></span>

### <span data-ttu-id="e9b51-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="e9b51-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="e9b51-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e9b51-131">NOTES</span></span>

## <span data-ttu-id="e9b51-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e9b51-132">RELATED LINKS</span></span>
