---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 0579220e372a937dd25d5956735a321e84523f69
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292877"
---
# <span data-ttu-id="bc462-101">Get-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc462-101">Get-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="bc462-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc462-102">SYNOPSIS</span></span>
<span data-ttu-id="bc462-103">Ruft Informationen zu einer Serverkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="bc462-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="bc462-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc462-104">SYNTAX</span></span>

### <span data-ttu-id="bc462-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="bc462-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bc462-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="bc462-106">Get</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bc462-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bc462-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc462-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc462-108">DESCRIPTION</span></span>
<span data-ttu-id="bc462-109">Ruft Informationen zu einer Serverkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="bc462-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="bc462-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bc462-110">EXAMPLES</span></span>

### <span data-ttu-id="bc462-111">Beispiel 1: Auflisten aller Konfigurationen im angegebenen Server "MySql"</span><span class="sxs-lookup"><span data-stu-id="bc462-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
archive        OFF    OFF           system-default ON, OFF      Enumeration
...
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="bc462-112">Dieses Cmdlet listet alle Konfigurationen im angegebenen Server "MySql" auf.</span><span class="sxs-lookup"><span data-stu-id="bc462-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="bc462-113">Beispiel 2: Angegebene MeineSql-Konfiguration nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="bc462-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="bc462-114">Dieses Cmdlet wird als Name für die Konfiguration von MySql angegeben.</span><span class="sxs-lookup"><span data-stu-id="bc462-114">This cmdlet gets specified MySql configuration by name.</span></span>

### <span data-ttu-id="bc462-115">Beispiel 3: Auflisten der Konfiguration nach Identität</span><span class="sxs-lookup"><span data-stu-id="bc462-115">Example 3: List configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="bc462-116">Dieses Cmdlet wird als MySql-Konfiguration nach Identität angegeben.</span><span class="sxs-lookup"><span data-stu-id="bc462-116">This cmdlet gets specified MySql configuration by identity.</span></span>

## <span data-ttu-id="bc462-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc462-117">PARAMETERS</span></span>

### <span data-ttu-id="bc462-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc462-118">-DefaultProfile</span></span>
<span data-ttu-id="bc462-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bc462-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc462-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc462-120">-InputObject</span></span>
<span data-ttu-id="bc462-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="bc462-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bc462-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bc462-122">-Name</span></span>
<span data-ttu-id="bc462-123">Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="bc462-123">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc462-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc462-124">-ResourceGroupName</span></span>
<span data-ttu-id="bc462-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bc462-125">The name of the resource group.</span></span>
<span data-ttu-id="bc462-126">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="bc462-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bc462-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bc462-127">-ServerName</span></span>
<span data-ttu-id="bc462-128">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="bc462-128">The name of the server.</span></span>

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

### <span data-ttu-id="bc462-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc462-129">-SubscriptionId</span></span>
<span data-ttu-id="bc462-130">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="bc462-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bc462-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc462-131">CommonParameters</span></span>
<span data-ttu-id="bc462-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc462-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc462-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc462-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc462-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bc462-134">INPUTS</span></span>

### <span data-ttu-id="bc462-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="bc462-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="bc462-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bc462-136">OUTPUTS</span></span>

### <span data-ttu-id="bc462-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="bc462-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="bc462-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bc462-138">NOTES</span></span>

<span data-ttu-id="bc462-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="bc462-139">ALIASES</span></span>

<span data-ttu-id="bc462-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="bc462-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bc462-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bc462-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bc462-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bc462-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bc462-143">INPUTOBJECT <IMySqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="bc462-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bc462-144">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="bc462-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="bc462-145">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="bc462-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="bc462-146">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="bc462-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="bc462-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="bc462-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bc462-148">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="bc462-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="bc462-149">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="bc462-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="bc462-150">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bc462-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bc462-151">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="bc462-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="bc462-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="bc462-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="bc462-153">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="bc462-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="bc462-154">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="bc462-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bc462-155">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="bc462-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="bc462-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bc462-156">RELATED LINKS</span></span>

