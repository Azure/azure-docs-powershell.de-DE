---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 9188a1cc8dde39db4d755fb2059f3633fc85ead8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175349"
---
# <span data-ttu-id="87e0c-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="87e0c-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="87e0c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="87e0c-103">Aktualisiert eine Synapse Analytics-Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="87e0c-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="87e0c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87e0c-104">SYNTAX</span></span>

### <span data-ttu-id="87e0c-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="87e0c-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87e0c-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87e0c-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87e0c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87e0c-107">DESCRIPTION</span></span>
<span data-ttu-id="87e0c-108">Mit dem Cmdlet **Update-AzSynapseFirewallRule** wird eine Azure Synapse Analytics-Firewallregel geändert.</span><span class="sxs-lookup"><span data-stu-id="87e0c-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="87e0c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87e0c-109">EXAMPLES</span></span>

### <span data-ttu-id="87e0c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="87e0c-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="87e0c-111">Dieser Befehl aktualisiert die Firewall-Regel mit dem Namen ContosoFirewallRule unter Arbeitsbereich ContosoWorkspace mit dem Namen ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="87e0c-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="87e0c-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="87e0c-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="87e0c-113">Dieser Befehl aktualisiert die Firewall-Regel mit dem Namen ContosoFirewallRule unter einem Arbeitsbereich durch Pipeline.</span><span class="sxs-lookup"><span data-stu-id="87e0c-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="87e0c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="87e0c-114">PARAMETERS</span></span>

### <span data-ttu-id="87e0c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87e0c-115">-AsJob</span></span>
<span data-ttu-id="87e0c-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="87e0c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="87e0c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87e0c-117">-DefaultProfile</span></span>
<span data-ttu-id="87e0c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="87e0c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87e0c-119">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="87e0c-119">-EndIpAddress</span></span>
<span data-ttu-id="87e0c-120">Die End-IP-Adresse der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="87e0c-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="87e0c-121">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="87e0c-121">Must be IPv4 format.</span></span>
<span data-ttu-id="87e0c-122">Muss größer als oder gleich startIpAddress sein.</span><span class="sxs-lookup"><span data-stu-id="87e0c-122">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="87e0c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="87e0c-123">-Name</span></span>
<span data-ttu-id="87e0c-124">Der Name der firerwall-Regel für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="87e0c-124">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="87e0c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87e0c-125">-ResourceGroupName</span></span>
<span data-ttu-id="87e0c-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="87e0c-126">Resource group name.</span></span>

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

### <span data-ttu-id="87e0c-127">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="87e0c-127">-StartIpAddress</span></span>
<span data-ttu-id="87e0c-128">Die Start-IP-Adresse der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="87e0c-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="87e0c-129">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="87e0c-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="87e0c-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="87e0c-130">-WorkspaceName</span></span>
<span data-ttu-id="87e0c-131">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="87e0c-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="87e0c-132">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="87e0c-132">-WorkspaceObject</span></span>
<span data-ttu-id="87e0c-133">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="87e0c-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="87e0c-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="87e0c-134">-Confirm</span></span>
<span data-ttu-id="87e0c-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87e0c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87e0c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87e0c-136">-WhatIf</span></span>
<span data-ttu-id="87e0c-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87e0c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87e0c-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87e0c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87e0c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e0c-139">CommonParameters</span></span>
<span data-ttu-id="87e0c-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87e0c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e0c-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87e0c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e0c-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87e0c-142">INPUTS</span></span>

### <span data-ttu-id="87e0c-143">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="87e0c-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="87e0c-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87e0c-144">OUTPUTS</span></span>

### <span data-ttu-id="87e0c-145">Microsoft. Azure. Commands. Synapse. Models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="87e0c-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="87e0c-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="87e0c-146">NOTES</span></span>

## <span data-ttu-id="87e0c-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87e0c-147">RELATED LINKS</span></span>
