---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: cfbbfd9472d18d75dea3da68cb4d2e06cf54c9a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927899"
---
# <span data-ttu-id="00370-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="00370-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="00370-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00370-102">SYNOPSIS</span></span>
<span data-ttu-id="00370-103">Erstellt oder aktualisiert eine vorhandene Regel für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="00370-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="00370-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00370-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="00370-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00370-105">DESCRIPTION</span></span>
<span data-ttu-id="00370-106">Erstellt oder aktualisiert eine vorhandene Regel für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="00370-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="00370-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="00370-107">EXAMPLES</span></span>

### <span data-ttu-id="00370-108">Beispiel 1: Erstellen einer Regel für ein virtuelles Netzwerk für eine MariaDB</span><span class="sxs-lookup"><span data-stu-id="00370-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="00370-109">Mit diesem Befehl wird eine virtuelle Netzwerkregel für eine MariaDB erstellt.</span><span class="sxs-lookup"><span data-stu-id="00370-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="00370-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="00370-110">PARAMETERS</span></span>

### <span data-ttu-id="00370-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00370-111">-AsJob</span></span>
<span data-ttu-id="00370-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="00370-112">Run the command as a job</span></span>

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

### <span data-ttu-id="00370-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00370-113">-DefaultProfile</span></span>
<span data-ttu-id="00370-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00370-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00370-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="00370-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="00370-116">Erstellen Sie eine Firewallregel, bevor für das virtuelle Netzwerk der vnet-Dienstendpunkt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="00370-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="00370-117">-Name</span><span class="sxs-lookup"><span data-stu-id="00370-117">-Name</span></span>
<span data-ttu-id="00370-118">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="00370-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="00370-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="00370-119">-NoWait</span></span>
<span data-ttu-id="00370-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="00370-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="00370-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00370-121">-PassThru</span></span>
<span data-ttu-id="00370-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="00370-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="00370-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00370-123">-ResourceGroupName</span></span>
<span data-ttu-id="00370-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="00370-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="00370-125">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="00370-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="00370-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="00370-126">-ServerName</span></span>
<span data-ttu-id="00370-127">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="00370-127">The name of the server.</span></span>

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

### <span data-ttu-id="00370-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="00370-128">-SubnetId</span></span>
<span data-ttu-id="00370-129">Die ARM Ressourcen-ID des Subnetzes des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="00370-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="00370-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00370-130">-SubscriptionId</span></span>
<span data-ttu-id="00370-131">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="00370-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="00370-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="00370-132">-Confirm</span></span>
<span data-ttu-id="00370-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="00370-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00370-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00370-134">-WhatIf</span></span>
<span data-ttu-id="00370-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="00370-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00370-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="00370-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00370-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00370-137">CommonParameters</span></span>
<span data-ttu-id="00370-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00370-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00370-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00370-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00370-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="00370-140">INPUTS</span></span>

## <span data-ttu-id="00370-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="00370-141">OUTPUTS</span></span>

### <span data-ttu-id="00370-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="00370-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="00370-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="00370-143">NOTES</span></span>

<span data-ttu-id="00370-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="00370-144">ALIASES</span></span>

## <span data-ttu-id="00370-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="00370-145">RELATED LINKS</span></span>

