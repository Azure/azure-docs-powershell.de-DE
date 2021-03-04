---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 48f2ea831470482a91e9ff78dc8b70472e2f556a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948195"
---
# <span data-ttu-id="6102e-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6102e-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="6102e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6102e-102">SYNOPSIS</span></span>
<span data-ttu-id="6102e-103">Aktualisiert eine Synapse Analytics-Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="6102e-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="6102e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6102e-104">SYNTAX</span></span>

### <span data-ttu-id="6102e-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6102e-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6102e-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6102e-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6102e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6102e-107">DESCRIPTION</span></span>
<span data-ttu-id="6102e-108">Das **Cmdlet Update-AzSynapseFirewallRule** geändert eine Azure Synapse Analytics-Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="6102e-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="6102e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6102e-109">EXAMPLES</span></span>

### <span data-ttu-id="6102e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6102e-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="6102e-111">Mit diesem Befehl wird die Firewallregel "ContosoFirewallRule" unter dem Arbeitsbereich ContosoWorkspace mit dem Namen ContosoFirewallRule aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6102e-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="6102e-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6102e-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="6102e-113">Mit diesem Befehl wird die Firewallregel "ContosoFirewallRule" unter einem Arbeitsbereich über die Pipeline aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6102e-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="6102e-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6102e-114">PARAMETERS</span></span>

### <span data-ttu-id="6102e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6102e-115">-AsJob</span></span>
<span data-ttu-id="6102e-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6102e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6102e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6102e-117">-DefaultProfile</span></span>
<span data-ttu-id="6102e-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6102e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6102e-119">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="6102e-119">-EndIpAddress</span></span>
<span data-ttu-id="6102e-120">Die End-IP-Adresse der Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="6102e-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="6102e-121">Muss das IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="6102e-121">Must be IPv4 format.</span></span>
<span data-ttu-id="6102e-122">Muss größer als oder gleich "startIpAddress" sein.</span><span class="sxs-lookup"><span data-stu-id="6102e-122">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="6102e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6102e-123">-Name</span></span>
<span data-ttu-id="6102e-124">Der Name der Firerwallregel für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="6102e-124">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="6102e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6102e-125">-ResourceGroupName</span></span>
<span data-ttu-id="6102e-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6102e-126">Resource group name.</span></span>

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

### <span data-ttu-id="6102e-127">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="6102e-127">-StartIpAddress</span></span>
<span data-ttu-id="6102e-128">Die Start-IP-Adresse der Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="6102e-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="6102e-129">Muss das IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="6102e-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6102e-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6102e-130">-WorkspaceName</span></span>
<span data-ttu-id="6102e-131">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="6102e-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6102e-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6102e-132">-WorkspaceObject</span></span>
<span data-ttu-id="6102e-133">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6102e-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6102e-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6102e-134">-Confirm</span></span>
<span data-ttu-id="6102e-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6102e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6102e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6102e-136">-WhatIf</span></span>
<span data-ttu-id="6102e-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6102e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6102e-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6102e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6102e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6102e-139">CommonParameters</span></span>
<span data-ttu-id="6102e-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6102e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6102e-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6102e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6102e-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6102e-142">INPUTS</span></span>

### <span data-ttu-id="6102e-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6102e-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6102e-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6102e-144">OUTPUTS</span></span>

### <span data-ttu-id="6102e-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6102e-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="6102e-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6102e-146">NOTES</span></span>

## <span data-ttu-id="6102e-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6102e-147">RELATED LINKS</span></span>
