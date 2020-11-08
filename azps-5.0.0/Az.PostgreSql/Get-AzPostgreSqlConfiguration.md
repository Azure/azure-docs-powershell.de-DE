---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
ms.openlocfilehash: 7fdc31b4a64733ce686b38ccfb176f754f3f84ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178135"
---
# <span data-ttu-id="a12ed-101">Get-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a12ed-101">Get-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="a12ed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a12ed-102">SYNOPSIS</span></span>
<span data-ttu-id="a12ed-103">Ruft Informationen zu einer Serverkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="a12ed-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="a12ed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a12ed-104">SYNTAX</span></span>

### <span data-ttu-id="a12ed-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="a12ed-105">List (Default)</span></span>
```
Get-AzPostgreSqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a12ed-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="a12ed-106">Get</span></span>
```
Get-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a12ed-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a12ed-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a12ed-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a12ed-108">DESCRIPTION</span></span>
<span data-ttu-id="a12ed-109">Ruft Informationen zu einer Serverkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="a12ed-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="a12ed-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a12ed-110">EXAMPLES</span></span>

### <span data-ttu-id="a12ed-111">Beispiel 1: Auflisten aller Konfigurationen in PostgreSQL Server</span><span class="sxs-lookup"><span data-stu-id="a12ed-111">Example 1: List all configurations in PostgreSql server</span></span>
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

<span data-ttu-id="a12ed-112">Dieses Cmdlet listet alle Konfigurationen auf dem angegebenen PostgreSQL-Server auf.</span><span class="sxs-lookup"><span data-stu-id="a12ed-112">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

### <span data-ttu-id="a12ed-113">Beispiel 2: Abrufen der angegebenen PostgreSQL-Konfiguration nach Name</span><span class="sxs-lookup"><span data-stu-id="a12ed-113">Example 2: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -Name timezone -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name     Value
----     -----
timezone UTC
```

<span data-ttu-id="a12ed-114">Dieses Cmdlet erhält die angegebene PostgreSQL-Konfiguration nach Namen.</span><span class="sxs-lookup"><span data-stu-id="a12ed-114">This cmdlet gets specified PostgreSql configuration by name.</span></span>

## <span data-ttu-id="a12ed-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a12ed-115">PARAMETERS</span></span>

### <span data-ttu-id="a12ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a12ed-116">-DefaultProfile</span></span>
<span data-ttu-id="a12ed-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a12ed-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a12ed-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a12ed-118">-InputObject</span></span>
<span data-ttu-id="a12ed-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a12ed-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a12ed-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a12ed-120">-Name</span></span>
<span data-ttu-id="a12ed-121">Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="a12ed-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="a12ed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a12ed-122">-ResourceGroupName</span></span>
<span data-ttu-id="a12ed-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a12ed-123">The name of the resource group.</span></span>
<span data-ttu-id="a12ed-124">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="a12ed-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a12ed-125">-Servername</span><span class="sxs-lookup"><span data-stu-id="a12ed-125">-ServerName</span></span>
<span data-ttu-id="a12ed-126">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="a12ed-126">The name of the server.</span></span>

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

### <span data-ttu-id="a12ed-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a12ed-127">-SubscriptionId</span></span>
<span data-ttu-id="a12ed-128">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a12ed-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a12ed-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a12ed-129">CommonParameters</span></span>
<span data-ttu-id="a12ed-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a12ed-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a12ed-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a12ed-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a12ed-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a12ed-132">INPUTS</span></span>

### <span data-ttu-id="a12ed-133">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="a12ed-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="a12ed-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a12ed-134">OUTPUTS</span></span>

### <span data-ttu-id="a12ed-135">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="a12ed-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="a12ed-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a12ed-136">NOTES</span></span>

<span data-ttu-id="a12ed-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="a12ed-137">ALIASES</span></span>

<span data-ttu-id="a12ed-138">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a12ed-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a12ed-139">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a12ed-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a12ed-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="a12ed-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a12ed-141">Inputobject <IPostgreSqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="a12ed-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a12ed-142">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="a12ed-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a12ed-143">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a12ed-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a12ed-144">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="a12ed-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a12ed-145">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="a12ed-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a12ed-146">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="a12ed-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a12ed-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a12ed-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a12ed-148">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="a12ed-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="a12ed-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="a12ed-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a12ed-150">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="a12ed-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a12ed-151">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a12ed-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a12ed-152">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a12ed-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a12ed-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a12ed-153">RELATED LINKS</span></span>

