---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/new-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
ms.openlocfilehash: c511e605af327f5ac1b913f133cf725baeee894c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927928"
---
# <span data-ttu-id="de63e-101">New-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="de63e-101">New-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="de63e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de63e-102">SYNOPSIS</span></span>
<span data-ttu-id="de63e-103">Erstellt eine neue Firewallregel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="de63e-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="de63e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de63e-104">SYNTAX</span></span>

### <span data-ttu-id="de63e-105">CreateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="de63e-105">CreateExpanded (Default)</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="de63e-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="de63e-106">AllowAll</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="de63e-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="de63e-107">ClientIPAddress</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="de63e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de63e-108">DESCRIPTION</span></span>
<span data-ttu-id="de63e-109">Erstellt eine neue Firewallregel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="de63e-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="de63e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="de63e-110">EXAMPLES</span></span>

### <span data-ttu-id="de63e-111">Beispiel 1: Erstellen einer Firewallregel unter einer MariaDB</span><span class="sxs-lookup"><span data-stu-id="de63e-111">Example 1: Create a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -Name firewall-101 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -EndIPAddress 0.0.2.255 -StartIPAddress 0.0.2.1

Name         StartIPAddress EndIPAddress
----         -------------- ------------
firewall-101 0.0.2.1        0.0.2.255
```

<span data-ttu-id="de63e-112">Mit diesem Befehl wird eine Firewallregel unter einer MariaDB erstellt.</span><span class="sxs-lookup"><span data-stu-id="de63e-112">This command creates a firewall rule under a MariaDB.</span></span>

### <span data-ttu-id="de63e-113">Beispiel 2: Erstellen Einer neuen MariaDB-Firewallregel mit -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="de63e-113">Example 2: Create a new MariaDB Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="de63e-114">Diese Cmdlets erstellen eine MariaDB-Firewallregel mit -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="de63e-114">This cmdlets create a MariaDB Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="de63e-115">Beispiel 3: Erstellen einer neuen MariaDB-Firewallregel zum Zulassen aller IPs</span><span class="sxs-lookup"><span data-stu-id="de63e-115">Example 3: Create a new MariaDB Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="de63e-116">Diese Cmdlets erstellen eine neue MariaDB-Firewallregel, um alle IPs zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="de63e-116">This cmdlets create a new MariaDB Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="de63e-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="de63e-117">PARAMETERS</span></span>

### <span data-ttu-id="de63e-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="de63e-118">-AllowAll</span></span>
<span data-ttu-id="de63e-119">Präsentieren, um alle Bereichs-IPs von 0,0,0,0 bis 255,255.255.255 zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="de63e-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="de63e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de63e-120">-AsJob</span></span>
<span data-ttu-id="de63e-121">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="de63e-121">Run the command as a job</span></span>

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

### <span data-ttu-id="de63e-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="de63e-122">-ClientIPAddress</span></span>
<span data-ttu-id="de63e-123">Client hat einzelne IP der Serverfirewallregel angegeben.</span><span class="sxs-lookup"><span data-stu-id="de63e-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="de63e-124">Muss das IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="de63e-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="de63e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de63e-125">-DefaultProfile</span></span>
<span data-ttu-id="de63e-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de63e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de63e-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="de63e-127">-EndIPAddress</span></span>
<span data-ttu-id="de63e-128">Die End-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="de63e-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="de63e-129">Muss das IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="de63e-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="de63e-130">-Name</span><span class="sxs-lookup"><span data-stu-id="de63e-130">-Name</span></span>
<span data-ttu-id="de63e-131">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="de63e-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="de63e-132">Wenn nicht angegeben, ist die Standardeinstellung nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="de63e-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="de63e-133">Wenn AllowAll vorhanden ist, ist der Standardname AllowAll_yyyy-MM-dd_HH-mm-ss.</span><span class="sxs-lookup"><span data-stu-id="de63e-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="de63e-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="de63e-134">-NoWait</span></span>
<span data-ttu-id="de63e-135">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="de63e-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="de63e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de63e-136">-ResourceGroupName</span></span>
<span data-ttu-id="de63e-137">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="de63e-137">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="de63e-138">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="de63e-138">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="de63e-139">-Servername</span><span class="sxs-lookup"><span data-stu-id="de63e-139">-ServerName</span></span>
<span data-ttu-id="de63e-140">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="de63e-140">The name of the server.</span></span>

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

### <span data-ttu-id="de63e-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="de63e-141">-StartIPAddress</span></span>
<span data-ttu-id="de63e-142">Die Start-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="de63e-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="de63e-143">Muss das IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="de63e-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="de63e-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de63e-144">-SubscriptionId</span></span>
<span data-ttu-id="de63e-145">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="de63e-145">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="de63e-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="de63e-146">-Confirm</span></span>
<span data-ttu-id="de63e-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="de63e-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de63e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de63e-148">-WhatIf</span></span>
<span data-ttu-id="de63e-149">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="de63e-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de63e-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de63e-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de63e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de63e-151">CommonParameters</span></span>
<span data-ttu-id="de63e-152">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de63e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de63e-153">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de63e-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de63e-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="de63e-154">INPUTS</span></span>

## <span data-ttu-id="de63e-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="de63e-155">OUTPUTS</span></span>

### <span data-ttu-id="de63e-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="de63e-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="de63e-157">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="de63e-157">NOTES</span></span>

<span data-ttu-id="de63e-158">ALIASE</span><span class="sxs-lookup"><span data-stu-id="de63e-158">ALIASES</span></span>

## <span data-ttu-id="de63e-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="de63e-159">RELATED LINKS</span></span>

