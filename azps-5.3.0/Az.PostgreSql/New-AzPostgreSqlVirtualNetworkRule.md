---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: f617f853a8e9106ecb2d1268dfbe4e46a22efb45
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384514"
---
# <span data-ttu-id="e6d66-101">New-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e6d66-101">New-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="e6d66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6d66-102">SYNOPSIS</span></span>
<span data-ttu-id="e6d66-103">Erstellt oder aktualisiert eine vorhandene Regel für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e6d66-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="e6d66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6d66-104">SYNTAX</span></span>

```
New-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e6d66-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6d66-105">DESCRIPTION</span></span>
<span data-ttu-id="e6d66-106">Erstellt oder aktualisiert eine vorhandene Regel für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e6d66-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="e6d66-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e6d66-107">EXAMPLES</span></span>

### <span data-ttu-id="e6d66-108">Beispiel 1: Erstellen einer neuen virtuellen Netzwerkregel für den PostgreSql-Server</span><span class="sxs-lookup"><span data-stu-id="e6d66-108">Example 1: Create a new PostgreSql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> New-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="e6d66-109">Diese Cmdlets erstellen eine virtuelle Netzwerkregel für den PostgreSql-Server.</span><span class="sxs-lookup"><span data-stu-id="e6d66-109">These cmdlets create a PostgreSql server Virtual Network Rule.</span></span>

## <span data-ttu-id="e6d66-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6d66-110">PARAMETERS</span></span>

### <span data-ttu-id="e6d66-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6d66-111">-AsJob</span></span>
<span data-ttu-id="e6d66-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="e6d66-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e6d66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6d66-113">-DefaultProfile</span></span>
<span data-ttu-id="e6d66-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6d66-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6d66-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6d66-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="e6d66-116">Erstellen Sie eine Firewallregel, bevor der vnet-Dienstendpunkt im virtuellen Netzwerk aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e6d66-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="e6d66-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e6d66-117">-Name</span></span>
<span data-ttu-id="e6d66-118">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e6d66-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="e6d66-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e6d66-119">-NoWait</span></span>
<span data-ttu-id="e6d66-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="e6d66-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e6d66-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6d66-121">-PassThru</span></span>
<span data-ttu-id="e6d66-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="e6d66-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e6d66-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6d66-123">-ResourceGroupName</span></span>
<span data-ttu-id="e6d66-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e6d66-124">The name of the resource group.</span></span>
<span data-ttu-id="e6d66-125">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="e6d66-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e6d66-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e6d66-126">-ServerName</span></span>
<span data-ttu-id="e6d66-127">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="e6d66-127">The name of the server.</span></span>

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

### <span data-ttu-id="e6d66-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e6d66-128">-SubnetId</span></span>
<span data-ttu-id="e6d66-129">Die ARM Ressourcen-ID des virtuellen Netzwerk-Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="e6d66-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="e6d66-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6d66-130">-SubscriptionId</span></span>
<span data-ttu-id="e6d66-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="e6d66-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e6d66-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6d66-132">-Confirm</span></span>
<span data-ttu-id="e6d66-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e6d66-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6d66-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e6d66-134">-WhatIf</span></span>
<span data-ttu-id="e6d66-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e6d66-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6d66-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6d66-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6d66-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6d66-137">CommonParameters</span></span>
<span data-ttu-id="e6d66-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6d66-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6d66-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6d66-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6d66-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e6d66-140">INPUTS</span></span>

## <span data-ttu-id="e6d66-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e6d66-141">OUTPUTS</span></span>

### <span data-ttu-id="e6d66-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e6d66-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="e6d66-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e6d66-143">NOTES</span></span>

<span data-ttu-id="e6d66-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e6d66-144">ALIASES</span></span>

## <span data-ttu-id="e6d66-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e6d66-145">RELATED LINKS</span></span>

