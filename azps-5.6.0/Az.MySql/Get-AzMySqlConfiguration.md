---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: 7b1ed42777dcd24460dabb91cf67160dac709aea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935672"
---
# <span data-ttu-id="424d5-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="424d5-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="424d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="424d5-102">SYNOPSIS</span></span>
<span data-ttu-id="424d5-103">Ruft Informationen zu einer Serverkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="424d5-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="424d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="424d5-104">SYNTAX</span></span>

### <span data-ttu-id="424d5-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="424d5-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="424d5-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="424d5-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="424d5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="424d5-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="424d5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="424d5-108">DESCRIPTION</span></span>
<span data-ttu-id="424d5-109">Ruft Informationen zu einer Serverkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="424d5-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="424d5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="424d5-110">EXAMPLES</span></span>

### <span data-ttu-id="424d5-111">Beispiel 1: Auflisten aller Konfigurationen im angegebenen MySql-Server</span><span class="sxs-lookup"><span data-stu-id="424d5-111">Example 1: List all configurations in specified MySql server</span></span>
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

<span data-ttu-id="424d5-112">In diesem Cmdlet werden alle Konfigurationen im angegebenen MySql-Server aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="424d5-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="424d5-113">Beispiel 2: Angegebene MySql-Konfiguration nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="424d5-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="424d5-114">Dieses Cmdlet erhält die angegebene MySql-Konfiguration nach Name.</span><span class="sxs-lookup"><span data-stu-id="424d5-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="424d5-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="424d5-115">PARAMETERS</span></span>

### <span data-ttu-id="424d5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424d5-116">-DefaultProfile</span></span>
<span data-ttu-id="424d5-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="424d5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="424d5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="424d5-118">-InputObject</span></span>
<span data-ttu-id="424d5-119">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="424d5-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="424d5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="424d5-120">-Name</span></span>
<span data-ttu-id="424d5-121">Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="424d5-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="424d5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="424d5-122">-ResourceGroupName</span></span>
<span data-ttu-id="424d5-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="424d5-123">The name of the resource group.</span></span>
<span data-ttu-id="424d5-124">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="424d5-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="424d5-125">-Servername</span><span class="sxs-lookup"><span data-stu-id="424d5-125">-ServerName</span></span>
<span data-ttu-id="424d5-126">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="424d5-126">The name of the server.</span></span>

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

### <span data-ttu-id="424d5-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="424d5-127">-SubscriptionId</span></span>
<span data-ttu-id="424d5-128">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="424d5-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="424d5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424d5-129">CommonParameters</span></span>
<span data-ttu-id="424d5-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="424d5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424d5-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="424d5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424d5-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="424d5-132">INPUTS</span></span>

### <span data-ttu-id="424d5-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="424d5-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="424d5-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="424d5-134">OUTPUTS</span></span>

### <span data-ttu-id="424d5-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="424d5-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="424d5-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="424d5-136">NOTES</span></span>

<span data-ttu-id="424d5-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="424d5-137">ALIASES</span></span>

<span data-ttu-id="424d5-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="424d5-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="424d5-139">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="424d5-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="424d5-140">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="424d5-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="424d5-141">INPUTOBJECT <IMySqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="424d5-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="424d5-142">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="424d5-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="424d5-143">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="424d5-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="424d5-144">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="424d5-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="424d5-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="424d5-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="424d5-146">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="424d5-146">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="424d5-147">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="424d5-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="424d5-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="424d5-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="424d5-149">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="424d5-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="424d5-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="424d5-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="424d5-151">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="424d5-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="424d5-152">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="424d5-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="424d5-153">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="424d5-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="424d5-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="424d5-154">RELATED LINKS</span></span>

