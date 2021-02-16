---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: d8dc345ae9f307bbd5f1cd003edf1cba4a7ea6b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160393"
---
# <span data-ttu-id="9c150-101">Get-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="9c150-101">Get-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="9c150-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c150-102">SYNOPSIS</span></span>
<span data-ttu-id="9c150-103">Ruft Informationen zu einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="9c150-103">Gets information about a server.</span></span>

## <span data-ttu-id="9c150-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c150-104">SYNTAX</span></span>

### <span data-ttu-id="9c150-105">Liste1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="9c150-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9c150-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="9c150-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9c150-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9c150-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c150-108">Liste</span><span class="sxs-lookup"><span data-stu-id="9c150-108">List</span></span>
```
Get-AzPostgreSqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9c150-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c150-109">DESCRIPTION</span></span>
<span data-ttu-id="9c150-110">Ruft Informationen zu einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="9c150-110">Gets information about a server.</span></span>

## <span data-ttu-id="9c150-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9c150-111">EXAMPLES</span></span>

### <span data-ttu-id="9c150-112">Beispiel 1: Server "PostgreSql" mit Standardkontext erhalten</span><span class="sxs-lookup"><span data-stu-id="9c150-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="9c150-113">Dieses Cmdlet ruft die PostgreSql-Server mit dem Standardkontext ab.</span><span class="sxs-lookup"><span data-stu-id="9c150-113">This cmdlet gets PostgreSql servers with default context.</span></span>

### <span data-ttu-id="9c150-114">Beispiel 2: "PostgreSql-Server nach Ressourcengruppe und Servername erhalten"</span><span class="sxs-lookup"><span data-stu-id="9c150-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="9c150-115">Dieses Cmdlet ruft die PostgreSql-Server nach Ressourcengruppe und Servernamen ab.</span><span class="sxs-lookup"><span data-stu-id="9c150-115">This cmdlet gets PostgreSql servers by resource group and server name.</span></span>

### <span data-ttu-id="9c150-116">Beispiel 3: Listet alle PostgreSql-Server in der angegebenen Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="9c150-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest

Name             Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----             -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test  eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
postgresql-test2 eastus   postgresql-test     12     32768                   Standard_42s_v3 GeneralPurpose
```

<span data-ttu-id="9c150-117">Dieses Cmdlet listet alle PostgreSql-Server in der angegebenen Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="9c150-117">This cmdlet lists all the PostgreSql servers in the specified resource group.</span></span>

### <span data-ttu-id="9c150-118">Beispiel 4: Erhalten des PostgreSql-Servers nach Identität</span><span class="sxs-lookup"><span data-stu-id="9c150-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test"
PS C:\> Get-AzPostgreSqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test         12     32768                    Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="9c150-119">Diese Cmdletlisten ruft die Server von PostgreSql nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="9c150-119">This cmdlet lists gets PostgreSql servers by identity.</span></span>

## <span data-ttu-id="9c150-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c150-120">PARAMETERS</span></span>

### <span data-ttu-id="9c150-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c150-121">-DefaultProfile</span></span>
<span data-ttu-id="9c150-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9c150-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c150-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c150-123">-InputObject</span></span>
<span data-ttu-id="9c150-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="9c150-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9c150-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9c150-125">-Name</span></span>
<span data-ttu-id="9c150-126">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="9c150-126">The name of the server.</span></span>

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

### <span data-ttu-id="9c150-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c150-127">-ResourceGroupName</span></span>
<span data-ttu-id="9c150-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9c150-128">The name of the resource group.</span></span>
<span data-ttu-id="9c150-129">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="9c150-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9c150-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c150-130">-SubscriptionId</span></span>
<span data-ttu-id="9c150-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="9c150-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9c150-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c150-132">CommonParameters</span></span>
<span data-ttu-id="9c150-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c150-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c150-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c150-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c150-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9c150-135">INPUTS</span></span>

### <span data-ttu-id="9c150-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="9c150-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="9c150-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9c150-137">OUTPUTS</span></span>

### <span data-ttu-id="9c150-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="9c150-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="9c150-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9c150-139">NOTES</span></span>

<span data-ttu-id="9c150-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="9c150-140">ALIASES</span></span>

<span data-ttu-id="9c150-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="9c150-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9c150-142">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9c150-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9c150-143">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9c150-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9c150-144">INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="9c150-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9c150-145">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="9c150-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9c150-146">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9c150-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9c150-147">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="9c150-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9c150-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="9c150-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9c150-149">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="9c150-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9c150-150">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9c150-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9c150-151">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="9c150-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="9c150-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="9c150-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9c150-153">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="9c150-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9c150-154">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="9c150-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9c150-155">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="9c150-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9c150-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9c150-156">RELATED LINKS</span></span>

