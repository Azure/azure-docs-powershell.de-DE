---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 8667de4551e9fc0c4baf623099f70f778ec8f0a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659083"
---
# <span data-ttu-id="a5f71-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a5f71-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="a5f71-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5f71-102">SYNOPSIS</span></span>
<span data-ttu-id="a5f71-103">Erstellt eine Azure SQL Server-Regel für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a5f71-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="a5f71-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5f71-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5f71-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5f71-105">DESCRIPTION</span></span>
<span data-ttu-id="a5f71-106">Erstellt eine Azure SQL Server-Regel für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a5f71-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="a5f71-107">Es werden virtuelle Netzwerkregeln verwendet, um den Azure SQL Server mit einem bestimmten virtuellen Netzwerk zu verbinden, um den Zugriff auf Azure SQL Server so zu beschränken, dass er nur im virtuellen Netzwerk zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="a5f71-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="a5f71-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5f71-108">EXAMPLES</span></span>

### <span data-ttu-id="a5f71-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a5f71-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="a5f71-110">Erstellt eine virtuelle Azure SQL Server-Netzwerkregel</span><span class="sxs-lookup"><span data-stu-id="a5f71-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="a5f71-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5f71-111">PARAMETERS</span></span>

### <span data-ttu-id="a5f71-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5f71-112">-AsJob</span></span>
<span data-ttu-id="a5f71-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a5f71-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5f71-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5f71-114">-DefaultProfile</span></span>
<span data-ttu-id="a5f71-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a5f71-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f71-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a5f71-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="a5f71-117">Erstellen Sie eine Firewallregel, bevor das virtuelle Netzwerk den vnet-Dienstendpunkt aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="a5f71-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="a5f71-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5f71-118">-ResourceGroupName</span></span>
<span data-ttu-id="a5f71-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a5f71-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5f71-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="a5f71-120">-ServerName</span></span>
<span data-ttu-id="a5f71-121">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="a5f71-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="a5f71-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="a5f71-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="a5f71-123">Azure SQL Server-Regel Name für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="a5f71-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="a5f71-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="a5f71-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="a5f71-125">Die Subnetz-ID des virtuellen Netzwerks, die die Microsoft. Network-Details angibt</span><span class="sxs-lookup"><span data-stu-id="a5f71-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="a5f71-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a5f71-126">-Confirm</span></span>
<span data-ttu-id="a5f71-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5f71-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5f71-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5f71-128">-WhatIf</span></span>
<span data-ttu-id="a5f71-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5f71-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5f71-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5f71-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5f71-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5f71-131">CommonParameters</span></span>
<span data-ttu-id="a5f71-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5f71-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5f71-133">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5f71-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5f71-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5f71-134">INPUTS</span></span>

### <span data-ttu-id="a5f71-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a5f71-135">System.String</span></span>

## <span data-ttu-id="a5f71-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5f71-136">OUTPUTS</span></span>

### <span data-ttu-id="a5f71-137">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="a5f71-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="a5f71-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5f71-138">NOTES</span></span>

## <span data-ttu-id="a5f71-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5f71-139">RELATED LINKS</span></span>
