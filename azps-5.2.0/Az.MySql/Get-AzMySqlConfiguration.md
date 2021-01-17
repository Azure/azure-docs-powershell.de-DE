---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: fae355df0b33fa648be1d9043f140123cf9d79a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359020"
---
# <span data-ttu-id="0ce95-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ce95-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="0ce95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ce95-102">SYNOPSIS</span></span>
<span data-ttu-id="0ce95-103">Ruft Informationen zu einer Serverkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="0ce95-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="0ce95-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ce95-104">SYNTAX</span></span>

### <span data-ttu-id="0ce95-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ce95-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0ce95-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="0ce95-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0ce95-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0ce95-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0ce95-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ce95-108">DESCRIPTION</span></span>
<span data-ttu-id="0ce95-109">Ruft Informationen zu einer Serverkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="0ce95-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="0ce95-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0ce95-110">EXAMPLES</span></span>

### <span data-ttu-id="0ce95-111">Beispiel 1: Auflisten aller Konfigurationen im angegebenen Server "MySql"</span><span class="sxs-lookup"><span data-stu-id="0ce95-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name                                     Type
----                                     ----
audit_log_enabled                        Microsoft.DBforMySQL/servers/configurations
audit_log_events                         Microsoft.DBforMySQL/servers/configurations
audit_log_exclude_users                  Microsoft.DBforMySQL/servers/configurations
audit_log_include_users                  Microsoft.DBforMySQL/servers/configurations
...
transaction_prealloc_size                Microsoft.DBforMySQL/servers/configurations
tx_isolation                             Microsoft.DBforMySQL/servers/configurations
updatable_views_with_limit               Microsoft.DBforMySQL/servers/configurations
wait_timeout                             Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="0ce95-112">Dieses Cmdlet listet alle Konfigurationen im angegebenen Server "MySql" auf.</span><span class="sxs-lookup"><span data-stu-id="0ce95-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="0ce95-113">Beispiel 2: Angegebene MeineSql-Konfiguration nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="0ce95-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="0ce95-114">Dieses Cmdlet wird als Name für die Konfiguration von MySql angegeben.</span><span class="sxs-lookup"><span data-stu-id="0ce95-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="0ce95-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ce95-115">PARAMETERS</span></span>

### <span data-ttu-id="0ce95-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ce95-116">-DefaultProfile</span></span>
<span data-ttu-id="0ce95-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ce95-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ce95-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ce95-118">-InputObject</span></span>
<span data-ttu-id="0ce95-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0ce95-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0ce95-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0ce95-120">-Name</span></span>
<span data-ttu-id="0ce95-121">Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0ce95-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="0ce95-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ce95-122">-ResourceGroupName</span></span>
<span data-ttu-id="0ce95-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0ce95-123">The name of the resource group.</span></span>
<span data-ttu-id="0ce95-124">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="0ce95-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0ce95-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0ce95-125">-ServerName</span></span>
<span data-ttu-id="0ce95-126">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="0ce95-126">The name of the server.</span></span>

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

### <span data-ttu-id="0ce95-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0ce95-127">-SubscriptionId</span></span>
<span data-ttu-id="0ce95-128">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="0ce95-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0ce95-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce95-129">CommonParameters</span></span>
<span data-ttu-id="0ce95-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ce95-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce95-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ce95-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce95-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0ce95-132">INPUTS</span></span>

### <span data-ttu-id="0ce95-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0ce95-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="0ce95-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0ce95-134">OUTPUTS</span></span>

### <span data-ttu-id="0ce95-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ce95-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="0ce95-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0ce95-136">NOTES</span></span>

<span data-ttu-id="0ce95-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="0ce95-137">ALIASES</span></span>

<span data-ttu-id="0ce95-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="0ce95-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0ce95-139">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0ce95-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0ce95-140">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0ce95-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0ce95-141">INPUTOBJECT <IMySqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="0ce95-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0ce95-142">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0ce95-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0ce95-143">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0ce95-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0ce95-144">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="0ce95-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0ce95-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="0ce95-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0ce95-146">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="0ce95-146">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="0ce95-147">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="0ce95-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0ce95-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0ce95-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0ce95-149">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="0ce95-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="0ce95-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="0ce95-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0ce95-151">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="0ce95-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0ce95-152">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="0ce95-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0ce95-153">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0ce95-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0ce95-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0ce95-154">RELATED LINKS</span></span>

