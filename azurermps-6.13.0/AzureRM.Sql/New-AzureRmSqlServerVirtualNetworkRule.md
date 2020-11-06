---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: c2e3386d7c9146eeaa96220ddcbea4cf50864e10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477641"
---
# <span data-ttu-id="55afd-101">New-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="55afd-101">New-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="55afd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="55afd-102">SYNOPSIS</span></span>
<span data-ttu-id="55afd-103">Erstellt eine Azure SQL Server-Regel für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="55afd-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55afd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="55afd-104">SYNTAX</span></span>

```
New-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55afd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55afd-105">DESCRIPTION</span></span>
<span data-ttu-id="55afd-106">Erstellt eine Azure SQL Server-Regel für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="55afd-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="55afd-107">Es werden virtuelle Netzwerkregeln verwendet, um den Azure SQL Server mit einem bestimmten virtuellen Netzwerk zu verbinden, um den Zugriff auf Azure SQL Server so zu beschränken, dass er nur im virtuellen Netzwerk zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="55afd-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="55afd-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55afd-108">EXAMPLES</span></span>

### <span data-ttu-id="55afd-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="55afd-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="55afd-110">Erstellt eine virtuelle Azure SQL Server-Netzwerkregel</span><span class="sxs-lookup"><span data-stu-id="55afd-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="55afd-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="55afd-111">PARAMETERS</span></span>

### <span data-ttu-id="55afd-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55afd-112">-AsJob</span></span>
<span data-ttu-id="55afd-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="55afd-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55afd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55afd-114">-DefaultProfile</span></span>
<span data-ttu-id="55afd-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="55afd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55afd-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="55afd-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="55afd-117">Erstellen Sie eine Firewallregel, bevor das virtuelle Netzwerk den vnet-Dienstendpunkt aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="55afd-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="55afd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55afd-118">-ResourceGroupName</span></span>
<span data-ttu-id="55afd-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="55afd-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="55afd-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="55afd-120">-ServerName</span></span>
<span data-ttu-id="55afd-121">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="55afd-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="55afd-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="55afd-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="55afd-123">Azure SQL Server-Regel Name für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="55afd-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="55afd-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="55afd-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="55afd-125">Die Subnetz-ID des virtuellen Netzwerks, die die Microsoft. Network-Details angibt</span><span class="sxs-lookup"><span data-stu-id="55afd-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="55afd-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="55afd-126">-Confirm</span></span>
<span data-ttu-id="55afd-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55afd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55afd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55afd-128">-WhatIf</span></span>
<span data-ttu-id="55afd-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55afd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55afd-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55afd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55afd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55afd-131">CommonParameters</span></span>
<span data-ttu-id="55afd-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55afd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55afd-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55afd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55afd-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="55afd-134">INPUTS</span></span>

### <span data-ttu-id="55afd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="55afd-135">System.String</span></span>

## <span data-ttu-id="55afd-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="55afd-136">OUTPUTS</span></span>

### <span data-ttu-id="55afd-137">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="55afd-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="55afd-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="55afd-138">NOTES</span></span>

## <span data-ttu-id="55afd-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="55afd-139">RELATED LINKS</span></span>
