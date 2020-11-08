---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 3b660f5db14e1197c1e262a10f8225e4e9a82b81
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008378"
---
# <span data-ttu-id="64a25-101">New-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="64a25-101">New-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="64a25-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64a25-102">SYNOPSIS</span></span>
<span data-ttu-id="64a25-103">Erstellt oder aktualisiert eine vorhandene virtuelle Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="64a25-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="64a25-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64a25-104">SYNTAX</span></span>

```
New-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64a25-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64a25-105">DESCRIPTION</span></span>
<span data-ttu-id="64a25-106">Erstellt oder aktualisiert eine vorhandene virtuelle Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="64a25-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="64a25-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64a25-107">EXAMPLES</span></span>

### <span data-ttu-id="64a25-108">Beispiel 1: Erstellen einer neuen virtuellen MySQL Server-Netzwerkregel</span><span class="sxs-lookup"><span data-stu-id="64a25-108">Example 1: Create a new MySql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> New-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="64a25-109">Mit diesen Cmdlets wird eine MySQL Server-Regel für virtuelles Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="64a25-109">These cmdlets create a MySql server Virtual Network Rule.</span></span>

## <span data-ttu-id="64a25-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="64a25-110">PARAMETERS</span></span>

### <span data-ttu-id="64a25-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64a25-111">-AsJob</span></span>
<span data-ttu-id="64a25-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="64a25-112">Run the command as a job</span></span>

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

### <span data-ttu-id="64a25-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a25-113">-DefaultProfile</span></span>
<span data-ttu-id="64a25-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="64a25-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64a25-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="64a25-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="64a25-116">Erstellen Sie eine Firewallregel, bevor das virtuelle Netzwerk den vnet-Dienstendpunkt aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="64a25-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="64a25-117">-Name</span><span class="sxs-lookup"><span data-stu-id="64a25-117">-Name</span></span>
<span data-ttu-id="64a25-118">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="64a25-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="64a25-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="64a25-119">-NoWait</span></span>
<span data-ttu-id="64a25-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="64a25-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="64a25-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64a25-121">-PassThru</span></span>
<span data-ttu-id="64a25-122">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="64a25-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="64a25-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64a25-123">-ResourceGroupName</span></span>
<span data-ttu-id="64a25-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="64a25-124">The name of the resource group.</span></span>
<span data-ttu-id="64a25-125">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="64a25-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="64a25-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="64a25-126">-ServerName</span></span>
<span data-ttu-id="64a25-127">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="64a25-127">The name of the server.</span></span>

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

### <span data-ttu-id="64a25-128">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="64a25-128">-SubnetId</span></span>
<span data-ttu-id="64a25-129">Die Arm-Ressourcen-ID des virtuellen Netzwerk-Subnets.</span><span class="sxs-lookup"><span data-stu-id="64a25-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="64a25-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="64a25-130">-SubscriptionId</span></span>
<span data-ttu-id="64a25-131">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="64a25-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="64a25-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="64a25-132">-Confirm</span></span>
<span data-ttu-id="64a25-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="64a25-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64a25-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64a25-134">-WhatIf</span></span>
<span data-ttu-id="64a25-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64a25-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64a25-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64a25-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64a25-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a25-137">CommonParameters</span></span>
<span data-ttu-id="64a25-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a25-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a25-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64a25-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a25-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64a25-140">INPUTS</span></span>

## <span data-ttu-id="64a25-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64a25-141">OUTPUTS</span></span>

### <span data-ttu-id="64a25-142">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="64a25-142">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="64a25-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="64a25-143">NOTES</span></span>

<span data-ttu-id="64a25-144">Aliase</span><span class="sxs-lookup"><span data-stu-id="64a25-144">ALIASES</span></span>

## <span data-ttu-id="64a25-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64a25-145">RELATED LINKS</span></span>

