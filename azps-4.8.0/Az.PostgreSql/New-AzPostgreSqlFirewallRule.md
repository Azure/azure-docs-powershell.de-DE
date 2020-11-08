---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: bafd0e20530198da87c1fa3ece36905e73307a42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008988"
---
# <span data-ttu-id="eb636-101">New-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="eb636-101">New-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="eb636-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb636-102">SYNOPSIS</span></span>
<span data-ttu-id="eb636-103">Erstellt eine neue Firewall-Regel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="eb636-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="eb636-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb636-104">SYNTAX</span></span>

### <span data-ttu-id="eb636-105">Createexpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="eb636-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eb636-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="eb636-106">AllowAll</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="eb636-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="eb636-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eb636-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb636-108">DESCRIPTION</span></span>
<span data-ttu-id="eb636-109">Erstellt eine neue Firewall-Regel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="eb636-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="eb636-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb636-110">EXAMPLES</span></span>

### <span data-ttu-id="eb636-111">Beispiel 1: Erstellen einer neuen PostgreSQL-Server Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="eb636-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="eb636-112">Diese Cmdlets erstellen eine Firewall-Regel für den PostgreSQL-Server.</span><span class="sxs-lookup"><span data-stu-id="eb636-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="eb636-113">Beispiel 2: Erstellen einer neuen PostgreSQL-Firewallregel mithilfe von-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="eb636-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="eb636-114">Diese Cmdlets erstellen eine PostgreSQL-Firewallregel mithilfe von-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="eb636-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="eb636-115">Beispiel 3: Erstellen einer neuen PostgreSQL-Firewall-Regel, um alle IPS zuzulassen</span><span class="sxs-lookup"><span data-stu-id="eb636-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="eb636-116">Diese Cmdlets erstellen eine neue PostgreSQL-Firewallregel, damit alle IPS zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="eb636-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="eb636-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb636-117">PARAMETERS</span></span>

### <span data-ttu-id="eb636-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="eb636-118">-AllowAll</span></span>
<span data-ttu-id="eb636-119">Präsentieren, damit alle IP-Adressen von 0.0.0.0 zu 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="eb636-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="eb636-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb636-120">-AsJob</span></span>
<span data-ttu-id="eb636-121">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="eb636-121">Run the command as a job</span></span>

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

### <span data-ttu-id="eb636-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="eb636-122">-ClientIPAddress</span></span>
<span data-ttu-id="eb636-123">Client hat eine einzelne IP-Adresse der Server Firewall-Regel angegeben.</span><span class="sxs-lookup"><span data-stu-id="eb636-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="eb636-124">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="eb636-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="eb636-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb636-125">-DefaultProfile</span></span>
<span data-ttu-id="eb636-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eb636-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb636-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="eb636-127">-EndIPAddress</span></span>
<span data-ttu-id="eb636-128">Die End-IP-Adresse der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="eb636-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="eb636-129">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="eb636-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="eb636-130">-Name</span><span class="sxs-lookup"><span data-stu-id="eb636-130">-Name</span></span>
<span data-ttu-id="eb636-131">Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="eb636-131">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="eb636-132">-Nowait</span><span class="sxs-lookup"><span data-stu-id="eb636-132">-NoWait</span></span>
<span data-ttu-id="eb636-133">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="eb636-133">Run the command asynchronously</span></span>

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

### <span data-ttu-id="eb636-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb636-134">-ResourceGroupName</span></span>
<span data-ttu-id="eb636-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="eb636-135">The name of the resource group.</span></span>
<span data-ttu-id="eb636-136">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="eb636-136">The name is case insensitive.</span></span>

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

### <span data-ttu-id="eb636-137">-Servername</span><span class="sxs-lookup"><span data-stu-id="eb636-137">-ServerName</span></span>
<span data-ttu-id="eb636-138">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="eb636-138">The name of the server.</span></span>

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

### <span data-ttu-id="eb636-139">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="eb636-139">-StartIPAddress</span></span>
<span data-ttu-id="eb636-140">Die Start-IP-Adresse der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="eb636-140">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="eb636-141">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="eb636-141">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="eb636-142">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="eb636-142">-SubscriptionId</span></span>
<span data-ttu-id="eb636-143">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="eb636-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="eb636-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eb636-144">-Confirm</span></span>
<span data-ttu-id="eb636-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eb636-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb636-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb636-146">-WhatIf</span></span>
<span data-ttu-id="eb636-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb636-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb636-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb636-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb636-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb636-149">CommonParameters</span></span>
<span data-ttu-id="eb636-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb636-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb636-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb636-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb636-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb636-152">INPUTS</span></span>

## <span data-ttu-id="eb636-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb636-153">OUTPUTS</span></span>

### <span data-ttu-id="eb636-154">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="eb636-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="eb636-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb636-155">NOTES</span></span>

<span data-ttu-id="eb636-156">Aliase</span><span class="sxs-lookup"><span data-stu-id="eb636-156">ALIASES</span></span>

## <span data-ttu-id="eb636-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb636-157">RELATED LINKS</span></span>

