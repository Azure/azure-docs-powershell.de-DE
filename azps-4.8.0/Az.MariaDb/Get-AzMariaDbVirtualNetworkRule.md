---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 7ae1159c3cd5f5feea3d836a421dd9fe08c78da8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166511"
---
# <span data-ttu-id="91486-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="91486-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="91486-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91486-102">SYNOPSIS</span></span>
<span data-ttu-id="91486-103">Ruft eine virtuelle Netzwerkregel ab.</span><span class="sxs-lookup"><span data-stu-id="91486-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="91486-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91486-104">SYNTAX</span></span>

### <span data-ttu-id="91486-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="91486-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="91486-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="91486-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="91486-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="91486-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="91486-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91486-108">DESCRIPTION</span></span>
<span data-ttu-id="91486-109">Ruft eine virtuelle Netzwerkregel ab.</span><span class="sxs-lookup"><span data-stu-id="91486-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="91486-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91486-110">EXAMPLES</span></span>

### <span data-ttu-id="91486-111">Beispiel 1: Auflisten der gesamten virtuellen Netzwerkregel unter einem MariaDB</span><span class="sxs-lookup"><span data-stu-id="91486-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="91486-112">Dieser Befehl listet alle virtuellen Netzwerkregeln unter einem MariaDB auf.</span><span class="sxs-lookup"><span data-stu-id="91486-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="91486-113">Beispiel 2: Abrufen einer virtuellen Netzwerkregel unter einem MariaDB</span><span class="sxs-lookup"><span data-stu-id="91486-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="91486-114">Dieser Befehl ruft eine virtuelle Netzwerkregel unter einem MariaDB.</span><span class="sxs-lookup"><span data-stu-id="91486-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="91486-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="91486-115">PARAMETERS</span></span>

### <span data-ttu-id="91486-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91486-116">-DefaultProfile</span></span>
<span data-ttu-id="91486-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91486-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91486-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="91486-118">-InputObject</span></span>
<span data-ttu-id="91486-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="91486-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="91486-120">-Name</span><span class="sxs-lookup"><span data-stu-id="91486-120">-Name</span></span>
<span data-ttu-id="91486-121">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="91486-121">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="91486-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91486-122">-PassThru</span></span>
<span data-ttu-id="91486-123">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="91486-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="91486-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91486-124">-ResourceGroupName</span></span>
<span data-ttu-id="91486-125">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="91486-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="91486-126">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="91486-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="91486-127">-Servername</span><span class="sxs-lookup"><span data-stu-id="91486-127">-ServerName</span></span>
<span data-ttu-id="91486-128">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="91486-128">The name of the server.</span></span>

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

### <span data-ttu-id="91486-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="91486-129">-SubscriptionId</span></span>
<span data-ttu-id="91486-130">Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="91486-130">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="91486-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91486-131">CommonParameters</span></span>
<span data-ttu-id="91486-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91486-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91486-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91486-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91486-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91486-134">INPUTS</span></span>

### <span data-ttu-id="91486-135">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="91486-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="91486-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91486-136">OUTPUTS</span></span>

### <span data-ttu-id="91486-137">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="91486-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="91486-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="91486-138">NOTES</span></span>

<span data-ttu-id="91486-139">Aliase</span><span class="sxs-lookup"><span data-stu-id="91486-139">ALIASES</span></span>

<span data-ttu-id="91486-140">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91486-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="91486-141">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="91486-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="91486-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="91486-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="91486-143">Inputobject <IMariaDbIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="91486-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="91486-144">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="91486-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="91486-145">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="91486-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="91486-146">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="91486-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="91486-147">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="91486-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="91486-148">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="91486-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="91486-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="91486-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="91486-150">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="91486-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="91486-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="91486-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="91486-152">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="91486-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="91486-153">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="91486-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="91486-154">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="91486-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="91486-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91486-155">RELATED LINKS</span></span>

