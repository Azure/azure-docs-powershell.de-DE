---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 2b2f52d8dc4f9e31a86b666b7ee81981fa6bd18c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009762"
---
# <span data-ttu-id="a9c7e-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a9c7e-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="a9c7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c7e-103">Ruft Informationen zu einer Server Firewall-Regel ab.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="a9c7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9c7e-104">SYNTAX</span></span>

### <span data-ttu-id="a9c7e-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9c7e-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a9c7e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="a9c7e-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a9c7e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a9c7e-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a9c7e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9c7e-108">DESCRIPTION</span></span>
<span data-ttu-id="a9c7e-109">Ruft Informationen zu einer Server Firewall-Regel ab.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="a9c7e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9c7e-110">EXAMPLES</span></span>

### <span data-ttu-id="a9c7e-111">Beispiel 1: Auflisten aller Firewallregel unter einem MariaDB</span><span class="sxs-lookup"><span data-stu-id="a9c7e-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="a9c7e-112">Dieser Befehl listet alle girewall-Regel unter einem MariaDB auf.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="a9c7e-113">Beispiel 2: Abrufen einer Firewall-Regel unter einem MariaDB</span><span class="sxs-lookup"><span data-stu-id="a9c7e-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="a9c7e-114">Dieser Befehl ruft eine Firewallregel unter einem MariaDB ab.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="a9c7e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9c7e-115">PARAMETERS</span></span>

### <span data-ttu-id="a9c7e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c7e-116">-DefaultProfile</span></span>
<span data-ttu-id="a9c7e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9c7e-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9c7e-118">-InputObject</span></span>
<span data-ttu-id="a9c7e-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9c7e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a9c7e-120">-Name</span></span>
<span data-ttu-id="a9c7e-121">Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-121">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9c7e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9c7e-122">-ResourceGroupName</span></span>
<span data-ttu-id="a9c7e-123">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a9c7e-124">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a9c7e-125">-Servername</span><span class="sxs-lookup"><span data-stu-id="a9c7e-125">-ServerName</span></span>
<span data-ttu-id="a9c7e-126">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-126">The name of the server.</span></span>

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

### <span data-ttu-id="a9c7e-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a9c7e-127">-SubscriptionId</span></span>
<span data-ttu-id="a9c7e-128">Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="a9c7e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c7e-129">CommonParameters</span></span>
<span data-ttu-id="a9c7e-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c7e-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9c7e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c7e-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9c7e-132">INPUTS</span></span>

### <span data-ttu-id="a9c7e-133">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="a9c7e-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="a9c7e-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9c7e-134">OUTPUTS</span></span>

### <span data-ttu-id="a9c7e-135">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a9c7e-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="a9c7e-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9c7e-136">NOTES</span></span>

<span data-ttu-id="a9c7e-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="a9c7e-137">ALIASES</span></span>

<span data-ttu-id="a9c7e-138">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a9c7e-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a9c7e-139">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a9c7e-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a9c7e-141">Inputobject <IMariaDbIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="a9c7e-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a9c7e-142">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a9c7e-143">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a9c7e-144">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a9c7e-145">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="a9c7e-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a9c7e-146">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a9c7e-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a9c7e-148">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a9c7e-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a9c7e-150">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a9c7e-151">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="a9c7e-152">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a9c7e-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a9c7e-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9c7e-153">RELATED LINKS</span></span>

