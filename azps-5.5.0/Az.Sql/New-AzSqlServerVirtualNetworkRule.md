---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 64fc7b3acdc497759b707f024a0fb14c7017c44c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163329"
---
# <span data-ttu-id="a6836-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a6836-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="a6836-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6836-102">SYNOPSIS</span></span>
<span data-ttu-id="a6836-103">Erstellt eine Azure SQL Server Virtuelle Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="a6836-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="a6836-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6836-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6836-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6836-105">DESCRIPTION</span></span>
<span data-ttu-id="a6836-106">Erstellt eine Azure SQL Server Virtuelle Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="a6836-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="a6836-107">Regeln für virtuelle Netzwerke werden verwendet, um azure SQL Server mit einem bestimmten virtuellen Netzwerk zu verbinden, um den Zugriff auf azure SQL Server auf die ausschließliche Bereitstellung innerhalb des virtuellen Netzwerks zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="a6836-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="a6836-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a6836-108">EXAMPLES</span></span>

### <span data-ttu-id="a6836-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a6836-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="a6836-110">Erstellt eine Azure SQL Server virtuelle Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="a6836-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="a6836-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6836-111">PARAMETERS</span></span>

### <span data-ttu-id="a6836-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6836-112">-AsJob</span></span>
<span data-ttu-id="a6836-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a6836-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6836-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6836-114">-DefaultProfile</span></span>
<span data-ttu-id="a6836-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a6836-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6836-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6836-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="a6836-117">Erstellen Sie eine Firewallregel, bevor der vnetdienstendpunkt im virtuellen Netzwerk aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a6836-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="a6836-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6836-118">-ResourceGroupName</span></span>
<span data-ttu-id="a6836-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a6836-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="a6836-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a6836-120">-ServerName</span></span>
<span data-ttu-id="a6836-121">Der Azure Sql Server-Name.</span><span class="sxs-lookup"><span data-stu-id="a6836-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="a6836-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="a6836-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="a6836-123">Name der virtuellen Azure Sql Server-Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="a6836-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="a6836-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="a6836-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="a6836-125">Die Subnetz-ID des virtuellen Netzwerks, die die Microsoft.Network-Details angibt</span><span class="sxs-lookup"><span data-stu-id="a6836-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="a6836-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6836-126">-Confirm</span></span>
<span data-ttu-id="a6836-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6836-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6836-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a6836-128">-WhatIf</span></span>
<span data-ttu-id="a6836-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6836-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6836-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6836-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6836-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6836-131">CommonParameters</span></span>
<span data-ttu-id="a6836-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6836-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6836-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6836-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6836-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a6836-134">INPUTS</span></span>

### <span data-ttu-id="a6836-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a6836-135">System.String</span></span>

## <span data-ttu-id="a6836-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a6836-136">OUTPUTS</span></span>

### <span data-ttu-id="a6836-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="a6836-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="a6836-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a6836-138">NOTES</span></span>

## <span data-ttu-id="a6836-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a6836-139">RELATED LINKS</span></span>
