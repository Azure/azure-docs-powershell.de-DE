---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: c71f8284cc3b1a2648e3523c77f0e9e2dd2d3876
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481962"
---
# <span data-ttu-id="3427b-101">Set-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3427b-101">Set-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="3427b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3427b-102">SYNOPSIS</span></span>
<span data-ttu-id="3427b-103">Ändert die Konfiguration einer virtuellen Azure SQL Server-Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="3427b-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3427b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3427b-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3427b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3427b-105">DESCRIPTION</span></span>
<span data-ttu-id="3427b-106">Mit diesem Befehl wird die Konfiguration einer virtuellen Azure SQL Server-Netzwerkregel geändert.</span><span class="sxs-lookup"><span data-stu-id="3427b-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="3427b-107">Verwenden Sie stattdessen "Add-AzureRmSqlServerVirtualNetworkRule" und "Remove-AzureRmSqlServerVirtualNetworkRule", um den Satz virtueller Netzwerkregeln auf dem Server zu steuern.</span><span class="sxs-lookup"><span data-stu-id="3427b-107">To control the set of virtual network rules in the server, use 'Add-AzureRmSqlServerVirtualNetworkRule' and 'Remove-AzureRmSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="3427b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3427b-108">EXAMPLES</span></span>

### <span data-ttu-id="3427b-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3427b-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="3427b-110">Ändert eine vorhandene virtuelle Netzwerkregel mit der neuen virtuellen Netzwerk-Subnetz-ID, die Informationen zum neuen virtuellen Netzwerk enthält.</span><span class="sxs-lookup"><span data-stu-id="3427b-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="3427b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3427b-111">PARAMETERS</span></span>

### <span data-ttu-id="3427b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3427b-112">-AsJob</span></span>
<span data-ttu-id="3427b-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3427b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3427b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3427b-114">-DefaultProfile</span></span>
<span data-ttu-id="3427b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3427b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3427b-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3427b-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="3427b-117">Erstellen Sie eine Firewallregel, bevor das virtuelle Netzwerk den vnet-Dienstendpunkt aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="3427b-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="3427b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3427b-118">-ResourceGroupName</span></span>
<span data-ttu-id="3427b-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3427b-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="3427b-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="3427b-120">-ServerName</span></span>
<span data-ttu-id="3427b-121">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="3427b-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="3427b-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="3427b-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="3427b-123">Der Name der virtuellen Azure SQL Server-Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="3427b-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="3427b-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="3427b-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="3427b-125">Die Subnetz-ID des virtuellen Netzwerks für die Regel.</span><span class="sxs-lookup"><span data-stu-id="3427b-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="3427b-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3427b-126">-Confirm</span></span>
<span data-ttu-id="3427b-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3427b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3427b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3427b-128">-WhatIf</span></span>
<span data-ttu-id="3427b-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3427b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3427b-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3427b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3427b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3427b-131">CommonParameters</span></span>
<span data-ttu-id="3427b-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3427b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3427b-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3427b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3427b-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3427b-134">INPUTS</span></span>

### <span data-ttu-id="3427b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3427b-135">System.String</span></span>

## <span data-ttu-id="3427b-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3427b-136">OUTPUTS</span></span>

### <span data-ttu-id="3427b-137">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="3427b-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="3427b-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="3427b-138">NOTES</span></span>

## <span data-ttu-id="3427b-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3427b-139">RELATED LINKS</span></span>
