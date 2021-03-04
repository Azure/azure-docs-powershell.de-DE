---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
ms.openlocfilehash: 84c5e5e49d80c04bcbfe3f7ec72e018ac7984bec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921947"
---
# <span data-ttu-id="41eb5-101">New-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="41eb5-101">New-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="41eb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="41eb5-103">Erstellt eine neue Firewallregel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="41eb5-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="41eb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41eb5-104">SYNTAX</span></span>

### <span data-ttu-id="41eb5-105">CreateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="41eb5-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="41eb5-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="41eb5-106">AllowAll</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="41eb5-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="41eb5-107">ClientIPAddress</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="41eb5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41eb5-108">DESCRIPTION</span></span>
<span data-ttu-id="41eb5-109">Erstellt eine neue Firewallregel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="41eb5-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="41eb5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="41eb5-110">EXAMPLES</span></span>

### <span data-ttu-id="41eb5-111">Beispiel 1: Erstellen einer neuen MySql-Serverfirewallregel</span><span class="sxs-lookup"><span data-stu-id="41eb5-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="41eb5-112">Mit diesen Cmdlets wird eine MySql-Serverfirewallregel erstellt.</span><span class="sxs-lookup"><span data-stu-id="41eb5-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="41eb5-113">Beispiel 2: Erstellen einer neuen MySql-Firewallregel mit -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="41eb5-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="41eb5-114">Diese Cmdlets erstellen eine MySql-Firewallregel mit -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="41eb5-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="41eb5-115">Beispiel 3: Erstellen einer neuen MySql-Firewallregel zum Zulassen aller IPs</span><span class="sxs-lookup"><span data-stu-id="41eb5-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="41eb5-116">Diese Cmdlets erstellen eine neue MySql-Firewallregel, um alle IPs zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="41eb5-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="41eb5-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="41eb5-117">PARAMETERS</span></span>

### <span data-ttu-id="41eb5-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="41eb5-118">-AllowAll</span></span>
<span data-ttu-id="41eb5-119">Präsentieren, um alle Bereichs-IPs von 0,0,0,0 bis 255,255.255.255 zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="41eb5-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AllowAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41eb5-120">-AsJob</span></span>
<span data-ttu-id="41eb5-121">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="41eb5-121">Run the command as a job</span></span>

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

### <span data-ttu-id="41eb5-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="41eb5-122">-ClientIPAddress</span></span>
<span data-ttu-id="41eb5-123">Client hat einzelne IP der Serverfirewallregel angegeben.</span><span class="sxs-lookup"><span data-stu-id="41eb5-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="41eb5-124">Muss das IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="41eb5-124">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41eb5-125">-DefaultProfile</span></span>
<span data-ttu-id="41eb5-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41eb5-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="41eb5-127">-EndIPAddress</span></span>
<span data-ttu-id="41eb5-128">Die End-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="41eb5-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="41eb5-129">Muss das IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="41eb5-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-130">-Name</span><span class="sxs-lookup"><span data-stu-id="41eb5-130">-Name</span></span>
<span data-ttu-id="41eb5-131">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="41eb5-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="41eb5-132">Wenn nicht angegeben, ist die Standardeinstellung nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="41eb5-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="41eb5-133">Wenn AllowAll vorhanden ist, ist der Standardname AllowAll_yyyy-MM-dd_HH-mm-ss.</span><span class="sxs-lookup"><span data-stu-id="41eb5-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="41eb5-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="41eb5-134">-NoWait</span></span>
<span data-ttu-id="41eb5-135">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="41eb5-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="41eb5-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41eb5-136">-ResourceGroupName</span></span>
<span data-ttu-id="41eb5-137">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="41eb5-137">The name of the resource group.</span></span>
<span data-ttu-id="41eb5-138">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="41eb5-138">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-139">-Servername</span><span class="sxs-lookup"><span data-stu-id="41eb5-139">-ServerName</span></span>
<span data-ttu-id="41eb5-140">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="41eb5-140">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="41eb5-141">-StartIPAddress</span></span>
<span data-ttu-id="41eb5-142">Die Start-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="41eb5-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="41eb5-143">Muss das IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="41eb5-143">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41eb5-144">-SubscriptionId</span></span>
<span data-ttu-id="41eb5-145">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="41eb5-145">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="41eb5-146">-Confirm</span></span>
<span data-ttu-id="41eb5-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="41eb5-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41eb5-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41eb5-148">-WhatIf</span></span>
<span data-ttu-id="41eb5-149">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41eb5-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41eb5-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41eb5-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41eb5-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41eb5-151">CommonParameters</span></span>
<span data-ttu-id="41eb5-152">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41eb5-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41eb5-153">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41eb5-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41eb5-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="41eb5-154">INPUTS</span></span>

## <span data-ttu-id="41eb5-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="41eb5-155">OUTPUTS</span></span>

### <span data-ttu-id="41eb5-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="41eb5-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="41eb5-157">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="41eb5-157">NOTES</span></span>

<span data-ttu-id="41eb5-158">ALIASE</span><span class="sxs-lookup"><span data-stu-id="41eb5-158">ALIASES</span></span>

## <span data-ttu-id="41eb5-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="41eb5-159">RELATED LINKS</span></span>

