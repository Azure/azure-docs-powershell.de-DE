---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 91d774931ac7ef4b8f1d41a70953d4a5b3a322cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173682"
---
# <span data-ttu-id="4126b-101">Get-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4126b-101">Get-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="4126b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4126b-102">SYNOPSIS</span></span>
<span data-ttu-id="4126b-103">Ruft eine virtuelle Netzwerkregel ab.</span><span class="sxs-lookup"><span data-stu-id="4126b-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="4126b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4126b-104">SYNTAX</span></span>

### <span data-ttu-id="4126b-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="4126b-105">List (Default)</span></span>
```
Get-AzMySqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4126b-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="4126b-106">Get</span></span>
```
Get-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4126b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4126b-107">GetViaIdentity</span></span>
```
Get-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="4126b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4126b-108">DESCRIPTION</span></span>
<span data-ttu-id="4126b-109">Ruft eine virtuelle Netzwerkregel ab.</span><span class="sxs-lookup"><span data-stu-id="4126b-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="4126b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4126b-110">EXAMPLES</span></span>

### <span data-ttu-id="4126b-111">Beispiel 1: Listet alle virtuellen Netzwerkregeln im angegebenen MySQL-Server auf</span><span class="sxs-lookup"><span data-stu-id="4126b-111">Example 1: Lists all the Virtual Network Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="4126b-112">Mit diesem Cmdlet werden alle virtuellen Netzwerkregeln im angegebenen MySQL-Server aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4126b-112">This cmdlet lists all the Virtual Network Rules in specified MySql server.</span></span>

### <span data-ttu-id="4126b-113">Beispiel 2: Abrufen einer virtuellen Netzwerkregel nach Namen</span><span class="sxs-lookup"><span data-stu-id="4126b-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="4126b-114">Mit diesem Cmdlet wird die virtuelle Netzwerkregel nach Namen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4126b-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="4126b-115">Beispiel 3: Abrufen einer virtuellen Netzwerkregel nach Identität</span><span class="sxs-lookup"><span data-stu-id="4126b-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Get-AzMySqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="4126b-116">Dieses Cmdlet ruft eine virtuelle Netzwerkregel nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="4126b-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="4126b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="4126b-117">PARAMETERS</span></span>

### <span data-ttu-id="4126b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4126b-118">-DefaultProfile</span></span>
<span data-ttu-id="4126b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4126b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4126b-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4126b-120">-InputObject</span></span>
<span data-ttu-id="4126b-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="4126b-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4126b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4126b-122">-Name</span></span>
<span data-ttu-id="4126b-123">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="4126b-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="4126b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4126b-124">-PassThru</span></span>
<span data-ttu-id="4126b-125">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="4126b-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4126b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4126b-126">-ResourceGroupName</span></span>
<span data-ttu-id="4126b-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4126b-127">The name of the resource group.</span></span>
<span data-ttu-id="4126b-128">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="4126b-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4126b-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="4126b-129">-ServerName</span></span>
<span data-ttu-id="4126b-130">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="4126b-130">The name of the server.</span></span>

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

### <span data-ttu-id="4126b-131">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="4126b-131">-SubscriptionId</span></span>
<span data-ttu-id="4126b-132">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="4126b-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4126b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4126b-133">CommonParameters</span></span>
<span data-ttu-id="4126b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4126b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4126b-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4126b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4126b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4126b-136">INPUTS</span></span>

### <span data-ttu-id="4126b-137">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="4126b-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="4126b-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4126b-138">OUTPUTS</span></span>

### <span data-ttu-id="4126b-139">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4126b-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="4126b-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="4126b-140">NOTES</span></span>

<span data-ttu-id="4126b-141">Aliase</span><span class="sxs-lookup"><span data-stu-id="4126b-141">ALIASES</span></span>

<span data-ttu-id="4126b-142">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4126b-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4126b-143">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4126b-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4126b-144">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="4126b-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4126b-145">Inputobject <IMySqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="4126b-145">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4126b-146">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4126b-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4126b-147">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="4126b-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4126b-148">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="4126b-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4126b-149">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="4126b-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4126b-150">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="4126b-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4126b-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4126b-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4126b-152">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="4126b-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="4126b-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="4126b-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4126b-154">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="4126b-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4126b-155">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="4126b-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4126b-156">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="4126b-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4126b-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4126b-157">RELATED LINKS</span></span>

