---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
ms.openlocfilehash: 22a7bb4c135a4424aa27a76f9e13ba14f21ca572
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007688"
---
# <span data-ttu-id="4d492-101">Get-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4d492-101">Get-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="4d492-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d492-102">SYNOPSIS</span></span>
<span data-ttu-id="4d492-103">Ruft eine Synapse Analytics-Firewall-Regel ab.</span><span class="sxs-lookup"><span data-stu-id="4d492-103">Gets a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="4d492-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d492-104">SYNTAX</span></span>

### <span data-ttu-id="4d492-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4d492-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d492-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d492-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseFirewallRule -WorkSpaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d492-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d492-107">DESCRIPTION</span></span>
<span data-ttu-id="4d492-108">Das Cmdlet " **Get-AzSynapseFirewallRule** " Ruft eine Azure Synapse Analytics-Firewallregel ab.</span><span class="sxs-lookup"><span data-stu-id="4d492-108">The **Get-AzSynapseFirewallRule** cmdlet gets a Azure Synapse Analytics Firewall Rule.</span></span>
<span data-ttu-id="4d492-109">Wenn Sie keinen Regelnamen angeben, ruft dieses Cmdlet alle Regeln ab.</span><span class="sxs-lookup"><span data-stu-id="4d492-109">If you do not specify a rule name, this cmdlet gets all rules.</span></span>

## <span data-ttu-id="4d492-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d492-110">EXAMPLES</span></span>

### <span data-ttu-id="4d492-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4d492-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="4d492-112">Dieser Befehl ruft alle Firewallregeln unter einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="4d492-112">This command gets all firewall rules under a workspace.</span></span>

### <span data-ttu-id="4d492-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4d492-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="4d492-114">Dieser Befehl ruft die Firewallregel unter Workspace ContosoWorkspace mit dem Namen ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="4d492-114">This command gets the firewall rule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="4d492-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4d492-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseFirewallRule
```

<span data-ttu-id="4d492-116">Dieser Befehl ruft alle Firewallregeln unter einem Arbeitsbereich durch Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="4d492-116">This command gets all firewall rules under a workspace through pipeline.</span></span>

## <span data-ttu-id="4d492-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d492-117">PARAMETERS</span></span>

### <span data-ttu-id="4d492-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d492-118">-DefaultProfile</span></span>
<span data-ttu-id="4d492-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4d492-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d492-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4d492-120">-Name</span></span>
<span data-ttu-id="4d492-121">Der Name der firerwall-Regel für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="4d492-121">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="4d492-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d492-122">-ResourceGroupName</span></span>
<span data-ttu-id="4d492-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4d492-123">Resource group name.</span></span>

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

### <span data-ttu-id="4d492-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4d492-124">-WorkspaceName</span></span>
<span data-ttu-id="4d492-125">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="4d492-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4d492-126">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="4d492-126">-WorkSpaceObject</span></span>
<span data-ttu-id="4d492-127">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="4d492-127">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4d492-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d492-128">CommonParameters</span></span>
<span data-ttu-id="4d492-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d492-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d492-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d492-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d492-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d492-131">INPUTS</span></span>

### <span data-ttu-id="4d492-132">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4d492-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4d492-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d492-133">OUTPUTS</span></span>

### <span data-ttu-id="4d492-134">Microsoft. Azure. Commands. Synapse. Models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4d492-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="4d492-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d492-135">NOTES</span></span>

## <span data-ttu-id="4d492-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d492-136">RELATED LINKS</span></span>
