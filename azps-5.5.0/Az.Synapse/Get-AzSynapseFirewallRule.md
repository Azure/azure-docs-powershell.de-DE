---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
ms.openlocfilehash: 22a7bb4c135a4424aa27a76f9e13ba14f21ca572
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174988"
---
# <span data-ttu-id="b984e-101">Get-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b984e-101">Get-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="b984e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b984e-102">SYNOPSIS</span></span>
<span data-ttu-id="b984e-103">Ruft eine Synapse Analytics-Firewallregel ab.</span><span class="sxs-lookup"><span data-stu-id="b984e-103">Gets a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="b984e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b984e-104">SYNTAX</span></span>

### <span data-ttu-id="b984e-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b984e-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b984e-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b984e-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseFirewallRule -WorkSpaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b984e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b984e-107">DESCRIPTION</span></span>
<span data-ttu-id="b984e-108">Das **Cmdlet "Get-AzSynapseFirewallRule"** ruft eine Azure Synapse Analytics-Firewallregel ab.</span><span class="sxs-lookup"><span data-stu-id="b984e-108">The **Get-AzSynapseFirewallRule** cmdlet gets a Azure Synapse Analytics Firewall Rule.</span></span>
<span data-ttu-id="b984e-109">Wenn Sie keinen Regelnamen angeben, ruft dieses Cmdlet alle Regeln ab.</span><span class="sxs-lookup"><span data-stu-id="b984e-109">If you do not specify a rule name, this cmdlet gets all rules.</span></span>

## <span data-ttu-id="b984e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b984e-110">EXAMPLES</span></span>

### <span data-ttu-id="b984e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b984e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="b984e-112">Dieser Befehl ruft alle Firewallregeln unter einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="b984e-112">This command gets all firewall rules under a workspace.</span></span>

### <span data-ttu-id="b984e-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b984e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="b984e-114">Dieser Befehl ruft die Firewallregel im Arbeitsbereich ContosoWorkspace mit dem Namen "ContosoFirewallRule" ab.</span><span class="sxs-lookup"><span data-stu-id="b984e-114">This command gets the firewall rule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="b984e-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b984e-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseFirewallRule
```

<span data-ttu-id="b984e-116">Dieser Befehl ruft alle Firewallregeln in einem Arbeitsbereich über die Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="b984e-116">This command gets all firewall rules under a workspace through pipeline.</span></span>

## <span data-ttu-id="b984e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b984e-117">PARAMETERS</span></span>

### <span data-ttu-id="b984e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b984e-118">-DefaultProfile</span></span>
<span data-ttu-id="b984e-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b984e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b984e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b984e-120">-Name</span></span>
<span data-ttu-id="b984e-121">Der Name der Firewallregel für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="b984e-121">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b984e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b984e-122">-ResourceGroupName</span></span>
<span data-ttu-id="b984e-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="b984e-123">Resource group name.</span></span>

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

### <span data-ttu-id="b984e-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b984e-124">-WorkspaceName</span></span>
<span data-ttu-id="b984e-125">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="b984e-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b984e-126">-WorkSpaceObject</span><span class="sxs-lookup"><span data-stu-id="b984e-126">-WorkSpaceObject</span></span>
<span data-ttu-id="b984e-127">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b984e-127">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b984e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b984e-128">CommonParameters</span></span>
<span data-ttu-id="b984e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b984e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b984e-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b984e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b984e-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b984e-131">INPUTS</span></span>

### <span data-ttu-id="b984e-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b984e-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b984e-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b984e-133">OUTPUTS</span></span>

### <span data-ttu-id="b984e-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b984e-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="b984e-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b984e-135">NOTES</span></span>

## <span data-ttu-id="b984e-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b984e-136">RELATED LINKS</span></span>
