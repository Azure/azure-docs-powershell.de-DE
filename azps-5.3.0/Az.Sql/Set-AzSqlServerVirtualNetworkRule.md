---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 55321b384a24e18a962b99cc40161eabbeb00160
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468396"
---
# <span data-ttu-id="8b4cf-101">Set-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8b4cf-101">Set-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="8b4cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b4cf-102">SYNOPSIS</span></span>
<span data-ttu-id="8b4cf-103">Ändert die Konfiguration einer Azure SQL Server Virtuelle Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="8b4cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b4cf-104">SYNTAX</span></span>

```
Set-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b4cf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b4cf-105">DESCRIPTION</span></span>
<span data-ttu-id="8b4cf-106">Mit diesem Befehl wird die Konfiguration einer Azure SQL Server Virtuelle Netzwerkregel geändert.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="8b4cf-107">Verwenden Sie stattdessen "Add-AzSqlServerVirtualNetworkRule" und "Remove-AzSqlServerVirtualNetworkRule", um den Satz virtueller Netzwerkregeln auf dem Server zu steuern.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-107">To control the set of virtual network rules in the server, use 'Add-AzSqlServerVirtualNetworkRule' and 'Remove-AzSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="8b4cf-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8b4cf-108">EXAMPLES</span></span>

### <span data-ttu-id="8b4cf-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8b4cf-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="8b4cf-110">Ändert eine vorhandene Regel für ein virtuelles Netzwerk mit der neuen Subnetz-ID des virtuellen Netzwerks, die Informationen zum neuen virtuellen Netzwerk enthält.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="8b4cf-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b4cf-111">PARAMETERS</span></span>

### <span data-ttu-id="8b4cf-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b4cf-112">-AsJob</span></span>
<span data-ttu-id="8b4cf-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8b4cf-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b4cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b4cf-114">-DefaultProfile</span></span>
<span data-ttu-id="8b4cf-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8b4cf-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b4cf-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="8b4cf-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="8b4cf-117">Erstellen Sie eine Firewallregel, bevor der vnet-Dienstendpunkt im virtuellen Netzwerk aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="8b4cf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b4cf-118">-ResourceGroupName</span></span>
<span data-ttu-id="8b4cf-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="8b4cf-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8b4cf-120">-ServerName</span></span>
<span data-ttu-id="8b4cf-121">Der Azure Sql Server-Name.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="8b4cf-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="8b4cf-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="8b4cf-123">Der Name der virtuellen Azure Sql Server-Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="8b4cf-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="8b4cf-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="8b4cf-125">Die Subnetz-ID des virtuellen Netzwerks für die Regel.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="8b4cf-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b4cf-126">-Confirm</span></span>
<span data-ttu-id="8b4cf-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b4cf-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8b4cf-128">-WhatIf</span></span>
<span data-ttu-id="8b4cf-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b4cf-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b4cf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b4cf-131">CommonParameters</span></span>
<span data-ttu-id="8b4cf-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b4cf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b4cf-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b4cf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b4cf-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8b4cf-134">INPUTS</span></span>

### <span data-ttu-id="8b4cf-135">System.String</span><span class="sxs-lookup"><span data-stu-id="8b4cf-135">System.String</span></span>

## <span data-ttu-id="8b4cf-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8b4cf-136">OUTPUTS</span></span>

### <span data-ttu-id="8b4cf-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="8b4cf-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="8b4cf-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8b4cf-138">NOTES</span></span>

## <span data-ttu-id="8b4cf-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8b4cf-139">RELATED LINKS</span></span>
