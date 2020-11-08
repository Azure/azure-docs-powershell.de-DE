---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 77a89dec96e0e9b7ca7bd003f8368274edf6acdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009224"
---
# <span data-ttu-id="c5287-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c5287-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="c5287-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5287-102">SYNOPSIS</span></span>
<span data-ttu-id="c5287-103">Erstellt oder aktualisiert eine vorhandene virtuelle Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="c5287-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="c5287-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5287-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c5287-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5287-105">DESCRIPTION</span></span>
<span data-ttu-id="c5287-106">Erstellt oder aktualisiert eine vorhandene virtuelle Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="c5287-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="c5287-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5287-107">EXAMPLES</span></span>

### <span data-ttu-id="c5287-108">Beispiel 1: Erstellen einer virtuellen Netzwerkregel für eine MariaDB</span><span class="sxs-lookup"><span data-stu-id="c5287-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="c5287-109">Dieser Befehl erstellt eine virtuelle Netzwerkregel für eine MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c5287-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="c5287-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5287-110">PARAMETERS</span></span>

### <span data-ttu-id="c5287-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5287-111">-AsJob</span></span>
<span data-ttu-id="c5287-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="c5287-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c5287-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5287-113">-DefaultProfile</span></span>
<span data-ttu-id="c5287-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c5287-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5287-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5287-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="c5287-116">Erstellen Sie eine Firewallregel, bevor das virtuelle Netzwerk den vnet-Dienstendpunkt aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="c5287-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="c5287-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c5287-117">-Name</span></span>
<span data-ttu-id="c5287-118">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c5287-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="c5287-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c5287-119">-NoWait</span></span>
<span data-ttu-id="c5287-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="c5287-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c5287-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5287-121">-PassThru</span></span>
<span data-ttu-id="c5287-122">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="c5287-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c5287-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5287-123">-ResourceGroupName</span></span>
<span data-ttu-id="c5287-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="c5287-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c5287-125">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="c5287-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c5287-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="c5287-126">-ServerName</span></span>
<span data-ttu-id="c5287-127">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="c5287-127">The name of the server.</span></span>

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

### <span data-ttu-id="c5287-128">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="c5287-128">-SubnetId</span></span>
<span data-ttu-id="c5287-129">Die Arm-Ressourcen-ID des virtuellen Netzwerk-Subnets.</span><span class="sxs-lookup"><span data-stu-id="c5287-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="c5287-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c5287-130">-SubscriptionId</span></span>
<span data-ttu-id="c5287-131">Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c5287-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="c5287-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c5287-132">-Confirm</span></span>
<span data-ttu-id="c5287-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c5287-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5287-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5287-134">-WhatIf</span></span>
<span data-ttu-id="c5287-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c5287-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5287-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5287-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5287-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5287-137">CommonParameters</span></span>
<span data-ttu-id="c5287-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5287-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5287-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5287-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5287-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5287-140">INPUTS</span></span>

## <span data-ttu-id="c5287-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5287-141">OUTPUTS</span></span>

### <span data-ttu-id="c5287-142">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c5287-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="c5287-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5287-143">NOTES</span></span>

<span data-ttu-id="c5287-144">Aliase</span><span class="sxs-lookup"><span data-stu-id="c5287-144">ALIASES</span></span>

## <span data-ttu-id="c5287-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5287-145">RELATED LINKS</span></span>

