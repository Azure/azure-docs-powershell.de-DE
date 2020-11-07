---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 64fc7b3acdc497759b707f024a0fb14c7017c44c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847376"
---
# <span data-ttu-id="f3072-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f3072-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="f3072-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3072-102">SYNOPSIS</span></span>
<span data-ttu-id="f3072-103">Erstellt eine Azure SQL Server-Regel für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f3072-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="f3072-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3072-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3072-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3072-105">DESCRIPTION</span></span>
<span data-ttu-id="f3072-106">Erstellt eine Azure SQL Server-Regel für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f3072-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="f3072-107">Es werden virtuelle Netzwerkregeln verwendet, um den Azure SQL Server mit einem bestimmten virtuellen Netzwerk zu verbinden, um den Zugriff auf Azure SQL Server so zu beschränken, dass er nur im virtuellen Netzwerk zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="f3072-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="f3072-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3072-108">EXAMPLES</span></span>

### <span data-ttu-id="f3072-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f3072-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="f3072-110">Erstellt eine virtuelle Azure SQL Server-Netzwerkregel</span><span class="sxs-lookup"><span data-stu-id="f3072-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="f3072-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3072-111">PARAMETERS</span></span>

### <span data-ttu-id="f3072-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3072-112">-AsJob</span></span>
<span data-ttu-id="f3072-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f3072-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3072-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3072-114">-DefaultProfile</span></span>
<span data-ttu-id="f3072-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f3072-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3072-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f3072-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="f3072-117">Erstellen Sie eine Firewallregel, bevor das virtuelle Netzwerk den vnet-Dienstendpunkt aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="f3072-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="f3072-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3072-118">-ResourceGroupName</span></span>
<span data-ttu-id="f3072-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f3072-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="f3072-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="f3072-120">-ServerName</span></span>
<span data-ttu-id="f3072-121">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="f3072-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="f3072-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="f3072-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="f3072-123">Azure SQL Server-Regel Name für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="f3072-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="f3072-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="f3072-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="f3072-125">Die Subnetz-ID des virtuellen Netzwerks, die die Microsoft. Network-Details angibt</span><span class="sxs-lookup"><span data-stu-id="f3072-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="f3072-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f3072-126">-Confirm</span></span>
<span data-ttu-id="f3072-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f3072-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3072-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3072-128">-WhatIf</span></span>
<span data-ttu-id="f3072-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f3072-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3072-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3072-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3072-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3072-131">CommonParameters</span></span>
<span data-ttu-id="f3072-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3072-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3072-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3072-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3072-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3072-134">INPUTS</span></span>

### <span data-ttu-id="f3072-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f3072-135">System.String</span></span>

## <span data-ttu-id="f3072-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3072-136">OUTPUTS</span></span>

### <span data-ttu-id="f3072-137">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="f3072-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="f3072-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3072-138">NOTES</span></span>

## <span data-ttu-id="f3072-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3072-139">RELATED LINKS</span></span>
