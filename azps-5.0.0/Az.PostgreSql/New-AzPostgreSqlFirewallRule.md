---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: bafd0e20530198da87c1fa3ece36905e73307a42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177776"
---
# <span data-ttu-id="5e209-101">New-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5e209-101">New-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="5e209-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e209-102">SYNOPSIS</span></span>
<span data-ttu-id="5e209-103">Erstellt eine neue Firewall-Regel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="5e209-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="5e209-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e209-104">SYNTAX</span></span>

### <span data-ttu-id="5e209-105">Createexpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e209-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5e209-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="5e209-106">AllowAll</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5e209-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="5e209-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5e209-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e209-108">DESCRIPTION</span></span>
<span data-ttu-id="5e209-109">Erstellt eine neue Firewall-Regel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="5e209-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="5e209-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e209-110">EXAMPLES</span></span>

### <span data-ttu-id="5e209-111">Beispiel 1: Erstellen einer neuen PostgreSQL-Server Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="5e209-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="5e209-112">Diese Cmdlets erstellen eine Firewall-Regel für den PostgreSQL-Server.</span><span class="sxs-lookup"><span data-stu-id="5e209-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="5e209-113">Beispiel 2: Erstellen einer neuen PostgreSQL-Firewallregel mithilfe von-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="5e209-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="5e209-114">Diese Cmdlets erstellen eine PostgreSQL-Firewallregel mithilfe von-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="5e209-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="5e209-115">Beispiel 3: Erstellen einer neuen PostgreSQL-Firewall-Regel, um alle IPS zuzulassen</span><span class="sxs-lookup"><span data-stu-id="5e209-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="5e209-116">Diese Cmdlets erstellen eine neue PostgreSQL-Firewallregel, damit alle IPS zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="5e209-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="5e209-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e209-117">PARAMETERS</span></span>

### <span data-ttu-id="5e209-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="5e209-118">-AllowAll</span></span>
<span data-ttu-id="5e209-119">Präsentieren, damit alle IP-Adressen von 0.0.0.0 zu 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="5e209-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="5e209-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e209-120">-AsJob</span></span>
<span data-ttu-id="5e209-121">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="5e209-121">Run the command as a job</span></span>

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

### <span data-ttu-id="5e209-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="5e209-122">-ClientIPAddress</span></span>
<span data-ttu-id="5e209-123">Client hat eine einzelne IP-Adresse der Server Firewall-Regel angegeben.</span><span class="sxs-lookup"><span data-stu-id="5e209-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="5e209-124">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="5e209-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="5e209-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e209-125">-DefaultProfile</span></span>
<span data-ttu-id="5e209-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e209-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e209-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="5e209-127">-EndIPAddress</span></span>
<span data-ttu-id="5e209-128">Die End-IP-Adresse der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="5e209-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="5e209-129">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="5e209-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="5e209-130">-Name</span><span class="sxs-lookup"><span data-stu-id="5e209-130">-Name</span></span>
<span data-ttu-id="5e209-131">Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="5e209-131">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="5e209-132">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5e209-132">-NoWait</span></span>
<span data-ttu-id="5e209-133">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="5e209-133">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5e209-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e209-134">-ResourceGroupName</span></span>
<span data-ttu-id="5e209-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e209-135">The name of the resource group.</span></span>
<span data-ttu-id="5e209-136">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="5e209-136">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5e209-137">-Servername</span><span class="sxs-lookup"><span data-stu-id="5e209-137">-ServerName</span></span>
<span data-ttu-id="5e209-138">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="5e209-138">The name of the server.</span></span>

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

### <span data-ttu-id="5e209-139">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="5e209-139">-StartIPAddress</span></span>
<span data-ttu-id="5e209-140">Die Start-IP-Adresse der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="5e209-140">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="5e209-141">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="5e209-141">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="5e209-142">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5e209-142">-SubscriptionId</span></span>
<span data-ttu-id="5e209-143">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="5e209-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5e209-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e209-144">-Confirm</span></span>
<span data-ttu-id="5e209-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e209-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e209-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e209-146">-WhatIf</span></span>
<span data-ttu-id="5e209-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e209-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e209-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e209-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e209-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e209-149">CommonParameters</span></span>
<span data-ttu-id="5e209-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e209-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e209-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e209-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e209-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e209-152">INPUTS</span></span>

## <span data-ttu-id="5e209-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e209-153">OUTPUTS</span></span>

### <span data-ttu-id="5e209-154">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5e209-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="5e209-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e209-155">NOTES</span></span>

<span data-ttu-id="5e209-156">Aliase</span><span class="sxs-lookup"><span data-stu-id="5e209-156">ALIASES</span></span>

## <span data-ttu-id="5e209-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e209-157">RELATED LINKS</span></span>

