---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
ms.openlocfilehash: 10a3ca97d5f4bba9bf47eff5b2e4bdbb29b8ff24
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157289"
---
# <span data-ttu-id="c5bba-101">Get-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="c5bba-101">Get-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="c5bba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5bba-102">SYNOPSIS</span></span>
<span data-ttu-id="c5bba-103">Ruft Informationen zu einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="c5bba-103">Gets information about a server.</span></span>

## <span data-ttu-id="c5bba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5bba-104">SYNTAX</span></span>

### <span data-ttu-id="c5bba-105">Liste1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="c5bba-105">List1 (Default)</span></span>
```
Get-AzMySqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c5bba-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="c5bba-106">Get</span></span>
```
Get-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c5bba-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c5bba-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c5bba-108">Liste</span><span class="sxs-lookup"><span data-stu-id="c5bba-108">List</span></span>
```
Get-AzMySqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c5bba-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5bba-109">DESCRIPTION</span></span>
<span data-ttu-id="c5bba-110">Ruft Informationen zu einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="c5bba-110">Gets information about a server.</span></span>

## <span data-ttu-id="c5bba-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c5bba-111">EXAMPLES</span></span>

### <span data-ttu-id="c5bba-112">Beispiel 1: Get MySql server with default context</span><span class="sxs-lookup"><span data-stu-id="c5bba-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11  westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="c5bba-113">Dieses Cmdlet ruft die Server von MySql mit dem Standardkontext ab.</span><span class="sxs-lookup"><span data-stu-id="c5bba-113">This cmdlet gets MySql servers with default context.</span></span>

### <span data-ttu-id="c5bba-114">Beispiel 2: "MySql-Server nach Ressourcengruppe und Servername erhalten"</span><span class="sxs-lookup"><span data-stu-id="c5bba-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test     westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="c5bba-115">Dieses Cmdlet ruft die MeineSqlserver nach Ressourcengruppe und Servernamen ab.</span><span class="sxs-lookup"><span data-stu-id="c5bba-115">This cmdlet gets MySql servers by resource group and server name.</span></span>

### <span data-ttu-id="c5bba-116">Beispiel 3: Listet alle MeineSqlserver in der angegebenen Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="c5bba-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11 westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
mysql-test-12 westus2   mysql_test2        5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="c5bba-117">Dieses Cmdlet listet alle MeineSqlserver in der angegebenen Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="c5bba-117">This cmdlet lists all the MySql servers in the specified resource group.</span></span>

### <span data-ttu-id="c5bba-118">Beispiel 4: "MySql-Server nach Identität erhalten"</span><span class="sxs-lookup"><span data-stu-id="c5bba-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="c5bba-119">Diese Cmdletlisten ruft die Server von MySql nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="c5bba-119">This cmdlet lists gets MySql servers by identity.</span></span>

## <span data-ttu-id="c5bba-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5bba-120">PARAMETERS</span></span>

### <span data-ttu-id="c5bba-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5bba-121">-DefaultProfile</span></span>
<span data-ttu-id="c5bba-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5bba-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5bba-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5bba-123">-InputObject</span></span>
<span data-ttu-id="c5bba-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c5bba-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c5bba-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c5bba-125">-Name</span></span>
<span data-ttu-id="c5bba-126">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="c5bba-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5bba-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5bba-127">-ResourceGroupName</span></span>
<span data-ttu-id="c5bba-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c5bba-128">The name of the resource group.</span></span>
<span data-ttu-id="c5bba-129">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="c5bba-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c5bba-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c5bba-130">-SubscriptionId</span></span>
<span data-ttu-id="c5bba-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="c5bba-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5bba-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5bba-132">CommonParameters</span></span>
<span data-ttu-id="c5bba-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5bba-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5bba-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5bba-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5bba-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c5bba-135">INPUTS</span></span>

### <span data-ttu-id="c5bba-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="c5bba-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="c5bba-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c5bba-137">OUTPUTS</span></span>

### <span data-ttu-id="c5bba-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="c5bba-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="c5bba-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c5bba-139">NOTES</span></span>

<span data-ttu-id="c5bba-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c5bba-140">ALIASES</span></span>

<span data-ttu-id="c5bba-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="c5bba-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c5bba-142">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c5bba-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c5bba-143">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c5bba-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c5bba-144">INPUTOBJECT <IMySqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="c5bba-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c5bba-145">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="c5bba-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c5bba-146">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c5bba-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c5bba-147">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="c5bba-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c5bba-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="c5bba-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c5bba-149">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="c5bba-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="c5bba-150">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="c5bba-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c5bba-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c5bba-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c5bba-152">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="c5bba-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="c5bba-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="c5bba-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c5bba-154">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="c5bba-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c5bba-155">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="c5bba-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c5bba-156">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c5bba-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c5bba-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c5bba-157">RELATED LINKS</span></span>

