---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: f35e4787779c49b399659f5e01ed8002df2e19ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950467"
---
# <span data-ttu-id="03a98-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="03a98-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="03a98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03a98-102">SYNOPSIS</span></span>
<span data-ttu-id="03a98-103">Ruft die erweiterten Einstellungen für den Bedrohungsschutz für einen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="03a98-103">Gets the advanced threat protection settings for a workspace.</span></span>

## <span data-ttu-id="03a98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03a98-104">SYNTAX</span></span>

### <span data-ttu-id="03a98-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="03a98-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03a98-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03a98-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03a98-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03a98-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03a98-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03a98-108">DESCRIPTION</span></span>
<span data-ttu-id="03a98-109">Das **Get-AzSynapseSqlAdvancedThreatProtectionSetting-Cmdlet** ruft die erweiterten Bedrohungsschutzeinstellungen eines Azure Synapse Analytics Workspace ab.</span><span class="sxs-lookup"><span data-stu-id="03a98-109">The **Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="03a98-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="03a98-110">EXAMPLES</span></span>

### <span data-ttu-id="03a98-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="03a98-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="03a98-112">Dieser Befehl ruft die erweiterten Bedrohungsschutzeinstellungen für einen Arbeitsbereich namens ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="03a98-112">This command gets the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="03a98-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="03a98-113">PARAMETERS</span></span>

### <span data-ttu-id="03a98-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03a98-114">-DefaultProfile</span></span>
<span data-ttu-id="03a98-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="03a98-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03a98-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03a98-116">-InputObject</span></span>
<span data-ttu-id="03a98-117">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="03a98-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="03a98-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03a98-118">-ResourceGroupName</span></span>
<span data-ttu-id="03a98-119">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="03a98-119">Resource group name.</span></span>

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

### <span data-ttu-id="03a98-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03a98-120">-ResourceId</span></span>
<span data-ttu-id="03a98-121">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="03a98-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="03a98-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="03a98-122">-WorkspaceName</span></span>
<span data-ttu-id="03a98-123">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="03a98-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="03a98-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a98-124">CommonParameters</span></span>
<span data-ttu-id="03a98-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03a98-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a98-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03a98-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a98-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="03a98-127">INPUTS</span></span>

### <span data-ttu-id="03a98-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="03a98-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="03a98-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="03a98-129">OUTPUTS</span></span>

### <span data-ttu-id="03a98-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="03a98-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="03a98-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="03a98-131">NOTES</span></span>

## <span data-ttu-id="03a98-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="03a98-132">RELATED LINKS</span></span>
