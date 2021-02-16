---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 43b5563a9328a5b8f96c1fdb538dc49e721c428c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170177"
---
# <span data-ttu-id="284fd-101">Get-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="284fd-101">Get-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="284fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="284fd-102">SYNOPSIS</span></span>
<span data-ttu-id="284fd-103">Ruft Informationen zu einer Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="284fd-103">Gets information about a database.</span></span>

## <span data-ttu-id="284fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="284fd-104">SYNTAX</span></span>

### <span data-ttu-id="284fd-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="284fd-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerDatabase -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="284fd-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="284fd-106">Get</span></span>
```
Get-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="284fd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="284fd-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="284fd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="284fd-108">DESCRIPTION</span></span>
<span data-ttu-id="284fd-109">Ruft Informationen zu einer Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="284fd-109">Gets information about a database.</span></span>

## <span data-ttu-id="284fd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="284fd-110">EXAMPLES</span></span>

### <span data-ttu-id="284fd-111">Beispiel 1: Erhalten einer MeineSql-Datenbank nach Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="284fd-111">Example 1: Get a MySql database by resource name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Name flexibleserverdb

Name            Charset     Collation              
----            -------- ------------------
flexibleserverdb latin1   latin1_swedish_ci  
```

<span data-ttu-id="284fd-112">Dieses Cmdlet ruft den Server "MySql" nach dem Ressourcennamen ab.</span><span class="sxs-lookup"><span data-stu-id="284fd-112">This cmdlet gets MySql server by resource name.</span></span>

### <span data-ttu-id="284fd-113">Beispiel 2: Erhalten von MySql-Datenbanken nach Identität</span><span class="sxs-lookup"><span data-stu-id="284fd-113">Example 2: Get MySql databases by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServerDatabase -InputObject $ID

Name             Charset     Collation            
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci 
```

<span data-ttu-id="284fd-114">Dieses Cmdlet ruft einen "MySql"-Server nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="284fd-114">This cmdlet gets a MySql server by identity.</span></span>

### <span data-ttu-id="284fd-115">Beispiel 3: Listet alle MeineSql-Datenbanken auf dem angegebenen Server auf.</span><span class="sxs-lookup"><span data-stu-id="284fd-115">Example 3: Lists all the MySql databases in the specified server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name             Charset     Collation        
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci
```

<span data-ttu-id="284fd-116">Dieses Cmdlet listet alle MySql-Server auf, die den Server angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="284fd-116">This cmdlet lists all the MySql servers in specified the server.</span></span>

## <span data-ttu-id="284fd-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="284fd-117">PARAMETERS</span></span>

### <span data-ttu-id="284fd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="284fd-118">-DefaultProfile</span></span>
<span data-ttu-id="284fd-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="284fd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="284fd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="284fd-120">-InputObject</span></span>
<span data-ttu-id="284fd-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="284fd-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="284fd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="284fd-122">-Name</span></span>
<span data-ttu-id="284fd-123">Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="284fd-123">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="284fd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="284fd-124">-ResourceGroupName</span></span>
<span data-ttu-id="284fd-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="284fd-125">The name of the resource group.</span></span>
<span data-ttu-id="284fd-126">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="284fd-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="284fd-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="284fd-127">-ServerName</span></span>
<span data-ttu-id="284fd-128">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="284fd-128">The name of the server.</span></span>

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

### <span data-ttu-id="284fd-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="284fd-129">-SubscriptionId</span></span>
<span data-ttu-id="284fd-130">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="284fd-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="284fd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="284fd-131">CommonParameters</span></span>
<span data-ttu-id="284fd-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="284fd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="284fd-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="284fd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="284fd-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="284fd-134">INPUTS</span></span>

### <span data-ttu-id="284fd-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="284fd-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="284fd-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="284fd-136">OUTPUTS</span></span>

### <span data-ttu-id="284fd-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="284fd-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="284fd-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="284fd-138">NOTES</span></span>

<span data-ttu-id="284fd-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="284fd-139">ALIASES</span></span>

<span data-ttu-id="284fd-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="284fd-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="284fd-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="284fd-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="284fd-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="284fd-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="284fd-143">INPUTOBJECT <IMySqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="284fd-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="284fd-144">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="284fd-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="284fd-145">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="284fd-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="284fd-146">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="284fd-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="284fd-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="284fd-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="284fd-148">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="284fd-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="284fd-149">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="284fd-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="284fd-150">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="284fd-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="284fd-151">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="284fd-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="284fd-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="284fd-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="284fd-153">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="284fd-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="284fd-154">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="284fd-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="284fd-155">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="284fd-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="284fd-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="284fd-156">RELATED LINKS</span></span>

