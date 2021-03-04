---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: dda229292436d07cf5383343cb85472b92881cdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927936"
---
# <span data-ttu-id="6e431-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6e431-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="6e431-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e431-102">SYNOPSIS</span></span>
<span data-ttu-id="6e431-103">Ruft eine Regel für ein virtuelles Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="6e431-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="6e431-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e431-104">SYNTAX</span></span>

### <span data-ttu-id="6e431-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="6e431-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="6e431-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="6e431-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="6e431-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6e431-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="6e431-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e431-108">DESCRIPTION</span></span>
<span data-ttu-id="6e431-109">Ruft eine Regel für ein virtuelles Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="6e431-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="6e431-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6e431-110">EXAMPLES</span></span>

### <span data-ttu-id="6e431-111">Beispiel 1: Auflisten aller virtuellen Netzwerkregel unter einer MariaDB</span><span class="sxs-lookup"><span data-stu-id="6e431-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="6e431-112">Mit diesem Befehl werden alle virtuellen Netzwerkregel unter einer MariaDB aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e431-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="6e431-113">Beispiel 2: Virtuelle Netzwerkregel unter einer MariaDB</span><span class="sxs-lookup"><span data-stu-id="6e431-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="6e431-114">Dieser Befehl ruft virtuelle Netzwerkregel unter einer MariaDB ab.</span><span class="sxs-lookup"><span data-stu-id="6e431-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="6e431-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6e431-115">PARAMETERS</span></span>

### <span data-ttu-id="6e431-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e431-116">-DefaultProfile</span></span>
<span data-ttu-id="6e431-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6e431-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e431-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e431-118">-InputObject</span></span>
<span data-ttu-id="6e431-119">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="6e431-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6e431-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6e431-120">-Name</span></span>
<span data-ttu-id="6e431-121">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="6e431-121">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="6e431-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e431-122">-PassThru</span></span>
<span data-ttu-id="6e431-123">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e431-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6e431-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e431-124">-ResourceGroupName</span></span>
<span data-ttu-id="6e431-125">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="6e431-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6e431-126">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="6e431-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6e431-127">-Servername</span><span class="sxs-lookup"><span data-stu-id="6e431-127">-ServerName</span></span>
<span data-ttu-id="6e431-128">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="6e431-128">The name of the server.</span></span>

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

### <span data-ttu-id="6e431-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6e431-129">-SubscriptionId</span></span>
<span data-ttu-id="6e431-130">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6e431-130">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="6e431-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e431-131">CommonParameters</span></span>
<span data-ttu-id="6e431-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e431-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e431-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e431-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e431-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6e431-134">INPUTS</span></span>

### <span data-ttu-id="6e431-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="6e431-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="6e431-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6e431-136">OUTPUTS</span></span>

### <span data-ttu-id="6e431-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6e431-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="6e431-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6e431-138">NOTES</span></span>

<span data-ttu-id="6e431-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="6e431-139">ALIASES</span></span>

<span data-ttu-id="6e431-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="6e431-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6e431-141">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="6e431-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6e431-142">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6e431-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6e431-143">INPUTOBJECT <IMariaDbIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="6e431-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6e431-144">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="6e431-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6e431-145">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="6e431-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6e431-146">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="6e431-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6e431-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="6e431-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6e431-148">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="6e431-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6e431-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="6e431-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="6e431-150">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="6e431-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="6e431-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="6e431-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6e431-152">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="6e431-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6e431-153">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6e431-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="6e431-154">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="6e431-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6e431-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6e431-155">RELATED LINKS</span></span>

