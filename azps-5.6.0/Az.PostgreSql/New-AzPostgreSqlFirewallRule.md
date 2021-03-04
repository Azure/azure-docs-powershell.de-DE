---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/new-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 7ba5a72d161f07ae55669ddfa9d0e399d7cf81ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944812"
---
# <span data-ttu-id="5a4c6-101">New-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5a4c6-101">New-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="5a4c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a4c6-102">SYNOPSIS</span></span>
<span data-ttu-id="5a4c6-103">Erstellt eine neue Firewallregel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="5a4c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a4c6-104">SYNTAX</span></span>

### <span data-ttu-id="5a4c6-105">CreateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a4c6-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5a4c6-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="5a4c6-106">AllowAll</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5a4c6-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="5a4c6-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5a4c6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a4c6-108">DESCRIPTION</span></span>
<span data-ttu-id="5a4c6-109">Erstellt eine neue Firewallregel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="5a4c6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5a4c6-110">EXAMPLES</span></span>

### <span data-ttu-id="5a4c6-111">Beispiel 1: Erstellen einer neuen PostgreSql-Serverfirewallregel</span><span class="sxs-lookup"><span data-stu-id="5a4c6-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="5a4c6-112">Mit diesen Cmdlets wird eine PostgreSql-Serverfirewallregel erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="5a4c6-113">Beispiel 2: Erstellen einer neuen PostgreSql-Firewallregel mit -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="5a4c6-114">Diese Cmdlets erstellen eine PostgreSql-Firewallregel mit -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="5a4c6-115">Beispiel 3: Erstellen einer neuen PostgreSql-Firewallregel zum Zulassen aller IPs</span><span class="sxs-lookup"><span data-stu-id="5a4c6-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="5a4c6-116">Diese Cmdlets erstellen eine neue PostgreSql-Firewallregel, um alle IPs zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="5a4c6-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5a4c6-117">PARAMETERS</span></span>

### <span data-ttu-id="5a4c6-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="5a4c6-118">-AllowAll</span></span>
<span data-ttu-id="5a4c6-119">Präsentieren, um alle Bereichs-IPs von 0,0,0,0 bis 255,255.255.255 zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="5a4c6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a4c6-120">-AsJob</span></span>
<span data-ttu-id="5a4c6-121">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="5a4c6-121">Run the command as a job</span></span>

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

### <span data-ttu-id="5a4c6-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="5a4c6-122">-ClientIPAddress</span></span>
<span data-ttu-id="5a4c6-123">Client hat einzelne IP der Serverfirewallregel angegeben.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="5a4c6-124">Muss das IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="5a4c6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a4c6-125">-DefaultProfile</span></span>
<span data-ttu-id="5a4c6-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a4c6-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="5a4c6-127">-EndIPAddress</span></span>
<span data-ttu-id="5a4c6-128">Die End-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="5a4c6-129">Muss das IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="5a4c6-130">-Name</span><span class="sxs-lookup"><span data-stu-id="5a4c6-130">-Name</span></span>
<span data-ttu-id="5a4c6-131">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-131">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="5a4c6-132">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5a4c6-132">-NoWait</span></span>
<span data-ttu-id="5a4c6-133">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="5a4c6-133">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5a4c6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a4c6-134">-ResourceGroupName</span></span>
<span data-ttu-id="5a4c6-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-135">The name of the resource group.</span></span>
<span data-ttu-id="5a4c6-136">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-136">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5a4c6-137">-Servername</span><span class="sxs-lookup"><span data-stu-id="5a4c6-137">-ServerName</span></span>
<span data-ttu-id="5a4c6-138">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-138">The name of the server.</span></span>

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

### <span data-ttu-id="5a4c6-139">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="5a4c6-139">-StartIPAddress</span></span>
<span data-ttu-id="5a4c6-140">Die Start-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-140">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="5a4c6-141">Muss das IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-141">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="5a4c6-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a4c6-142">-SubscriptionId</span></span>
<span data-ttu-id="5a4c6-143">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5a4c6-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5a4c6-144">-Confirm</span></span>
<span data-ttu-id="5a4c6-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a4c6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a4c6-146">-WhatIf</span></span>
<span data-ttu-id="5a4c6-147">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a4c6-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a4c6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a4c6-149">CommonParameters</span></span>
<span data-ttu-id="5a4c6-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a4c6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a4c6-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a4c6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a4c6-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5a4c6-152">INPUTS</span></span>

## <span data-ttu-id="5a4c6-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5a4c6-153">OUTPUTS</span></span>

### <span data-ttu-id="5a4c6-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5a4c6-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="5a4c6-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5a4c6-155">NOTES</span></span>

<span data-ttu-id="5a4c6-156">ALIASE</span><span class="sxs-lookup"><span data-stu-id="5a4c6-156">ALIASES</span></span>

## <span data-ttu-id="5a4c6-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5a4c6-157">RELATED LINKS</span></span>

