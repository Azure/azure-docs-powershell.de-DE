---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqladvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 47800968fec9a12255bae01499618f9928416648
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950472"
---
# <span data-ttu-id="579d8-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="579d8-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="579d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="579d8-102">SYNOPSIS</span></span>
<span data-ttu-id="579d8-103">Ruft die Advanced Data Security-Richtlinie eines Arbeitsbereichs ab.</span><span class="sxs-lookup"><span data-stu-id="579d8-103">Gets Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="579d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="579d8-104">SYNTAX</span></span>

### <span data-ttu-id="579d8-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="579d8-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="579d8-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="579d8-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="579d8-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="579d8-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="579d8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="579d8-108">DESCRIPTION</span></span>
<span data-ttu-id="579d8-109">Das **Cmdlet Get-AzSynapseSqlAdvancedDataSecurityPolicy** ruft die Advanced Data Security-Richtlinie eines Arbeitsbereichs ab.</span><span class="sxs-lookup"><span data-stu-id="579d8-109">The **Get-AzSynapseSqlAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="579d8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="579d8-110">EXAMPLES</span></span>

### <span data-ttu-id="579d8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="579d8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedDataSecurityPolicy -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="579d8-112">Dieser Befehl ruft Advanced Data Security für den Arbeitsbereich namens ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="579d8-112">This command gets Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="579d8-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="579d8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAdvancedDataSecurityPolicy
```

<span data-ttu-id="579d8-114">Dieser Befehl ruft Advanced Data Security für den Arbeitsbereich namens ContosoWorkspace über die Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="579d8-114">This command gets Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="579d8-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="579d8-115">PARAMETERS</span></span>

### <span data-ttu-id="579d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="579d8-116">-DefaultProfile</span></span>
<span data-ttu-id="579d8-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="579d8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="579d8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="579d8-118">-InputObject</span></span>
<span data-ttu-id="579d8-119">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="579d8-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="579d8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="579d8-120">-ResourceGroupName</span></span>
<span data-ttu-id="579d8-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="579d8-121">Resource group name.</span></span>

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

### <span data-ttu-id="579d8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="579d8-122">-ResourceId</span></span>
<span data-ttu-id="579d8-123">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="579d8-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="579d8-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="579d8-124">-WorkspaceName</span></span>
<span data-ttu-id="579d8-125">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="579d8-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="579d8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="579d8-126">CommonParameters</span></span>
<span data-ttu-id="579d8-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="579d8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="579d8-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="579d8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="579d8-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="579d8-129">INPUTS</span></span>

### <span data-ttu-id="579d8-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="579d8-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="579d8-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="579d8-131">OUTPUTS</span></span>

### <span data-ttu-id="579d8-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="579d8-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="579d8-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="579d8-133">NOTES</span></span>

## <span data-ttu-id="579d8-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="579d8-134">RELATED LINKS</span></span>
