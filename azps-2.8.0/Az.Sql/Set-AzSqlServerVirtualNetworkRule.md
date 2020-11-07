---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 3b318e08e4dbf900b54581b18f551a3accb75480
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826143"
---
# <span data-ttu-id="41f06-101">Set-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="41f06-101">Set-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="41f06-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="41f06-102">SYNOPSIS</span></span>
<span data-ttu-id="41f06-103">Ändert die Konfiguration einer virtuellen Azure SQL Server-Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="41f06-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="41f06-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="41f06-104">SYNTAX</span></span>

```
Set-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41f06-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41f06-105">DESCRIPTION</span></span>
<span data-ttu-id="41f06-106">Mit diesem Befehl wird die Konfiguration einer virtuellen Azure SQL Server-Netzwerkregel geändert.</span><span class="sxs-lookup"><span data-stu-id="41f06-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="41f06-107">Verwenden Sie stattdessen "Add-AzSqlServerVirtualNetworkRule" und "Remove-AzSqlServerVirtualNetworkRule", um den Satz virtueller Netzwerkregeln auf dem Server zu steuern.</span><span class="sxs-lookup"><span data-stu-id="41f06-107">To control the set of virtual network rules in the server, use 'Add-AzSqlServerVirtualNetworkRule' and 'Remove-AzSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="41f06-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="41f06-108">EXAMPLES</span></span>

### <span data-ttu-id="41f06-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="41f06-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="41f06-110">Ändert eine vorhandene virtuelle Netzwerkregel mit der neuen virtuellen Netzwerk-Subnetz-ID, die Informationen zum neuen virtuellen Netzwerk enthält.</span><span class="sxs-lookup"><span data-stu-id="41f06-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="41f06-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="41f06-111">PARAMETERS</span></span>

### <span data-ttu-id="41f06-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41f06-112">-AsJob</span></span>
<span data-ttu-id="41f06-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="41f06-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41f06-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41f06-114">-DefaultProfile</span></span>
<span data-ttu-id="41f06-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="41f06-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41f06-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="41f06-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="41f06-117">Erstellen Sie eine Firewallregel, bevor das virtuelle Netzwerk den vnet-Dienstendpunkt aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="41f06-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="41f06-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41f06-118">-ResourceGroupName</span></span>
<span data-ttu-id="41f06-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="41f06-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="41f06-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="41f06-120">-ServerName</span></span>
<span data-ttu-id="41f06-121">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="41f06-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="41f06-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="41f06-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="41f06-123">Der Name der virtuellen Azure SQL Server-Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="41f06-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="41f06-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="41f06-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="41f06-125">Die Subnetz-ID des virtuellen Netzwerks für die Regel.</span><span class="sxs-lookup"><span data-stu-id="41f06-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="41f06-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="41f06-126">-Confirm</span></span>
<span data-ttu-id="41f06-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="41f06-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41f06-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41f06-128">-WhatIf</span></span>
<span data-ttu-id="41f06-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41f06-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41f06-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41f06-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41f06-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f06-131">CommonParameters</span></span>
<span data-ttu-id="41f06-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41f06-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41f06-133">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41f06-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f06-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="41f06-134">INPUTS</span></span>

### <span data-ttu-id="41f06-135">System. String</span><span class="sxs-lookup"><span data-stu-id="41f06-135">System.String</span></span>

## <span data-ttu-id="41f06-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="41f06-136">OUTPUTS</span></span>

### <span data-ttu-id="41f06-137">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="41f06-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="41f06-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="41f06-138">NOTES</span></span>

## <span data-ttu-id="41f06-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="41f06-139">RELATED LINKS</span></span>
