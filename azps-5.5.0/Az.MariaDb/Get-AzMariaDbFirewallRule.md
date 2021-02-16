---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 2b2f52d8dc4f9e31a86b666b7ee81981fa6bd18c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157484"
---
# <span data-ttu-id="f4831-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f4831-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="f4831-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4831-102">SYNOPSIS</span></span>
<span data-ttu-id="f4831-103">Ruft Informationen zu einer Serverfirewallregel ab.</span><span class="sxs-lookup"><span data-stu-id="f4831-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="f4831-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4831-104">SYNTAX</span></span>

### <span data-ttu-id="f4831-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4831-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f4831-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="f4831-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f4831-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f4831-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f4831-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4831-108">DESCRIPTION</span></span>
<span data-ttu-id="f4831-109">Ruft Informationen zu einer Serverfirewallregel ab.</span><span class="sxs-lookup"><span data-stu-id="f4831-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="f4831-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4831-110">EXAMPLES</span></span>

### <span data-ttu-id="f4831-111">Beispiel 1: Auflisten aller Firewallregeln unter einer MariaDB</span><span class="sxs-lookup"><span data-stu-id="f4831-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="f4831-112">Dieser Befehl listet alle "Girewall"-Regeln unter einer MariaDB auf.</span><span class="sxs-lookup"><span data-stu-id="f4831-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="f4831-113">Beispiel 2: Erhalten einer Firewallregel unter einer MariaDB</span><span class="sxs-lookup"><span data-stu-id="f4831-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="f4831-114">Dieser Befehl ruft eine Firewallregel unter einer MariaDB ab.</span><span class="sxs-lookup"><span data-stu-id="f4831-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="f4831-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4831-115">PARAMETERS</span></span>

### <span data-ttu-id="f4831-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4831-116">-DefaultProfile</span></span>
<span data-ttu-id="f4831-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4831-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4831-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4831-118">-InputObject</span></span>
<span data-ttu-id="f4831-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f4831-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4831-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f4831-120">-Name</span></span>
<span data-ttu-id="f4831-121">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="f4831-121">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4831-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4831-122">-ResourceGroupName</span></span>
<span data-ttu-id="f4831-123">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="f4831-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f4831-124">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="f4831-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4831-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f4831-125">-ServerName</span></span>
<span data-ttu-id="f4831-126">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="f4831-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4831-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4831-127">-SubscriptionId</span></span>
<span data-ttu-id="f4831-128">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f4831-128">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4831-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4831-129">CommonParameters</span></span>
<span data-ttu-id="f4831-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4831-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4831-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4831-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4831-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4831-132">INPUTS</span></span>

### <span data-ttu-id="f4831-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="f4831-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="f4831-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4831-134">OUTPUTS</span></span>

### <span data-ttu-id="f4831-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f4831-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="f4831-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f4831-136">NOTES</span></span>

<span data-ttu-id="f4831-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f4831-137">ALIASES</span></span>

<span data-ttu-id="f4831-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="f4831-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f4831-139">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f4831-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f4831-140">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f4831-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f4831-141">INPUTOBJECT <IMariaDbIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="f4831-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f4831-142">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f4831-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f4831-143">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f4831-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f4831-144">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="f4831-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f4831-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="f4831-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f4831-146">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="f4831-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f4831-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="f4831-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f4831-148">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="f4831-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f4831-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="f4831-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f4831-150">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="f4831-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f4831-151">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f4831-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="f4831-152">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f4831-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f4831-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f4831-153">RELATED LINKS</span></span>

