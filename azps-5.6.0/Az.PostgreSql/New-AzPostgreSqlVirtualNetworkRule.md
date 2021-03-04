---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/new-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: 1705b053939d8c5b67666d550c6c8340e892ae45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936688"
---
# <span data-ttu-id="fa440-101">New-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fa440-101">New-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="fa440-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa440-102">SYNOPSIS</span></span>
<span data-ttu-id="fa440-103">Erstellt oder aktualisiert eine vorhandene Regel für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="fa440-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="fa440-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa440-104">SYNTAX</span></span>

```
New-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fa440-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa440-105">DESCRIPTION</span></span>
<span data-ttu-id="fa440-106">Erstellt oder aktualisiert eine vorhandene Regel für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="fa440-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="fa440-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fa440-107">EXAMPLES</span></span>

### <span data-ttu-id="fa440-108">Beispiel 1: Erstellen einer neuen virtuellen Netzwerkregel für postgreSql-Server</span><span class="sxs-lookup"><span data-stu-id="fa440-108">Example 1: Create a new PostgreSql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> New-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="fa440-109">Diese Cmdlets erstellen eine virtuelle Netzwerkregel für postgreSql-Server.</span><span class="sxs-lookup"><span data-stu-id="fa440-109">These cmdlets create a PostgreSql server Virtual Network Rule.</span></span>

## <span data-ttu-id="fa440-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fa440-110">PARAMETERS</span></span>

### <span data-ttu-id="fa440-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa440-111">-AsJob</span></span>
<span data-ttu-id="fa440-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="fa440-112">Run the command as a job</span></span>

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

### <span data-ttu-id="fa440-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa440-113">-DefaultProfile</span></span>
<span data-ttu-id="fa440-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa440-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa440-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa440-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="fa440-116">Erstellen Sie eine Firewallregel, bevor für das virtuelle Netzwerk der vnet-Dienstendpunkt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fa440-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="fa440-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fa440-117">-Name</span></span>
<span data-ttu-id="fa440-118">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="fa440-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="fa440-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fa440-119">-NoWait</span></span>
<span data-ttu-id="fa440-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="fa440-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fa440-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa440-121">-PassThru</span></span>
<span data-ttu-id="fa440-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa440-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fa440-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa440-123">-ResourceGroupName</span></span>
<span data-ttu-id="fa440-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fa440-124">The name of the resource group.</span></span>
<span data-ttu-id="fa440-125">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="fa440-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fa440-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="fa440-126">-ServerName</span></span>
<span data-ttu-id="fa440-127">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="fa440-127">The name of the server.</span></span>

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

### <span data-ttu-id="fa440-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="fa440-128">-SubnetId</span></span>
<span data-ttu-id="fa440-129">Die ARM Ressourcen-ID des Subnetzes des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="fa440-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="fa440-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fa440-130">-SubscriptionId</span></span>
<span data-ttu-id="fa440-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="fa440-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fa440-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fa440-132">-Confirm</span></span>
<span data-ttu-id="fa440-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fa440-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa440-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa440-134">-WhatIf</span></span>
<span data-ttu-id="fa440-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa440-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa440-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa440-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa440-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa440-137">CommonParameters</span></span>
<span data-ttu-id="fa440-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa440-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa440-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa440-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa440-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fa440-140">INPUTS</span></span>

## <span data-ttu-id="fa440-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fa440-141">OUTPUTS</span></span>

### <span data-ttu-id="fa440-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fa440-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="fa440-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fa440-143">NOTES</span></span>

<span data-ttu-id="fa440-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="fa440-144">ALIASES</span></span>

## <span data-ttu-id="fa440-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fa440-145">RELATED LINKS</span></span>

