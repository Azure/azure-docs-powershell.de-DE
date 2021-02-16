---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: b4579d01ed6dd5a7d742cbb82afb424151579772
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164572"
---
# <span data-ttu-id="a3c1b-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a3c1b-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="a3c1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="a3c1b-103">Erstellt eine Synapse Analytics-Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="a3c1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3c1b-104">SYNTAX</span></span>

### <span data-ttu-id="a3c1b-105">CreateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3c1b-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3c1b-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3c1b-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3c1b-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3c1b-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3c1b-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3c1b-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3c1b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3c1b-109">DESCRIPTION</span></span>
<span data-ttu-id="a3c1b-110">Das **Cmdlet "New-AzSynapseFirewallRule"** erstellt eine Azure Synapse Analytics-Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="a3c1b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a3c1b-111">EXAMPLES</span></span>

### <span data-ttu-id="a3c1b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a3c1b-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="a3c1b-113">Mit diesem Befehl wird eine Firewallregel namens "ContosoFirewallRule" im Arbeitsbereich "ContosoWorkspace" mit dem Namen "ContosoFirewallRule" erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="a3c1b-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a3c1b-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="a3c1b-115">Mit diesem Befehl wird eine Firewallregel namens "ContosoFirewallRule" in einem Arbeitsbereich über die Pipeline erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="a3c1b-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a3c1b-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="a3c1b-117">Mit diesem Befehl wird eine Firewallregel erstellt, die alle Azure-IPs in einem Arbeitsbereich zu erlaubt.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="a3c1b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3c1b-118">PARAMETERS</span></span>

### <span data-ttu-id="a3c1b-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="a3c1b-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="a3c1b-120">Erstellt eine spezielle Firewallregel, die allen Azure IPs Zugriff zulässt.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateByNameAllowAllIpParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c1b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3c1b-121">-AsJob</span></span>
<span data-ttu-id="a3c1b-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a3c1b-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3c1b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3c1b-123">-DefaultProfile</span></span>
<span data-ttu-id="a3c1b-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3c1b-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="a3c1b-125">-EndIpAddress</span></span>
<span data-ttu-id="a3c1b-126">Die End-IP-Adresse der Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="a3c1b-127">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-127">Must be IPv4 format.</span></span>
<span data-ttu-id="a3c1b-128">Muss größer gleich "startIpAddress" sein.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-128">Must be greater than or equal to startIpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c1b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="a3c1b-129">-Name</span></span>
<span data-ttu-id="a3c1b-130">Der Name der Firewallregel für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-130">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c1b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3c1b-131">-ResourceGroupName</span></span>
<span data-ttu-id="a3c1b-132">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c1b-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="a3c1b-133">-StartIpAddress</span></span>
<span data-ttu-id="a3c1b-134">Die Start-IP-Adresse der Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="a3c1b-135">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-135">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c1b-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a3c1b-136">-WorkspaceName</span></span>
<span data-ttu-id="a3c1b-137">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c1b-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a3c1b-138">-WorkspaceObject</span></span>
<span data-ttu-id="a3c1b-139">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3c1b-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3c1b-140">-Confirm</span></span>
<span data-ttu-id="a3c1b-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3c1b-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a3c1b-142">-WhatIf</span></span>
<span data-ttu-id="a3c1b-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3c1b-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3c1b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3c1b-145">CommonParameters</span></span>
<span data-ttu-id="a3c1b-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3c1b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3c1b-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3c1b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3c1b-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a3c1b-148">INPUTS</span></span>

### <span data-ttu-id="a3c1b-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a3c1b-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a3c1b-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a3c1b-150">OUTPUTS</span></span>

### <span data-ttu-id="a3c1b-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a3c1b-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="a3c1b-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a3c1b-152">NOTES</span></span>

## <span data-ttu-id="a3c1b-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a3c1b-153">RELATED LINKS</span></span>
