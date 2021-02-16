---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 7ae1159c3cd5f5feea3d836a421dd9fe08c78da8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157473"
---
# <span data-ttu-id="f162e-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f162e-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="f162e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f162e-102">SYNOPSIS</span></span>
<span data-ttu-id="f162e-103">Ruft eine Regel für ein virtuelles Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="f162e-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="f162e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f162e-104">SYNTAX</span></span>

### <span data-ttu-id="f162e-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="f162e-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="f162e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="f162e-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="f162e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f162e-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="f162e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f162e-108">DESCRIPTION</span></span>
<span data-ttu-id="f162e-109">Ruft eine Regel für ein virtuelles Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="f162e-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="f162e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f162e-110">EXAMPLES</span></span>

### <span data-ttu-id="f162e-111">Beispiel 1: Auflisten aller Regeln für virtuelle Netzwerke unter einer MariaDB</span><span class="sxs-lookup"><span data-stu-id="f162e-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="f162e-112">Dieser Befehl listet alle Regeln für virtuelle Netzwerke unter einer MariaDB auf.</span><span class="sxs-lookup"><span data-stu-id="f162e-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="f162e-113">Beispiel 2: Erhalten einer Regel für ein virtuelles Netzwerk unter einer MariaDB</span><span class="sxs-lookup"><span data-stu-id="f162e-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="f162e-114">Dieser Befehl ruft eine Regel für das virtuelle Netzwerk unter einer MariaDB ab.</span><span class="sxs-lookup"><span data-stu-id="f162e-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="f162e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f162e-115">PARAMETERS</span></span>

### <span data-ttu-id="f162e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f162e-116">-DefaultProfile</span></span>
<span data-ttu-id="f162e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f162e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f162e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f162e-118">-InputObject</span></span>
<span data-ttu-id="f162e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f162e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f162e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f162e-120">-Name</span></span>
<span data-ttu-id="f162e-121">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f162e-121">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="f162e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f162e-122">-PassThru</span></span>
<span data-ttu-id="f162e-123">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="f162e-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f162e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f162e-124">-ResourceGroupName</span></span>
<span data-ttu-id="f162e-125">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="f162e-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f162e-126">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="f162e-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f162e-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f162e-127">-ServerName</span></span>
<span data-ttu-id="f162e-128">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="f162e-128">The name of the server.</span></span>

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

### <span data-ttu-id="f162e-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f162e-129">-SubscriptionId</span></span>
<span data-ttu-id="f162e-130">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f162e-130">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="f162e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f162e-131">CommonParameters</span></span>
<span data-ttu-id="f162e-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f162e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f162e-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f162e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f162e-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f162e-134">INPUTS</span></span>

### <span data-ttu-id="f162e-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="f162e-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="f162e-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f162e-136">OUTPUTS</span></span>

### <span data-ttu-id="f162e-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f162e-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="f162e-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f162e-138">NOTES</span></span>

<span data-ttu-id="f162e-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f162e-139">ALIASES</span></span>

<span data-ttu-id="f162e-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="f162e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f162e-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f162e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f162e-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f162e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f162e-143">INPUTOBJECT <IMariaDbIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="f162e-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f162e-144">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f162e-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f162e-145">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f162e-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f162e-146">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="f162e-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f162e-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="f162e-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f162e-148">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="f162e-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f162e-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="f162e-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f162e-150">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="f162e-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f162e-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="f162e-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f162e-152">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="f162e-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f162e-153">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f162e-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="f162e-154">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f162e-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f162e-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f162e-155">RELATED LINKS</span></span>

