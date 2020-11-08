---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: b4579d01ed6dd5a7d742cbb82afb424151579772
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007675"
---
# <span data-ttu-id="1156a-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1156a-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="1156a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1156a-102">SYNOPSIS</span></span>
<span data-ttu-id="1156a-103">Erstellt eine Synapse Analytics-Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="1156a-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="1156a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1156a-104">SYNTAX</span></span>

### <span data-ttu-id="1156a-105">CreateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1156a-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1156a-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="1156a-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1156a-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1156a-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1156a-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="1156a-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1156a-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1156a-109">DESCRIPTION</span></span>
<span data-ttu-id="1156a-110">Das Cmdlet **New-AzSynapseFirewallRule** erstellt eine Azure Synapse Analytics-Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="1156a-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="1156a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1156a-111">EXAMPLES</span></span>

### <span data-ttu-id="1156a-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1156a-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="1156a-113">Dieser Befehl erstellt eine Firewallregel mit dem Namen ContosoFirewallRule unter Arbeitsbereich ContosoWorkspace mit dem Namen ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="1156a-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="1156a-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1156a-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="1156a-115">Dieser Befehl erstellt eine Firewallregel mit dem Namen ContosoFirewallRule unter einem Arbeitsbereich durch Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1156a-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="1156a-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="1156a-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="1156a-117">Mit diesem Befehl wird eine Firewall-Regel erstellt, die alle Azure IPS unter einem Arbeitsbereich zulässt.</span><span class="sxs-lookup"><span data-stu-id="1156a-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="1156a-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="1156a-118">PARAMETERS</span></span>

### <span data-ttu-id="1156a-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="1156a-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="1156a-120">Erstellt eine spezielle Firewallregel, die es allen Azure IPS ermöglicht, auf Access zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="1156a-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

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

### <span data-ttu-id="1156a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1156a-121">-AsJob</span></span>
<span data-ttu-id="1156a-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1156a-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1156a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1156a-123">-DefaultProfile</span></span>
<span data-ttu-id="1156a-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1156a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1156a-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="1156a-125">-EndIpAddress</span></span>
<span data-ttu-id="1156a-126">Die End-IP-Adresse der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="1156a-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="1156a-127">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="1156a-127">Must be IPv4 format.</span></span>
<span data-ttu-id="1156a-128">Muss größer als oder gleich startIpAddress sein.</span><span class="sxs-lookup"><span data-stu-id="1156a-128">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="1156a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="1156a-129">-Name</span></span>
<span data-ttu-id="1156a-130">Der Name der firerwall-Regel für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="1156a-130">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="1156a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1156a-131">-ResourceGroupName</span></span>
<span data-ttu-id="1156a-132">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1156a-132">Resource group name.</span></span>

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

### <span data-ttu-id="1156a-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="1156a-133">-StartIpAddress</span></span>
<span data-ttu-id="1156a-134">Die Start-IP-Adresse der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="1156a-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="1156a-135">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="1156a-135">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="1156a-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1156a-136">-WorkspaceName</span></span>
<span data-ttu-id="1156a-137">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="1156a-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1156a-138">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="1156a-138">-WorkspaceObject</span></span>
<span data-ttu-id="1156a-139">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="1156a-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1156a-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1156a-140">-Confirm</span></span>
<span data-ttu-id="1156a-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1156a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1156a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1156a-142">-WhatIf</span></span>
<span data-ttu-id="1156a-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1156a-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1156a-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1156a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1156a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1156a-145">CommonParameters</span></span>
<span data-ttu-id="1156a-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1156a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1156a-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1156a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1156a-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1156a-148">INPUTS</span></span>

### <span data-ttu-id="1156a-149">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1156a-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1156a-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1156a-150">OUTPUTS</span></span>

### <span data-ttu-id="1156a-151">Microsoft. Azure. Commands. Synapse. Models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1156a-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="1156a-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="1156a-152">NOTES</span></span>

## <span data-ttu-id="1156a-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1156a-153">RELATED LINKS</span></span>
