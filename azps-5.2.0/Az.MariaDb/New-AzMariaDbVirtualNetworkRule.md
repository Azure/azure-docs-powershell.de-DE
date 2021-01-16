---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 77a89dec96e0e9b7ca7bd003f8368274edf6acdf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305192"
---
# <span data-ttu-id="ed51f-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ed51f-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="ed51f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed51f-102">SYNOPSIS</span></span>
<span data-ttu-id="ed51f-103">Erstellt oder aktualisiert eine vorhandene Regel für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="ed51f-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="ed51f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed51f-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ed51f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed51f-105">DESCRIPTION</span></span>
<span data-ttu-id="ed51f-106">Erstellt oder aktualisiert eine vorhandene Regel für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="ed51f-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="ed51f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ed51f-107">EXAMPLES</span></span>

### <span data-ttu-id="ed51f-108">Beispiel 1: Erstellen einer Virtuellen Netzwerkregel für eine MariaDB</span><span class="sxs-lookup"><span data-stu-id="ed51f-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="ed51f-109">Mit diesem Befehl wird eine virtuelle Netzwerkregel für eine MariaDB erstellt.</span><span class="sxs-lookup"><span data-stu-id="ed51f-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="ed51f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed51f-110">PARAMETERS</span></span>

### <span data-ttu-id="ed51f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed51f-111">-AsJob</span></span>
<span data-ttu-id="ed51f-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="ed51f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ed51f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed51f-113">-DefaultProfile</span></span>
<span data-ttu-id="ed51f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed51f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed51f-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed51f-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="ed51f-116">Erstellen Sie eine Firewallregel, bevor der vnetdienstendpunkt im virtuellen Netzwerk aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ed51f-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="ed51f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ed51f-117">-Name</span></span>
<span data-ttu-id="ed51f-118">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="ed51f-118">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed51f-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ed51f-119">-NoWait</span></span>
<span data-ttu-id="ed51f-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="ed51f-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ed51f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed51f-121">-PassThru</span></span>
<span data-ttu-id="ed51f-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ed51f-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ed51f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed51f-123">-ResourceGroupName</span></span>
<span data-ttu-id="ed51f-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="ed51f-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ed51f-125">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="ed51f-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed51f-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ed51f-126">-ServerName</span></span>
<span data-ttu-id="ed51f-127">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="ed51f-127">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed51f-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ed51f-128">-SubnetId</span></span>
<span data-ttu-id="ed51f-129">Die ARM Ressourcen-ID des virtuellen Netzwerk-Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="ed51f-129">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed51f-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed51f-130">-SubscriptionId</span></span>
<span data-ttu-id="ed51f-131">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ed51f-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed51f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed51f-132">-Confirm</span></span>
<span data-ttu-id="ed51f-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed51f-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed51f-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ed51f-134">-WhatIf</span></span>
<span data-ttu-id="ed51f-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed51f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed51f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed51f-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed51f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed51f-137">CommonParameters</span></span>
<span data-ttu-id="ed51f-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed51f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed51f-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed51f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed51f-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ed51f-140">INPUTS</span></span>

## <span data-ttu-id="ed51f-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ed51f-141">OUTPUTS</span></span>

### <span data-ttu-id="ed51f-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ed51f-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="ed51f-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ed51f-143">NOTES</span></span>

<span data-ttu-id="ed51f-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ed51f-144">ALIASES</span></span>

## <span data-ttu-id="ed51f-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ed51f-145">RELATED LINKS</span></span>

