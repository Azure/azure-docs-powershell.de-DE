---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
ms.openlocfilehash: 036628943afc8b2c5f07b30f2db14f27229364c7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180225"
---
# <span data-ttu-id="0d22c-101">New-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0d22c-101">New-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="0d22c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d22c-102">SYNOPSIS</span></span>
<span data-ttu-id="0d22c-103">Erstellt eine neue Firewall-Regel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="0d22c-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="0d22c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d22c-104">SYNTAX</span></span>

### <span data-ttu-id="0d22c-105">Createexpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="0d22c-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0d22c-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="0d22c-106">AllowAll</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0d22c-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="0d22c-107">ClientIPAddress</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0d22c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d22c-108">DESCRIPTION</span></span>
<span data-ttu-id="0d22c-109">Erstellt eine neue Firewall-Regel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="0d22c-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="0d22c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d22c-110">EXAMPLES</span></span>

### <span data-ttu-id="0d22c-111">Beispiel 1: Erstellen einer neuen MySQL-Server-Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="0d22c-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="0d22c-112">Mit diesen Cmdlets wird eine MySQL Server-Firewall-Regel erstellt.</span><span class="sxs-lookup"><span data-stu-id="0d22c-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="0d22c-113">Beispiel 2: Erstellen einer neuen MySQL-Firewallregel mithilfe von-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="0d22c-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="0d22c-114">Diese Cmdlets erstellen eine MySQL-Firewallregel mithilfe von-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="0d22c-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="0d22c-115">Beispiel 3: Erstellen einer neuen MySQL-Firewall-Regel, um alle IPS zuzulassen</span><span class="sxs-lookup"><span data-stu-id="0d22c-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="0d22c-116">Diese Cmdlets erstellen eine neue MySQL-Firewallregel, damit alle IPS zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="0d22c-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="0d22c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d22c-117">PARAMETERS</span></span>

### <span data-ttu-id="0d22c-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="0d22c-118">-AllowAll</span></span>
<span data-ttu-id="0d22c-119">Präsentieren, damit alle IP-Adressen von 0.0.0.0 zu 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="0d22c-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="0d22c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d22c-120">-AsJob</span></span>
<span data-ttu-id="0d22c-121">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="0d22c-121">Run the command as a job</span></span>

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

### <span data-ttu-id="0d22c-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="0d22c-122">-ClientIPAddress</span></span>
<span data-ttu-id="0d22c-123">Client hat eine einzelne IP-Adresse der Server Firewall-Regel angegeben.</span><span class="sxs-lookup"><span data-stu-id="0d22c-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="0d22c-124">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="0d22c-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0d22c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d22c-125">-DefaultProfile</span></span>
<span data-ttu-id="0d22c-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d22c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d22c-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="0d22c-127">-EndIPAddress</span></span>
<span data-ttu-id="0d22c-128">Die End-IP-Adresse der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="0d22c-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="0d22c-129">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="0d22c-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0d22c-130">-Name</span><span class="sxs-lookup"><span data-stu-id="0d22c-130">-Name</span></span>
<span data-ttu-id="0d22c-131">Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="0d22c-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="0d22c-132">Wenn keine Angabe erfolgt, ist der Standardwert undefined.</span><span class="sxs-lookup"><span data-stu-id="0d22c-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="0d22c-133">Wenn AllowAll vorhanden ist, lautet der Standardname AllowAll_yyyy-mm-dd_HH-mm-SS.</span><span class="sxs-lookup"><span data-stu-id="0d22c-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="0d22c-134">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0d22c-134">-NoWait</span></span>
<span data-ttu-id="0d22c-135">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="0d22c-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0d22c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d22c-136">-ResourceGroupName</span></span>
<span data-ttu-id="0d22c-137">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0d22c-137">The name of the resource group.</span></span>
<span data-ttu-id="0d22c-138">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="0d22c-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0d22c-139">-Servername</span><span class="sxs-lookup"><span data-stu-id="0d22c-139">-ServerName</span></span>
<span data-ttu-id="0d22c-140">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="0d22c-140">The name of the server.</span></span>

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

### <span data-ttu-id="0d22c-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="0d22c-141">-StartIPAddress</span></span>
<span data-ttu-id="0d22c-142">Die Start-IP-Adresse der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="0d22c-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="0d22c-143">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="0d22c-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0d22c-144">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="0d22c-144">-SubscriptionId</span></span>
<span data-ttu-id="0d22c-145">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="0d22c-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0d22c-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0d22c-146">-Confirm</span></span>
<span data-ttu-id="0d22c-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d22c-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d22c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d22c-148">-WhatIf</span></span>
<span data-ttu-id="0d22c-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d22c-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d22c-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d22c-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d22c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d22c-151">CommonParameters</span></span>
<span data-ttu-id="0d22c-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d22c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d22c-153">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d22c-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d22c-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d22c-154">INPUTS</span></span>

## <span data-ttu-id="0d22c-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d22c-155">OUTPUTS</span></span>

### <span data-ttu-id="0d22c-156">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0d22c-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="0d22c-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d22c-157">NOTES</span></span>

<span data-ttu-id="0d22c-158">Aliase</span><span class="sxs-lookup"><span data-stu-id="0d22c-158">ALIASES</span></span>

## <span data-ttu-id="0d22c-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d22c-159">RELATED LINKS</span></span>

