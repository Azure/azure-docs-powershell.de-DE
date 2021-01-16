---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 8dd3321804afb2f7901a8acd22cfdab3dd990c41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369212"
---
# <span data-ttu-id="a05f4-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a05f4-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="a05f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a05f4-102">SYNOPSIS</span></span>
<span data-ttu-id="a05f4-103">Löscht eine Synapse Analytics-Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="a05f4-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="a05f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a05f4-104">SYNTAX</span></span>

### <span data-ttu-id="a05f4-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a05f4-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a05f4-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a05f4-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a05f4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a05f4-107">DESCRIPTION</span></span>
<span data-ttu-id="a05f4-108">Das **Cmdlet "Remove-AzSynapseFirewallRule"** löscht eine Azure Synapse Analytics-Firewallregel endgültig.</span><span class="sxs-lookup"><span data-stu-id="a05f4-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="a05f4-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a05f4-109">EXAMPLES</span></span>

### <span data-ttu-id="a05f4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a05f4-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="a05f4-111">Mit diesem Befehl wird die Firewallregel namens "ContosoFirewallRule" im Arbeitsbereich "ContosoWorkspace" mit dem Namen "ContosoFirewallRule" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a05f4-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="a05f4-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a05f4-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="a05f4-113">Mit diesem Befehl wird die Firewallregel namens "ContosoFirewallRule" in einem Arbeitsbereich über die Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a05f4-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="a05f4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a05f4-114">PARAMETERS</span></span>

### <span data-ttu-id="a05f4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a05f4-115">-AsJob</span></span>
<span data-ttu-id="a05f4-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a05f4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a05f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a05f4-117">-DefaultProfile</span></span>
<span data-ttu-id="a05f4-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a05f4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a05f4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a05f4-119">-Force</span></span>
<span data-ttu-id="a05f4-120">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="a05f4-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a05f4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a05f4-121">-Name</span></span>
<span data-ttu-id="a05f4-122">Der Name der Firewallregel für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a05f4-122">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="a05f4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a05f4-123">-PassThru</span></span>
<span data-ttu-id="a05f4-124">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="a05f4-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a05f4-125">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a05f4-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a05f4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a05f4-126">-ResourceGroupName</span></span>
<span data-ttu-id="a05f4-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="a05f4-127">Resource group name.</span></span>

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

### <span data-ttu-id="a05f4-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a05f4-128">-WorkspaceName</span></span>
<span data-ttu-id="a05f4-129">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a05f4-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a05f4-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a05f4-130">-WorkspaceObject</span></span>
<span data-ttu-id="a05f4-131">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a05f4-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a05f4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a05f4-132">-Confirm</span></span>
<span data-ttu-id="a05f4-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a05f4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a05f4-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a05f4-134">-WhatIf</span></span>
<span data-ttu-id="a05f4-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a05f4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a05f4-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a05f4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a05f4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a05f4-137">CommonParameters</span></span>
<span data-ttu-id="a05f4-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a05f4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a05f4-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a05f4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a05f4-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a05f4-140">INPUTS</span></span>

### <span data-ttu-id="a05f4-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a05f4-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a05f4-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a05f4-142">OUTPUTS</span></span>

### <span data-ttu-id="a05f4-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a05f4-143">System.Boolean</span></span>

## <span data-ttu-id="a05f4-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a05f4-144">NOTES</span></span>

## <span data-ttu-id="a05f4-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a05f4-145">RELATED LINKS</span></span>
