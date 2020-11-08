---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 6094c8d7e75136c9a9abf220ccfcb8775bda5dd7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010120"
---
# <span data-ttu-id="5f7e8-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5f7e8-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="5f7e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f7e8-102">SYNOPSIS</span></span>
<span data-ttu-id="5f7e8-103">Löscht eine Synapse Analytics-Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="5f7e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f7e8-104">SYNTAX</span></span>

### <span data-ttu-id="5f7e8-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f7e8-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f7e8-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f7e8-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f7e8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f7e8-107">DESCRIPTION</span></span>
<span data-ttu-id="5f7e8-108">Das Cmdlet **Remove-AzSynapseFirewallRule** löscht permanent eine Azure Synapse Analytics-Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="5f7e8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f7e8-109">EXAMPLES</span></span>

### <span data-ttu-id="5f7e8-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5f7e8-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="5f7e8-111">Dieser Befehl löscht die Firewallregel mit dem Namen ContosoFirewallRule unter Arbeitsbereich ContosoWorkspace mit dem Namen ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="5f7e8-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5f7e8-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="5f7e8-113">Dieser Befehl löscht die Firewall-Regel namens ContosoFirewallRule unter einem Arbeitsbereich durch Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="5f7e8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f7e8-114">PARAMETERS</span></span>

### <span data-ttu-id="5f7e8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f7e8-115">-AsJob</span></span>
<span data-ttu-id="5f7e8-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5f7e8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5f7e8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f7e8-117">-DefaultProfile</span></span>
<span data-ttu-id="5f7e8-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f7e8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5f7e8-119">-Name</span></span>
<span data-ttu-id="5f7e8-120">Der Name der firerwall-Regel für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-120">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="5f7e8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f7e8-121">-PassThru</span></span>
<span data-ttu-id="5f7e8-122">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-122">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5f7e8-123">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5f7e8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f7e8-124">-ResourceGroupName</span></span>
<span data-ttu-id="5f7e8-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-125">Resource group name.</span></span>

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

### <span data-ttu-id="5f7e8-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5f7e8-126">-WorkspaceName</span></span>
<span data-ttu-id="5f7e8-127">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="5f7e8-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5f7e8-128">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="5f7e8-128">-WorkspaceObject</span></span>
<span data-ttu-id="5f7e8-129">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5f7e8-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5f7e8-130">-Confirm</span></span>
<span data-ttu-id="5f7e8-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f7e8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f7e8-132">-WhatIf</span></span>
<span data-ttu-id="5f7e8-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f7e8-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f7e8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f7e8-135">CommonParameters</span></span>
<span data-ttu-id="5f7e8-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f7e8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f7e8-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f7e8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f7e8-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f7e8-138">INPUTS</span></span>

### <span data-ttu-id="5f7e8-139">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5f7e8-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5f7e8-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f7e8-140">OUTPUTS</span></span>

### <span data-ttu-id="5f7e8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5f7e8-141">System.Boolean</span></span>

## <span data-ttu-id="5f7e8-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f7e8-142">NOTES</span></span>

## <span data-ttu-id="5f7e8-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f7e8-143">RELATED LINKS</span></span>
