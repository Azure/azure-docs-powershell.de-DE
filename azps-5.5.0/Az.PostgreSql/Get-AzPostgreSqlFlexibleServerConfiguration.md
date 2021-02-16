---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: 0f65a007a37df559802a134ec5d6d8fc6fb33d01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146393"
---
# <span data-ttu-id="99e4e-101">Get-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="99e4e-101">Get-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="99e4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="99e4e-103">Ruft Informationen zu einer Serverkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="99e4e-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="99e4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99e4e-104">SYNTAX</span></span>

### <span data-ttu-id="99e4e-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="99e4e-105">List (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="99e4e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="99e4e-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="99e4e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="99e4e-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="99e4e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99e4e-108">DESCRIPTION</span></span>
<span data-ttu-id="99e4e-109">Ruft Informationen zu einer Serverkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="99e4e-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="99e4e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="99e4e-110">EXAMPLES</span></span>

### <span data-ttu-id="99e4e-111">Beispiel 1: Angegebene Konfiguration von PostgreSql nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="99e4e-111">Example 1: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem        4096  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="99e4e-112">Dieses Cmdlet wird nach Name als "PostgreSql-Konfiguration" angegeben.</span><span class="sxs-lookup"><span data-stu-id="99e4e-112">This cmdlet gets specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="99e4e-113">Beispiel 2: Auflisten aller Konfigurationen im angegebenen PostgreSql-Server</span><span class="sxs-lookup"><span data-stu-id="99e4e-113">Example 2: List all configurations in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
application_name  ""    ""           system-default [A-Za-z0-9._-]*      String
...
pgbouncer.enabled   false  false         system-default true, false   Boolean
```

<span data-ttu-id="99e4e-114">Dieses Cmdlet listet alle Konfigurationen im angegebenen Server von PostgreSql auf.</span><span class="sxs-lookup"><span data-stu-id="99e4e-114">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

## <span data-ttu-id="99e4e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99e4e-115">PARAMETERS</span></span>

### <span data-ttu-id="99e4e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e4e-116">-DefaultProfile</span></span>
<span data-ttu-id="99e4e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99e4e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99e4e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99e4e-118">-InputObject</span></span>
<span data-ttu-id="99e4e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="99e4e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="99e4e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="99e4e-120">-Name</span></span>
<span data-ttu-id="99e4e-121">Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="99e4e-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="99e4e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99e4e-122">-ResourceGroupName</span></span>
<span data-ttu-id="99e4e-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="99e4e-123">The name of the resource group.</span></span>
<span data-ttu-id="99e4e-124">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="99e4e-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="99e4e-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="99e4e-125">-ServerName</span></span>
<span data-ttu-id="99e4e-126">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="99e4e-126">The name of the server.</span></span>

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

### <span data-ttu-id="99e4e-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="99e4e-127">-SubscriptionId</span></span>
<span data-ttu-id="99e4e-128">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="99e4e-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="99e4e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e4e-129">CommonParameters</span></span>
<span data-ttu-id="99e4e-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99e4e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e4e-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99e4e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e4e-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="99e4e-132">INPUTS</span></span>

### <span data-ttu-id="99e4e-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="99e4e-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="99e4e-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="99e4e-134">OUTPUTS</span></span>

### <span data-ttu-id="99e4e-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="99e4e-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="99e4e-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="99e4e-136">NOTES</span></span>

<span data-ttu-id="99e4e-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="99e4e-137">ALIASES</span></span>

<span data-ttu-id="99e4e-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="99e4e-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="99e4e-139">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="99e4e-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="99e4e-140">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="99e4e-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="99e4e-141">INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="99e4e-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="99e4e-142">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="99e4e-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="99e4e-143">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="99e4e-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="99e4e-144">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="99e4e-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="99e4e-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="99e4e-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="99e4e-146">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="99e4e-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="99e4e-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="99e4e-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="99e4e-148">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="99e4e-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="99e4e-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="99e4e-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="99e4e-150">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="99e4e-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="99e4e-151">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="99e4e-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="99e4e-152">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="99e4e-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="99e4e-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="99e4e-153">RELATED LINKS</span></span>

