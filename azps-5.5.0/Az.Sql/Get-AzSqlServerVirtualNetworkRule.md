---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f8ac34526691f3bdacdd0736189e063c969f63ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145676"
---
# <span data-ttu-id="0a237-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0a237-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="0a237-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a237-102">SYNOPSIS</span></span>
<span data-ttu-id="0a237-103">Ruft Azure SQL Server virtuelle Netzwerkregel ab oder listet diese auf.</span><span class="sxs-lookup"><span data-stu-id="0a237-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="0a237-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a237-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a237-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a237-105">DESCRIPTION</span></span>
<span data-ttu-id="0a237-106">Dieser Befehl ruft eine bestimmte Azure SQL Server Virtuelle Netzwerkregel oder eine Liste der Azure SQL Server Virtuellen Netzwerkregeln unter einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="0a237-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="0a237-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0a237-107">EXAMPLES</span></span>

### <span data-ttu-id="0a237-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0a237-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="0a237-109">Ruft eine einzelne Azure SQL Server virtuelle Netzwerkregel ab</span><span class="sxs-lookup"><span data-stu-id="0a237-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="0a237-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0a237-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="0a237-111">Ruft die Liste der Azure SQL Server virtuellen Netzwerkregeln unter dem angegebenen Server ab.</span><span class="sxs-lookup"><span data-stu-id="0a237-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="0a237-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0a237-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="0a237-113">Ruft die Liste der Azure SQL Server virtuellen Netzwerkregeln unter dem angegebenen Server ab, die mit "virtualNetworkRule" beginnen.</span><span class="sxs-lookup"><span data-stu-id="0a237-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="0a237-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a237-114">PARAMETERS</span></span>

### <span data-ttu-id="0a237-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a237-115">-DefaultProfile</span></span>
<span data-ttu-id="0a237-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0a237-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a237-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a237-117">-ResourceGroupName</span></span>
<span data-ttu-id="0a237-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0a237-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="0a237-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0a237-119">-ServerName</span></span>
<span data-ttu-id="0a237-120">Der Azure Sql Server-Name.</span><span class="sxs-lookup"><span data-stu-id="0a237-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="0a237-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="0a237-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="0a237-122">Der Name der virtuellen Azure Sql Server-Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="0a237-122">The Azure Sql Server Virtual Network Rule name.</span></span>

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

### <span data-ttu-id="0a237-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a237-123">CommonParameters</span></span>
<span data-ttu-id="0a237-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a237-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a237-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a237-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a237-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0a237-126">INPUTS</span></span>

### <span data-ttu-id="0a237-127">System.String</span><span class="sxs-lookup"><span data-stu-id="0a237-127">System.String</span></span>

## <span data-ttu-id="0a237-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0a237-128">OUTPUTS</span></span>

### <span data-ttu-id="0a237-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="0a237-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="0a237-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0a237-130">NOTES</span></span>

## <span data-ttu-id="0a237-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0a237-131">RELATED LINKS</span></span>
