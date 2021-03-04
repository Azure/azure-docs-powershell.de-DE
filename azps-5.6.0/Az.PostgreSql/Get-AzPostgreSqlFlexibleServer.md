---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 3354014ed0e6e81b1460da061e75e614bbd5f95c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948507"
---
# <span data-ttu-id="499e5-101">Get-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="499e5-101">Get-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="499e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="499e5-102">SYNOPSIS</span></span>
<span data-ttu-id="499e5-103">Ruft Informationen zu einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="499e5-103">Gets information about a server.</span></span>

## <span data-ttu-id="499e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="499e5-104">SYNTAX</span></span>

### <span data-ttu-id="499e5-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="499e5-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="499e5-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="499e5-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="499e5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="499e5-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="499e5-108">Liste</span><span class="sxs-lookup"><span data-stu-id="499e5-108">List</span></span>
```
Get-AzPostgreSqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="499e5-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="499e5-109">DESCRIPTION</span></span>
<span data-ttu-id="499e5-110">Ruft Informationen zu einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="499e5-110">Gets information about a server.</span></span>

## <span data-ttu-id="499e5-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="499e5-111">EXAMPLES</span></span>

### <span data-ttu-id="499e5-112">Beispiel 1: PostgreSql-Server mit Standardkontext erhalten</span><span class="sxs-lookup"><span data-stu-id="499e5-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="499e5-113">Dieses Cmdlet ruft PostgreSql-Server mit Standardkontext ab.</span><span class="sxs-lookup"><span data-stu-id="499e5-113">This cmdlet gets PostgreSql servers with default context.</span></span>

### <span data-ttu-id="499e5-114">Beispiel 2: Erhalten von PostgreSql-Server nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="499e5-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="499e5-115">Dieses Cmdlet ruft PostgreSql-Server nach Ressourcengruppe und Servernamen ab.</span><span class="sxs-lookup"><span data-stu-id="499e5-115">This cmdlet gets PostgreSql servers by resource group and server name.</span></span>

### <span data-ttu-id="499e5-116">Beispiel 3: Listet alle PostgreSql-Server in einer angegebenen Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="499e5-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest

Name             Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----             -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test  eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
postgresql-test2 eastus   postgresql-test     12     32768                   Standard_42s_v3 GeneralPurpose
```

<span data-ttu-id="499e5-117">In diesem Cmdlet werden alle PostgreSql-Server in der angegebenen Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="499e5-117">This cmdlet lists all the PostgreSql servers in the specified resource group.</span></span>

### <span data-ttu-id="499e5-118">Beispiel 4: Holen Sie sich den PostgreSql-Server nach Identität</span><span class="sxs-lookup"><span data-stu-id="499e5-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test"
PS C:\> Get-AzPostgreSqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test         12     32768                    Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="499e5-119">Diese Cmdletlisten erhalten PostgreSql-Server nach Identität.</span><span class="sxs-lookup"><span data-stu-id="499e5-119">This cmdlet lists gets PostgreSql servers by identity.</span></span>

## <span data-ttu-id="499e5-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="499e5-120">PARAMETERS</span></span>

### <span data-ttu-id="499e5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="499e5-121">-DefaultProfile</span></span>
<span data-ttu-id="499e5-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="499e5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="499e5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="499e5-123">-InputObject</span></span>
<span data-ttu-id="499e5-124">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="499e5-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="499e5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="499e5-125">-Name</span></span>
<span data-ttu-id="499e5-126">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="499e5-126">The name of the server.</span></span>

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

### <span data-ttu-id="499e5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="499e5-127">-ResourceGroupName</span></span>
<span data-ttu-id="499e5-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="499e5-128">The name of the resource group.</span></span>
<span data-ttu-id="499e5-129">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="499e5-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="499e5-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="499e5-130">-SubscriptionId</span></span>
<span data-ttu-id="499e5-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="499e5-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="499e5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="499e5-132">CommonParameters</span></span>
<span data-ttu-id="499e5-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="499e5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="499e5-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="499e5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="499e5-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="499e5-135">INPUTS</span></span>

### <span data-ttu-id="499e5-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="499e5-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="499e5-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="499e5-137">OUTPUTS</span></span>

### <span data-ttu-id="499e5-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="499e5-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="499e5-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="499e5-139">NOTES</span></span>

<span data-ttu-id="499e5-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="499e5-140">ALIASES</span></span>

<span data-ttu-id="499e5-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="499e5-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="499e5-142">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="499e5-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="499e5-143">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="499e5-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="499e5-144">INPUTOBJECT <IPostgreSqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="499e5-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="499e5-145">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="499e5-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="499e5-146">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="499e5-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="499e5-147">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="499e5-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="499e5-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="499e5-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="499e5-149">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="499e5-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="499e5-150">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="499e5-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="499e5-151">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="499e5-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="499e5-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="499e5-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="499e5-153">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="499e5-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="499e5-154">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="499e5-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="499e5-155">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="499e5-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="499e5-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="499e5-156">RELATED LINKS</span></span>

