---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: f617f853a8e9106ecb2d1268dfbe4e46a22efb45
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165053"
---
# <span data-ttu-id="ed870-101">New-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ed870-101">New-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="ed870-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed870-102">SYNOPSIS</span></span>
<span data-ttu-id="ed870-103">Erstellt oder aktualisiert eine vorhandene virtuelle Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="ed870-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="ed870-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed870-104">SYNTAX</span></span>

```
New-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ed870-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed870-105">DESCRIPTION</span></span>
<span data-ttu-id="ed870-106">Erstellt oder aktualisiert eine vorhandene virtuelle Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="ed870-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="ed870-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed870-107">EXAMPLES</span></span>

### <span data-ttu-id="ed870-108">Beispiel 1: Erstellen einer neuen virtuellen Netzwerkregel für den PostgreSQL-Server</span><span class="sxs-lookup"><span data-stu-id="ed870-108">Example 1: Create a new PostgreSql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> New-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="ed870-109">Mit diesen Cmdlets wird eine virtuelle PostgreSQL-Server-Netzwerkregel erstellt.</span><span class="sxs-lookup"><span data-stu-id="ed870-109">These cmdlets create a PostgreSql server Virtual Network Rule.</span></span>

## <span data-ttu-id="ed870-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed870-110">PARAMETERS</span></span>

### <span data-ttu-id="ed870-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed870-111">-AsJob</span></span>
<span data-ttu-id="ed870-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="ed870-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ed870-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed870-113">-DefaultProfile</span></span>
<span data-ttu-id="ed870-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed870-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed870-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed870-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="ed870-116">Erstellen Sie eine Firewallregel, bevor das virtuelle Netzwerk den vnet-Dienstendpunkt aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="ed870-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="ed870-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ed870-117">-Name</span></span>
<span data-ttu-id="ed870-118">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="ed870-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="ed870-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ed870-119">-NoWait</span></span>
<span data-ttu-id="ed870-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="ed870-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ed870-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed870-121">-PassThru</span></span>
<span data-ttu-id="ed870-122">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="ed870-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ed870-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed870-123">-ResourceGroupName</span></span>
<span data-ttu-id="ed870-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ed870-124">The name of the resource group.</span></span>
<span data-ttu-id="ed870-125">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="ed870-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ed870-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="ed870-126">-ServerName</span></span>
<span data-ttu-id="ed870-127">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="ed870-127">The name of the server.</span></span>

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

### <span data-ttu-id="ed870-128">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="ed870-128">-SubnetId</span></span>
<span data-ttu-id="ed870-129">Die Arm-Ressourcen-ID des virtuellen Netzwerk-Subnets.</span><span class="sxs-lookup"><span data-stu-id="ed870-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="ed870-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="ed870-130">-SubscriptionId</span></span>
<span data-ttu-id="ed870-131">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="ed870-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ed870-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ed870-132">-Confirm</span></span>
<span data-ttu-id="ed870-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed870-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed870-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed870-134">-WhatIf</span></span>
<span data-ttu-id="ed870-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed870-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed870-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed870-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed870-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed870-137">CommonParameters</span></span>
<span data-ttu-id="ed870-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed870-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed870-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed870-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed870-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed870-140">INPUTS</span></span>

## <span data-ttu-id="ed870-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed870-141">OUTPUTS</span></span>

### <span data-ttu-id="ed870-142">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ed870-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="ed870-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed870-143">NOTES</span></span>

<span data-ttu-id="ed870-144">Aliase</span><span class="sxs-lookup"><span data-stu-id="ed870-144">ALIASES</span></span>

## <span data-ttu-id="ed870-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed870-145">RELATED LINKS</span></span>

