---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
ms.openlocfilehash: 7991f63e9deb6dcbcf3366a28a8c2159872c9da0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938611"
---
# <span data-ttu-id="13297-101">Get-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="13297-101">Get-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="13297-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13297-102">SYNOPSIS</span></span>
<span data-ttu-id="13297-103">Ruft Informationen zu einer Serverfirewallregel ab.</span><span class="sxs-lookup"><span data-stu-id="13297-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="13297-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13297-104">SYNTAX</span></span>

### <span data-ttu-id="13297-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="13297-105">List (Default)</span></span>
```
Get-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="13297-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="13297-106">Get</span></span>
```
Get-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="13297-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="13297-107">GetViaIdentity</span></span>
```
Get-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="13297-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13297-108">DESCRIPTION</span></span>
<span data-ttu-id="13297-109">Ruft Informationen zu einer Serverfirewallregel ab.</span><span class="sxs-lookup"><span data-stu-id="13297-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="13297-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="13297-110">EXAMPLES</span></span>

### <span data-ttu-id="13297-111">Beispiel 1: Listet alle Firewallregeln im angegebenen MySql-Server auf.</span><span class="sxs-lookup"><span data-stu-id="13297-111">Example 1: Lists all the Firewall Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="13297-112">In diesem Cmdlet werden alle Firewallregeln auf dem angegebenen MySql-Server aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="13297-112">This cmdlet lists all the Firewall Rule in specified MySql server.</span></span>

### <span data-ttu-id="13297-113">Beispiel 2: Firewallregel nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="13297-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="13297-114">Dieses Cmdlet ruft die Firewallregel nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="13297-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="13297-115">Beispiel 3: Firewallregel nach Identität erhalten</span><span class="sxs-lookup"><span data-stu-id="13297-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Get-AzMySqlFirewallRule -InputObject $ID

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="13297-116">Dieses Cmdlet ruft die Firewallregel nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="13297-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="13297-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="13297-117">PARAMETERS</span></span>

### <span data-ttu-id="13297-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13297-118">-DefaultProfile</span></span>
<span data-ttu-id="13297-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13297-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13297-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13297-120">-InputObject</span></span>
<span data-ttu-id="13297-121">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="13297-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13297-122">-Name</span><span class="sxs-lookup"><span data-stu-id="13297-122">-Name</span></span>
<span data-ttu-id="13297-123">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="13297-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="13297-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13297-124">-ResourceGroupName</span></span>
<span data-ttu-id="13297-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="13297-125">The name of the resource group.</span></span>
<span data-ttu-id="13297-126">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="13297-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="13297-127">-Servername</span><span class="sxs-lookup"><span data-stu-id="13297-127">-ServerName</span></span>
<span data-ttu-id="13297-128">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="13297-128">The name of the server.</span></span>

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

### <span data-ttu-id="13297-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13297-129">-SubscriptionId</span></span>
<span data-ttu-id="13297-130">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="13297-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="13297-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13297-131">CommonParameters</span></span>
<span data-ttu-id="13297-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13297-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13297-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13297-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13297-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="13297-134">INPUTS</span></span>

### <span data-ttu-id="13297-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="13297-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="13297-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="13297-136">OUTPUTS</span></span>

### <span data-ttu-id="13297-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="13297-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="13297-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="13297-138">NOTES</span></span>

<span data-ttu-id="13297-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="13297-139">ALIASES</span></span>

<span data-ttu-id="13297-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="13297-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="13297-141">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="13297-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="13297-142">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="13297-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="13297-143">INPUTOBJECT <IMySqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="13297-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="13297-144">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="13297-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="13297-145">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="13297-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="13297-146">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="13297-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="13297-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="13297-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="13297-148">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="13297-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="13297-149">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="13297-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="13297-150">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="13297-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="13297-151">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="13297-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="13297-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="13297-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="13297-153">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="13297-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="13297-154">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="13297-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="13297-155">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="13297-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="13297-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="13297-156">RELATED LINKS</span></span>

