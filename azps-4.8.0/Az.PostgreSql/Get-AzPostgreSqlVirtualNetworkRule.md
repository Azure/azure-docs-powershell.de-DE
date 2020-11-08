---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: eb8fc13bd2c1ef4e829cf5d4626453909b6ff773
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165059"
---
# <span data-ttu-id="20c8f-101">Get-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="20c8f-101">Get-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="20c8f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20c8f-102">SYNOPSIS</span></span>
<span data-ttu-id="20c8f-103">Ruft eine virtuelle Netzwerkregel ab.</span><span class="sxs-lookup"><span data-stu-id="20c8f-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="20c8f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20c8f-104">SYNTAX</span></span>

### <span data-ttu-id="20c8f-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="20c8f-105">List (Default)</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="20c8f-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="20c8f-106">Get</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="20c8f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="20c8f-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="20c8f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20c8f-108">DESCRIPTION</span></span>
<span data-ttu-id="20c8f-109">Ruft eine virtuelle Netzwerkregel ab.</span><span class="sxs-lookup"><span data-stu-id="20c8f-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="20c8f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20c8f-110">EXAMPLES</span></span>

### <span data-ttu-id="20c8f-111">Beispiel 1: Listet alle virtuellen Netzwerkregeln auf dem angegebenen PostgreSQL-Server auf</span><span class="sxs-lookup"><span data-stu-id="20c8f-111">Example 1: Lists all the Virtual Network Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="20c8f-112">Mit diesem Cmdlet werden alle virtuellen Netzwerkregeln auf dem angegebenen PostgreSQL-Server aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="20c8f-112">This cmdlet lists all the Virtual Network Rules in specified PostgreSql server.</span></span>

### <span data-ttu-id="20c8f-113">Beispiel 2: Abrufen einer virtuellen Netzwerkregel nach Namen</span><span class="sxs-lookup"><span data-stu-id="20c8f-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="20c8f-114">Mit diesem Cmdlet wird die virtuelle Netzwerkregel nach Namen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="20c8f-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="20c8f-115">Beispiel 3: Abrufen einer virtuellen Netzwerkregel nach Identität</span><span class="sxs-lookup"><span data-stu-id="20c8f-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="20c8f-116">Dieses Cmdlet ruft eine virtuelle Netzwerkregel nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="20c8f-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="20c8f-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="20c8f-117">PARAMETERS</span></span>

### <span data-ttu-id="20c8f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c8f-118">-DefaultProfile</span></span>
<span data-ttu-id="20c8f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="20c8f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20c8f-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="20c8f-120">-InputObject</span></span>
<span data-ttu-id="20c8f-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="20c8f-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="20c8f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="20c8f-122">-Name</span></span>
<span data-ttu-id="20c8f-123">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="20c8f-123">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20c8f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20c8f-124">-PassThru</span></span>
<span data-ttu-id="20c8f-125">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="20c8f-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20c8f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20c8f-126">-ResourceGroupName</span></span>
<span data-ttu-id="20c8f-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="20c8f-127">The name of the resource group.</span></span>
<span data-ttu-id="20c8f-128">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="20c8f-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="20c8f-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="20c8f-129">-ServerName</span></span>
<span data-ttu-id="20c8f-130">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="20c8f-130">The name of the server.</span></span>

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

### <span data-ttu-id="20c8f-131">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="20c8f-131">-SubscriptionId</span></span>
<span data-ttu-id="20c8f-132">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="20c8f-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="20c8f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c8f-133">CommonParameters</span></span>
<span data-ttu-id="20c8f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20c8f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c8f-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20c8f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c8f-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20c8f-136">INPUTS</span></span>

### <span data-ttu-id="20c8f-137">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="20c8f-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="20c8f-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20c8f-138">OUTPUTS</span></span>

### <span data-ttu-id="20c8f-139">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="20c8f-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="20c8f-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="20c8f-140">NOTES</span></span>

<span data-ttu-id="20c8f-141">Aliase</span><span class="sxs-lookup"><span data-stu-id="20c8f-141">ALIASES</span></span>

<span data-ttu-id="20c8f-142">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="20c8f-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="20c8f-143">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="20c8f-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="20c8f-144">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="20c8f-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="20c8f-145">Inputobject <IPostgreSqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="20c8f-145">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="20c8f-146">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="20c8f-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="20c8f-147">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="20c8f-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="20c8f-148">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="20c8f-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="20c8f-149">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="20c8f-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="20c8f-150">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="20c8f-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="20c8f-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="20c8f-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="20c8f-152">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="20c8f-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="20c8f-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="20c8f-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="20c8f-154">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="20c8f-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="20c8f-155">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="20c8f-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="20c8f-156">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="20c8f-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="20c8f-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20c8f-157">RELATED LINKS</span></span>

