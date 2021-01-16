---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
ms.openlocfilehash: 67ef03656b97514d1d39ae72f0f0d52d5b302619
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295924"
---
# <span data-ttu-id="5a278-101">New-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5a278-101">New-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="5a278-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a278-102">SYNOPSIS</span></span>
<span data-ttu-id="5a278-103">Erstellt eine neue Firewallregel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="5a278-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="5a278-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a278-104">SYNTAX</span></span>

### <span data-ttu-id="5a278-105">CreateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a278-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5a278-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="5a278-106">AllowAll</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5a278-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="5a278-107">ClientIPAddress</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5a278-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a278-108">DESCRIPTION</span></span>
<span data-ttu-id="5a278-109">Erstellt eine neue Firewallregel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="5a278-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="5a278-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5a278-110">EXAMPLES</span></span>

### <span data-ttu-id="5a278-111">Beispiel 1: Erstellen einer neuen MySql -Server-Firewallregel</span><span class="sxs-lookup"><span data-stu-id="5a278-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="5a278-112">Diese Cmdlets erstellen eine MySql-Server-Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="5a278-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="5a278-113">Beispiel 2: Erstellen einer neuen MySql-Firewallregel mit "-ClientIPAddress".</span><span class="sxs-lookup"><span data-stu-id="5a278-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="5a278-114">Diese Cmdlets erstellen eine MySql-Firewallregel mit "-ClientIPAddress".</span><span class="sxs-lookup"><span data-stu-id="5a278-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="5a278-115">Beispiel 3: Erstellen einer neuen MySql-Firewallregel, um alle IPs zu erlauben</span><span class="sxs-lookup"><span data-stu-id="5a278-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="5a278-116">Mit diesen Cmdlets wird eine neue MySql-Firewallregel erstellt, damit alle IPs zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5a278-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="5a278-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a278-117">PARAMETERS</span></span>

### <span data-ttu-id="5a278-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="5a278-118">-AllowAll</span></span>
<span data-ttu-id="5a278-119">Vorhanden, damit alle IPs des Bereichs von 0.0.0.0 bis 255.255.255.255 zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5a278-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="5a278-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a278-120">-AsJob</span></span>
<span data-ttu-id="5a278-121">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="5a278-121">Run the command as a job</span></span>

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

### <span data-ttu-id="5a278-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="5a278-122">-ClientIPAddress</span></span>
<span data-ttu-id="5a278-123">Vom Client angegebene einzelne IP der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="5a278-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="5a278-124">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="5a278-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="5a278-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a278-125">-DefaultProfile</span></span>
<span data-ttu-id="5a278-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a278-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a278-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="5a278-127">-EndIPAddress</span></span>
<span data-ttu-id="5a278-128">Die End-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="5a278-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="5a278-129">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="5a278-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="5a278-130">-Name</span><span class="sxs-lookup"><span data-stu-id="5a278-130">-Name</span></span>
<span data-ttu-id="5a278-131">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="5a278-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="5a278-132">Wenn nichts angegeben wird, ist der Standardwert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="5a278-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="5a278-133">Wenn "AllowAll" vorhanden ist, ist der Standardname AllowAll_yyyy-MM-dd_HH-mm-ss.</span><span class="sxs-lookup"><span data-stu-id="5a278-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="5a278-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5a278-134">-NoWait</span></span>
<span data-ttu-id="5a278-135">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="5a278-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5a278-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a278-136">-ResourceGroupName</span></span>
<span data-ttu-id="5a278-137">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5a278-137">The name of the resource group.</span></span>
<span data-ttu-id="5a278-138">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="5a278-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5a278-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5a278-139">-ServerName</span></span>
<span data-ttu-id="5a278-140">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="5a278-140">The name of the server.</span></span>

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

### <span data-ttu-id="5a278-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="5a278-141">-StartIPAddress</span></span>
<span data-ttu-id="5a278-142">Die Start-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="5a278-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="5a278-143">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="5a278-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="5a278-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a278-144">-SubscriptionId</span></span>
<span data-ttu-id="5a278-145">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="5a278-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5a278-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a278-146">-Confirm</span></span>
<span data-ttu-id="5a278-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a278-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a278-148">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5a278-148">-WhatIf</span></span>
<span data-ttu-id="5a278-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a278-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a278-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a278-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a278-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a278-151">CommonParameters</span></span>
<span data-ttu-id="5a278-152">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a278-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a278-153">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a278-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a278-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5a278-154">INPUTS</span></span>

## <span data-ttu-id="5a278-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5a278-155">OUTPUTS</span></span>

### <span data-ttu-id="5a278-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5a278-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="5a278-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5a278-157">NOTES</span></span>

<span data-ttu-id="5a278-158">ALIASE</span><span class="sxs-lookup"><span data-stu-id="5a278-158">ALIASES</span></span>

## <span data-ttu-id="5a278-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5a278-159">RELATED LINKS</span></span>

