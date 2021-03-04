---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 6df0e33ff94be7bf5e060b929206c09180d830f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923160"
---
# <span data-ttu-id="c60a5-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c60a5-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="c60a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c60a5-102">SYNOPSIS</span></span>
<span data-ttu-id="c60a5-103">Löscht eine Synapse Analytics-Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="c60a5-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="c60a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c60a5-104">SYNTAX</span></span>

### <span data-ttu-id="c60a5-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c60a5-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c60a5-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c60a5-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c60a5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c60a5-107">DESCRIPTION</span></span>
<span data-ttu-id="c60a5-108">Das **Cmdlet Remove-AzSynapseFirewallRule** löscht eine Azure Synapse Analytics-Firewallregel endgültig.</span><span class="sxs-lookup"><span data-stu-id="c60a5-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="c60a5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c60a5-109">EXAMPLES</span></span>

### <span data-ttu-id="c60a5-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c60a5-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="c60a5-111">Mit diesem Befehl wird die Firewallregel "ContosoFirewallRule" unter dem Arbeitsbereich ContosoWorkspace mit dem Namen ContosoFirewallRule gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c60a5-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="c60a5-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c60a5-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="c60a5-113">Mit diesem Befehl wird die Firewallregel "ContosoFirewallRule" unter einem Arbeitsbereich über die Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c60a5-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="c60a5-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c60a5-114">PARAMETERS</span></span>

### <span data-ttu-id="c60a5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c60a5-115">-AsJob</span></span>
<span data-ttu-id="c60a5-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c60a5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c60a5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c60a5-117">-DefaultProfile</span></span>
<span data-ttu-id="c60a5-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c60a5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c60a5-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="c60a5-119">-Force</span></span>
<span data-ttu-id="c60a5-120">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="c60a5-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c60a5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c60a5-121">-Name</span></span>
<span data-ttu-id="c60a5-122">Der Name der Firerwallregel für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="c60a5-122">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="c60a5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c60a5-123">-PassThru</span></span>
<span data-ttu-id="c60a5-124">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c60a5-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c60a5-125">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="c60a5-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c60a5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c60a5-126">-ResourceGroupName</span></span>
<span data-ttu-id="c60a5-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c60a5-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c60a5-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c60a5-128">-WorkspaceName</span></span>
<span data-ttu-id="c60a5-129">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="c60a5-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c60a5-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c60a5-130">-WorkspaceObject</span></span>
<span data-ttu-id="c60a5-131">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c60a5-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c60a5-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c60a5-132">-Confirm</span></span>
<span data-ttu-id="c60a5-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c60a5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c60a5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c60a5-134">-WhatIf</span></span>
<span data-ttu-id="c60a5-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c60a5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c60a5-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c60a5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c60a5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c60a5-137">CommonParameters</span></span>
<span data-ttu-id="c60a5-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c60a5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c60a5-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c60a5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c60a5-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c60a5-140">INPUTS</span></span>

### <span data-ttu-id="c60a5-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c60a5-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c60a5-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c60a5-142">OUTPUTS</span></span>

### <span data-ttu-id="c60a5-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c60a5-143">System.Boolean</span></span>

## <span data-ttu-id="c60a5-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c60a5-144">NOTES</span></span>

## <span data-ttu-id="c60a5-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c60a5-145">RELATED LINKS</span></span>
