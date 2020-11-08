---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
ms.openlocfilehash: 00da9023a7ed6607993af3faadccfbddbb784526
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009223"
---
# <span data-ttu-id="3bff2-101">New-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3bff2-101">New-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="3bff2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3bff2-102">SYNOPSIS</span></span>
<span data-ttu-id="3bff2-103">Erstellt eine neue Firewall-Regel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="3bff2-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="3bff2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bff2-104">SYNTAX</span></span>

### <span data-ttu-id="3bff2-105">Createexpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="3bff2-105">CreateExpanded (Default)</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3bff2-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="3bff2-106">AllowAll</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3bff2-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="3bff2-107">ClientIPAddress</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3bff2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3bff2-108">DESCRIPTION</span></span>
<span data-ttu-id="3bff2-109">Erstellt eine neue Firewall-Regel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="3bff2-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="3bff2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3bff2-110">EXAMPLES</span></span>

### <span data-ttu-id="3bff2-111">Beispiel 1: Erstellen einer Firewallregel unter einem MariaDB</span><span class="sxs-lookup"><span data-stu-id="3bff2-111">Example 1: Create a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -Name firewall-101 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -EndIPAddress 0.0.2.255 -StartIPAddress 0.0.2.1

Name         StartIPAddress EndIPAddress
----         -------------- ------------
firewall-101 0.0.2.1        0.0.2.255
```

<span data-ttu-id="3bff2-112">Dieser Befehl erstellt eine Firewallregel unter einem MariaDB.</span><span class="sxs-lookup"><span data-stu-id="3bff2-112">This command creates a firewall rule under a MariaDB.</span></span>

### <span data-ttu-id="3bff2-113">Beispiel 2: Erstellen einer neuen MariaDB-Firewallregel mithilfe von-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="3bff2-113">Example 2: Create a new MariaDB Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="3bff2-114">Mit diesen Cmdlets wird eine MariaDB-Firewall-Regel mit-ClientIPAddress erstellt.</span><span class="sxs-lookup"><span data-stu-id="3bff2-114">This cmdlets create a MariaDB Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="3bff2-115">Beispiel 3: Erstellen einer neuen MariaDB-Firewallregel, um alle IPS zuzulassen</span><span class="sxs-lookup"><span data-stu-id="3bff2-115">Example 3: Create a new MariaDB Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="3bff2-116">Diese Cmdlets erstellen eine neue MariaDB-Firewallregel, damit alle IPS zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="3bff2-116">This cmdlets create a new MariaDB Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="3bff2-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bff2-117">PARAMETERS</span></span>

### <span data-ttu-id="3bff2-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="3bff2-118">-AllowAll</span></span>
<span data-ttu-id="3bff2-119">Präsentieren, damit alle IP-Adressen von 0.0.0.0 zu 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="3bff2-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="3bff2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3bff2-120">-AsJob</span></span>
<span data-ttu-id="3bff2-121">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="3bff2-121">Run the command as a job</span></span>

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

### <span data-ttu-id="3bff2-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="3bff2-122">-ClientIPAddress</span></span>
<span data-ttu-id="3bff2-123">Client hat eine einzelne IP-Adresse der Server Firewall-Regel angegeben.</span><span class="sxs-lookup"><span data-stu-id="3bff2-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="3bff2-124">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="3bff2-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="3bff2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bff2-125">-DefaultProfile</span></span>
<span data-ttu-id="3bff2-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3bff2-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bff2-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="3bff2-127">-EndIPAddress</span></span>
<span data-ttu-id="3bff2-128">Die End-IP-Adresse der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="3bff2-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="3bff2-129">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="3bff2-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="3bff2-130">-Name</span><span class="sxs-lookup"><span data-stu-id="3bff2-130">-Name</span></span>
<span data-ttu-id="3bff2-131">Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="3bff2-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="3bff2-132">Wenn keine Angabe erfolgt, ist der Standardwert undefined.</span><span class="sxs-lookup"><span data-stu-id="3bff2-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="3bff2-133">Wenn AllowAll vorhanden ist, lautet der Standardname AllowAll_yyyy-mm-dd_HH-mm-SS.</span><span class="sxs-lookup"><span data-stu-id="3bff2-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="3bff2-134">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3bff2-134">-NoWait</span></span>
<span data-ttu-id="3bff2-135">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="3bff2-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3bff2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bff2-136">-ResourceGroupName</span></span>
<span data-ttu-id="3bff2-137">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="3bff2-137">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3bff2-138">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="3bff2-138">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3bff2-139">-Servername</span><span class="sxs-lookup"><span data-stu-id="3bff2-139">-ServerName</span></span>
<span data-ttu-id="3bff2-140">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="3bff2-140">The name of the server.</span></span>

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

### <span data-ttu-id="3bff2-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="3bff2-141">-StartIPAddress</span></span>
<span data-ttu-id="3bff2-142">Die Start-IP-Adresse der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="3bff2-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="3bff2-143">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="3bff2-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="3bff2-144">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="3bff2-144">-SubscriptionId</span></span>
<span data-ttu-id="3bff2-145">Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3bff2-145">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="3bff2-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3bff2-146">-Confirm</span></span>
<span data-ttu-id="3bff2-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3bff2-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bff2-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bff2-148">-WhatIf</span></span>
<span data-ttu-id="3bff2-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3bff2-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bff2-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3bff2-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bff2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bff2-151">CommonParameters</span></span>
<span data-ttu-id="3bff2-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bff2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bff2-153">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bff2-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bff2-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3bff2-154">INPUTS</span></span>

## <span data-ttu-id="3bff2-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3bff2-155">OUTPUTS</span></span>

### <span data-ttu-id="3bff2-156">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3bff2-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="3bff2-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="3bff2-157">NOTES</span></span>

<span data-ttu-id="3bff2-158">Aliase</span><span class="sxs-lookup"><span data-stu-id="3bff2-158">ALIASES</span></span>

## <span data-ttu-id="3bff2-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3bff2-159">RELATED LINKS</span></span>

