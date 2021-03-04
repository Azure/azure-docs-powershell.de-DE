---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 30e361d77f3c3b738703e1dde075ccbabc38b0b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932539"
---
# <span data-ttu-id="2d586-101">Get-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2d586-101">Get-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="2d586-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d586-102">SYNOPSIS</span></span>
<span data-ttu-id="2d586-103">Ruft eine Regel für ein virtuelles Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="2d586-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="2d586-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d586-104">SYNTAX</span></span>

### <span data-ttu-id="2d586-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d586-105">List (Default)</span></span>
```
Get-AzMySqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="2d586-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="2d586-106">Get</span></span>
```
Get-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="2d586-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2d586-107">GetViaIdentity</span></span>
```
Get-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="2d586-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d586-108">DESCRIPTION</span></span>
<span data-ttu-id="2d586-109">Ruft eine Regel für ein virtuelles Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="2d586-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="2d586-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2d586-110">EXAMPLES</span></span>

### <span data-ttu-id="2d586-111">Beispiel 1: Listet alle Regeln für virtuelle Netzwerke im angegebenen MySql-Server auf.</span><span class="sxs-lookup"><span data-stu-id="2d586-111">Example 1: Lists all the Virtual Network Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="2d586-112">In diesem Cmdlet werden alle Regeln für virtuelle Netzwerke im angegebenen MySql-Server aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d586-112">This cmdlet lists all the Virtual Network Rules in specified MySql server.</span></span>

### <span data-ttu-id="2d586-113">Beispiel 2: Virtuelle Netzwerkregel nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="2d586-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="2d586-114">Dieses Cmdlet ruft virtuelle Netzwerkregel nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="2d586-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="2d586-115">Beispiel 3: Virtuelle Netzwerkregel nach Identität erhalten</span><span class="sxs-lookup"><span data-stu-id="2d586-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Get-AzMySqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="2d586-116">Dieses Cmdlet ruft virtuelle Netzwerkregel nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="2d586-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="2d586-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2d586-117">PARAMETERS</span></span>

### <span data-ttu-id="2d586-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d586-118">-DefaultProfile</span></span>
<span data-ttu-id="2d586-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d586-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d586-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d586-120">-InputObject</span></span>
<span data-ttu-id="2d586-121">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2d586-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2d586-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2d586-122">-Name</span></span>
<span data-ttu-id="2d586-123">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="2d586-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="2d586-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d586-124">-PassThru</span></span>
<span data-ttu-id="2d586-125">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d586-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2d586-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d586-126">-ResourceGroupName</span></span>
<span data-ttu-id="2d586-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2d586-127">The name of the resource group.</span></span>
<span data-ttu-id="2d586-128">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="2d586-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2d586-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="2d586-129">-ServerName</span></span>
<span data-ttu-id="2d586-130">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="2d586-130">The name of the server.</span></span>

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

### <span data-ttu-id="2d586-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d586-131">-SubscriptionId</span></span>
<span data-ttu-id="2d586-132">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2d586-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2d586-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d586-133">CommonParameters</span></span>
<span data-ttu-id="2d586-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d586-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d586-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d586-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d586-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2d586-136">INPUTS</span></span>

### <span data-ttu-id="2d586-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="2d586-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="2d586-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2d586-138">OUTPUTS</span></span>

### <span data-ttu-id="2d586-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2d586-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="2d586-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2d586-140">NOTES</span></span>

<span data-ttu-id="2d586-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2d586-141">ALIASES</span></span>

<span data-ttu-id="2d586-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="2d586-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2d586-143">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="2d586-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2d586-144">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2d586-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2d586-145">INPUTOBJECT <IMySqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="2d586-145">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2d586-146">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d586-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2d586-147">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2d586-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2d586-148">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="2d586-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2d586-149">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="2d586-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2d586-150">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="2d586-150">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="2d586-151">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="2d586-151">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2d586-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2d586-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2d586-153">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="2d586-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="2d586-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2d586-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2d586-155">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="2d586-155">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2d586-156">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2d586-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2d586-157">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="2d586-157">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2d586-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2d586-158">RELATED LINKS</span></span>

