---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 766a5bb6777d1c1ef1e077d4345b7034ede82599
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940960"
---
# <span data-ttu-id="3ce76-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3ce76-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="3ce76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ce76-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce76-103">Löscht eine Azure SQL Server Virtual Network Rule.</span><span class="sxs-lookup"><span data-stu-id="3ce76-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="3ce76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ce76-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ce76-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ce76-105">DESCRIPTION</span></span>
<span data-ttu-id="3ce76-106">Mit diesem Befehl wird eine Azure SQL Server Virtuelle Netzwerkregel gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3ce76-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="3ce76-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3ce76-107">EXAMPLES</span></span>

### <span data-ttu-id="3ce76-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3ce76-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="3ce76-109">Löscht eine vorhandene Azure SQL Server Regel für virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="3ce76-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="3ce76-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3ce76-110">PARAMETERS</span></span>

### <span data-ttu-id="3ce76-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ce76-111">-AsJob</span></span>
<span data-ttu-id="3ce76-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3ce76-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ce76-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce76-113">-DefaultProfile</span></span>
<span data-ttu-id="3ce76-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3ce76-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ce76-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ce76-115">-ResourceGroupName</span></span>
<span data-ttu-id="3ce76-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3ce76-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="3ce76-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="3ce76-117">-ServerName</span></span>
<span data-ttu-id="3ce76-118">Der Azure Sql Server-Name.</span><span class="sxs-lookup"><span data-stu-id="3ce76-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="3ce76-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="3ce76-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="3ce76-120">Name der Azure Sql Server Virtual Network Rule</span><span class="sxs-lookup"><span data-stu-id="3ce76-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="3ce76-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3ce76-121">-Confirm</span></span>
<span data-ttu-id="3ce76-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3ce76-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ce76-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ce76-123">-WhatIf</span></span>
<span data-ttu-id="3ce76-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ce76-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ce76-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ce76-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ce76-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce76-126">CommonParameters</span></span>
<span data-ttu-id="3ce76-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ce76-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce76-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ce76-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce76-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3ce76-129">INPUTS</span></span>

### <span data-ttu-id="3ce76-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3ce76-130">System.String</span></span>

## <span data-ttu-id="3ce76-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3ce76-131">OUTPUTS</span></span>

### <span data-ttu-id="3ce76-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="3ce76-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="3ce76-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3ce76-133">NOTES</span></span>

## <span data-ttu-id="3ce76-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3ce76-134">RELATED LINKS</span></span>
