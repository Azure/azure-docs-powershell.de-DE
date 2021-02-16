---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 9188a1cc8dde39db4d755fb2059f3633fc85ead8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157801"
---
# <span data-ttu-id="3273a-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3273a-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="3273a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3273a-102">SYNOPSIS</span></span>
<span data-ttu-id="3273a-103">Aktualisiert eine Synapse Analytics-Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="3273a-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="3273a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3273a-104">SYNTAX</span></span>

### <span data-ttu-id="3273a-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3273a-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3273a-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3273a-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3273a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3273a-107">DESCRIPTION</span></span>
<span data-ttu-id="3273a-108">Das **Cmdlet "Update-AzSynapseFirewallRule"** geändert eine Azure Synapse Analytics-Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="3273a-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="3273a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3273a-109">EXAMPLES</span></span>

### <span data-ttu-id="3273a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3273a-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="3273a-111">Mit diesem Befehl wird die Firewallregel namens "ContosoFirewallRule" im Arbeitsbereich "ContosoWorkspace" mit dem Namen "ContosoFirewallRule" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3273a-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="3273a-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3273a-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="3273a-113">Mit diesem Befehl wird die Firewallregel namens "ContosoFirewallRule" in einem Arbeitsbereich über die Pipeline aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3273a-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="3273a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3273a-114">PARAMETERS</span></span>

### <span data-ttu-id="3273a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3273a-115">-AsJob</span></span>
<span data-ttu-id="3273a-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3273a-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3273a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3273a-117">-DefaultProfile</span></span>
<span data-ttu-id="3273a-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3273a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3273a-119">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="3273a-119">-EndIpAddress</span></span>
<span data-ttu-id="3273a-120">Die End-IP-Adresse der Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="3273a-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="3273a-121">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="3273a-121">Must be IPv4 format.</span></span>
<span data-ttu-id="3273a-122">Muss größer gleich "startIpAddress" sein.</span><span class="sxs-lookup"><span data-stu-id="3273a-122">Must be greater than or equal to startIpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3273a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3273a-123">-Name</span></span>
<span data-ttu-id="3273a-124">Der Name der Firewallregel für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="3273a-124">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3273a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3273a-125">-ResourceGroupName</span></span>
<span data-ttu-id="3273a-126">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="3273a-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3273a-127">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="3273a-127">-StartIpAddress</span></span>
<span data-ttu-id="3273a-128">Die Start-IP-Adresse der Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="3273a-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="3273a-129">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="3273a-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3273a-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3273a-130">-WorkspaceName</span></span>
<span data-ttu-id="3273a-131">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="3273a-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3273a-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3273a-132">-WorkspaceObject</span></span>
<span data-ttu-id="3273a-133">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3273a-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3273a-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3273a-134">-Confirm</span></span>
<span data-ttu-id="3273a-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3273a-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3273a-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3273a-136">-WhatIf</span></span>
<span data-ttu-id="3273a-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3273a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3273a-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3273a-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3273a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3273a-139">CommonParameters</span></span>
<span data-ttu-id="3273a-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3273a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3273a-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3273a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3273a-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3273a-142">INPUTS</span></span>

### <span data-ttu-id="3273a-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3273a-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3273a-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3273a-144">OUTPUTS</span></span>

### <span data-ttu-id="3273a-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3273a-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="3273a-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3273a-146">NOTES</span></span>

## <span data-ttu-id="3273a-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3273a-147">RELATED LINKS</span></span>
