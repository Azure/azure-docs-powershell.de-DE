---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: b92390969c4650d60d5c4a6954520fbbf3f26c71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302068"
---
# <span data-ttu-id="d240d-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d240d-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="d240d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d240d-102">SYNOPSIS</span></span>
<span data-ttu-id="d240d-103">Ruft Informationen zu einer Serverkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="d240d-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="d240d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d240d-104">SYNTAX</span></span>

### <span data-ttu-id="d240d-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="d240d-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d240d-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="d240d-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d240d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d240d-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d240d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d240d-108">DESCRIPTION</span></span>
<span data-ttu-id="d240d-109">Ruft Informationen zu einer Serverkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="d240d-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="d240d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d240d-110">EXAMPLES</span></span>

### <span data-ttu-id="d240d-111">Beispiel 1: Auflisten aller Konfigurationen im angegebenen MySQL-Server</span><span class="sxs-lookup"><span data-stu-id="d240d-111">Example 1: List all configurations in specified MySql server</span></span>
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

<span data-ttu-id="d240d-112">Dieses Cmdlet listet alle Konfigurationen im angegebenen MySQL-Server auf.</span><span class="sxs-lookup"><span data-stu-id="d240d-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="d240d-113">Beispiel 2: Abrufen der angegebenen MySQL-Konfiguration nach Name</span><span class="sxs-lookup"><span data-stu-id="d240d-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="d240d-114">Dieses Cmdlet erhält die angegebene MySQL-Konfiguration nach Namen.</span><span class="sxs-lookup"><span data-stu-id="d240d-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="d240d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d240d-115">PARAMETERS</span></span>

### <span data-ttu-id="d240d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d240d-116">-DefaultProfile</span></span>
<span data-ttu-id="d240d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d240d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d240d-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d240d-118">-InputObject</span></span>
<span data-ttu-id="d240d-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d240d-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d240d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d240d-120">-Name</span></span>
<span data-ttu-id="d240d-121">Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d240d-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="d240d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d240d-122">-ResourceGroupName</span></span>
<span data-ttu-id="d240d-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d240d-123">The name of the resource group.</span></span>
<span data-ttu-id="d240d-124">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="d240d-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d240d-125">-Servername</span><span class="sxs-lookup"><span data-stu-id="d240d-125">-ServerName</span></span>
<span data-ttu-id="d240d-126">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="d240d-126">The name of the server.</span></span>

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

### <span data-ttu-id="d240d-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d240d-127">-SubscriptionId</span></span>
<span data-ttu-id="d240d-128">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="d240d-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d240d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d240d-129">CommonParameters</span></span>
<span data-ttu-id="d240d-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d240d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d240d-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d240d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d240d-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d240d-132">INPUTS</span></span>

### <span data-ttu-id="d240d-133">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d240d-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d240d-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d240d-134">OUTPUTS</span></span>

### <span data-ttu-id="d240d-135">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="d240d-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="d240d-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="d240d-136">NOTES</span></span>

<span data-ttu-id="d240d-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="d240d-137">ALIASES</span></span>

<span data-ttu-id="d240d-138">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d240d-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d240d-139">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d240d-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d240d-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="d240d-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d240d-141">Inputobject <IMySqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="d240d-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d240d-142">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d240d-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d240d-143">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d240d-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d240d-144">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="d240d-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d240d-145">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="d240d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d240d-146">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="d240d-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d240d-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d240d-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d240d-148">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="d240d-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="d240d-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d240d-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d240d-150">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="d240d-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d240d-151">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="d240d-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d240d-152">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="d240d-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d240d-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d240d-153">RELATED LINKS</span></span>

