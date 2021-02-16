---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: f617f853a8e9106ecb2d1268dfbe4e46a22efb45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160348"
---
# <span data-ttu-id="4433c-101">New-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4433c-101">New-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="4433c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4433c-102">SYNOPSIS</span></span>
<span data-ttu-id="4433c-103">Erstellt oder aktualisiert eine vorhandene Regel für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="4433c-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="4433c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4433c-104">SYNTAX</span></span>

```
New-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4433c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4433c-105">DESCRIPTION</span></span>
<span data-ttu-id="4433c-106">Erstellt oder aktualisiert eine vorhandene Regel für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="4433c-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="4433c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4433c-107">EXAMPLES</span></span>

### <span data-ttu-id="4433c-108">Beispiel 1: Erstellen einer neuen virtuellen Netzwerkregel für den PostgreSqlserver</span><span class="sxs-lookup"><span data-stu-id="4433c-108">Example 1: Create a new PostgreSql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> New-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="4433c-109">Diese Cmdlets erstellen eine virtuelle Netzwerkregel für den PostgreSql-Server.</span><span class="sxs-lookup"><span data-stu-id="4433c-109">These cmdlets create a PostgreSql server Virtual Network Rule.</span></span>

## <span data-ttu-id="4433c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4433c-110">PARAMETERS</span></span>

### <span data-ttu-id="4433c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4433c-111">-AsJob</span></span>
<span data-ttu-id="4433c-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="4433c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="4433c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4433c-113">-DefaultProfile</span></span>
<span data-ttu-id="4433c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4433c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4433c-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4433c-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="4433c-116">Erstellen Sie eine Firewallregel, bevor der vnetdienstendpunkt im virtuellen Netzwerk aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4433c-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="4433c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4433c-117">-Name</span></span>
<span data-ttu-id="4433c-118">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="4433c-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="4433c-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4433c-119">-NoWait</span></span>
<span data-ttu-id="4433c-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="4433c-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4433c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4433c-121">-PassThru</span></span>
<span data-ttu-id="4433c-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="4433c-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4433c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4433c-123">-ResourceGroupName</span></span>
<span data-ttu-id="4433c-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4433c-124">The name of the resource group.</span></span>
<span data-ttu-id="4433c-125">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="4433c-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4433c-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4433c-126">-ServerName</span></span>
<span data-ttu-id="4433c-127">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="4433c-127">The name of the server.</span></span>

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

### <span data-ttu-id="4433c-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4433c-128">-SubnetId</span></span>
<span data-ttu-id="4433c-129">Die ARM Ressourcen-ID des virtuellen Netzwerk-Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="4433c-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="4433c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4433c-130">-SubscriptionId</span></span>
<span data-ttu-id="4433c-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="4433c-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4433c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4433c-132">-Confirm</span></span>
<span data-ttu-id="4433c-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4433c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4433c-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4433c-134">-WhatIf</span></span>
<span data-ttu-id="4433c-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4433c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4433c-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4433c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4433c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4433c-137">CommonParameters</span></span>
<span data-ttu-id="4433c-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4433c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4433c-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4433c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4433c-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4433c-140">INPUTS</span></span>

## <span data-ttu-id="4433c-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4433c-141">OUTPUTS</span></span>

### <span data-ttu-id="4433c-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4433c-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="4433c-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4433c-143">NOTES</span></span>

<span data-ttu-id="4433c-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="4433c-144">ALIASES</span></span>

## <span data-ttu-id="4433c-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4433c-145">RELATED LINKS</span></span>

