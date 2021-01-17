---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
ms.openlocfilehash: 7fdc31b4a64733ce686b38ccfb176f754f3f84ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378508"
---
# <span data-ttu-id="0de72-101">Get-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="0de72-101">Get-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="0de72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0de72-102">SYNOPSIS</span></span>
<span data-ttu-id="0de72-103">Ruft Informationen zu einer Serverkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="0de72-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="0de72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0de72-104">SYNTAX</span></span>

### <span data-ttu-id="0de72-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="0de72-105">List (Default)</span></span>
```
Get-AzPostgreSqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0de72-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="0de72-106">Get</span></span>
```
Get-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0de72-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0de72-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0de72-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0de72-108">DESCRIPTION</span></span>
<span data-ttu-id="0de72-109">Ruft Informationen zu einer Serverkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="0de72-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="0de72-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0de72-110">EXAMPLES</span></span>

### <span data-ttu-id="0de72-111">Beispiel 1: Auflisten aller Konfigurationen in PostgreSql Server</span><span class="sxs-lookup"><span data-stu-id="0de72-111">Example 1: List all configurations in PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                                  Value
----                                  -----
array_nulls                           on
backslash_quote                       safe_encoding
bytea_output                          hex
check_function_bodies                 on
client_encoding                       sql_ascii
...
azure.replication_support             REPLICA
max_wal_senders                       10
max_replication_slots                 10
hot_standby_feedback                  off
logging_collector                     on
```

<span data-ttu-id="0de72-112">Dieses Cmdlet listet alle Konfigurationen im angegebenen Server "PostgreSql" auf.</span><span class="sxs-lookup"><span data-stu-id="0de72-112">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

### <span data-ttu-id="0de72-113">Beispiel 2: Angegebene Konfiguration von PostgreSql nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="0de72-113">Example 2: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -Name timezone -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name     Value
----     -----
timezone UTC
```

<span data-ttu-id="0de72-114">Dieses Cmdlet wird nach Name als "PostgreSql-Konfiguration" angegeben.</span><span class="sxs-lookup"><span data-stu-id="0de72-114">This cmdlet gets specified PostgreSql configuration by name.</span></span>

## <span data-ttu-id="0de72-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0de72-115">PARAMETERS</span></span>

### <span data-ttu-id="0de72-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0de72-116">-DefaultProfile</span></span>
<span data-ttu-id="0de72-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0de72-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0de72-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0de72-118">-InputObject</span></span>
<span data-ttu-id="0de72-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0de72-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0de72-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0de72-120">-Name</span></span>
<span data-ttu-id="0de72-121">Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0de72-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="0de72-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0de72-122">-ResourceGroupName</span></span>
<span data-ttu-id="0de72-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0de72-123">The name of the resource group.</span></span>
<span data-ttu-id="0de72-124">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="0de72-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0de72-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0de72-125">-ServerName</span></span>
<span data-ttu-id="0de72-126">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="0de72-126">The name of the server.</span></span>

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

### <span data-ttu-id="0de72-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0de72-127">-SubscriptionId</span></span>
<span data-ttu-id="0de72-128">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="0de72-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0de72-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0de72-129">CommonParameters</span></span>
<span data-ttu-id="0de72-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0de72-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0de72-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0de72-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0de72-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0de72-132">INPUTS</span></span>

### <span data-ttu-id="0de72-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0de72-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="0de72-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0de72-134">OUTPUTS</span></span>

### <span data-ttu-id="0de72-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="0de72-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="0de72-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0de72-136">NOTES</span></span>

<span data-ttu-id="0de72-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="0de72-137">ALIASES</span></span>

<span data-ttu-id="0de72-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="0de72-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0de72-139">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0de72-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0de72-140">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0de72-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0de72-141">INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="0de72-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0de72-142">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0de72-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0de72-143">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0de72-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0de72-144">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="0de72-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0de72-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="0de72-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0de72-146">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="0de72-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0de72-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0de72-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0de72-148">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="0de72-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="0de72-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="0de72-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0de72-150">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="0de72-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0de72-151">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="0de72-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0de72-152">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0de72-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0de72-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0de72-153">RELATED LINKS</span></span>

