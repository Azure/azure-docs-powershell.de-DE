---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f8ac34526691f3bdacdd0736189e063c969f63ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008869"
---
# <span data-ttu-id="15a70-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="15a70-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="15a70-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15a70-102">SYNOPSIS</span></span>
<span data-ttu-id="15a70-103">Ruft die virtuelle Azure SQL Server-Netzwerkregel ab oder listet Sie auf.</span><span class="sxs-lookup"><span data-stu-id="15a70-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="15a70-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15a70-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15a70-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15a70-105">DESCRIPTION</span></span>
<span data-ttu-id="15a70-106">Dieser Befehl ruft eine bestimmte Azure SQL Server-Regel für virtuelles Netzwerk oder eine Liste von virtuellen Azure SQL Server-Netzwerkregeln unter einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="15a70-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="15a70-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15a70-107">EXAMPLES</span></span>

### <span data-ttu-id="15a70-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="15a70-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="15a70-109">Ruft eine einzelne Azure SQL Server-Regel für virtuelles Netzwerk ab</span><span class="sxs-lookup"><span data-stu-id="15a70-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="15a70-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="15a70-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="15a70-111">Ruft die Liste der virtuellen Azure SQL Server-Netzwerkregeln unter dem angegebenen Server ab.</span><span class="sxs-lookup"><span data-stu-id="15a70-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="15a70-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="15a70-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="15a70-113">Ruft die Liste der virtuellen Azure SQL Server-Netzwerkregeln unter dem angegebenen Server ab, die mit "virtualNetworkRule" beginnen.</span><span class="sxs-lookup"><span data-stu-id="15a70-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="15a70-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="15a70-114">PARAMETERS</span></span>

### <span data-ttu-id="15a70-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a70-115">-DefaultProfile</span></span>
<span data-ttu-id="15a70-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="15a70-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15a70-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a70-117">-ResourceGroupName</span></span>
<span data-ttu-id="15a70-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="15a70-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="15a70-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="15a70-119">-ServerName</span></span>
<span data-ttu-id="15a70-120">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="15a70-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="15a70-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="15a70-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="15a70-122">Der Name der virtuellen Azure SQL Server-Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="15a70-122">The Azure Sql Server Virtual Network Rule name.</span></span>

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

### <span data-ttu-id="15a70-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a70-123">CommonParameters</span></span>
<span data-ttu-id="15a70-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15a70-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a70-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15a70-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a70-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15a70-126">INPUTS</span></span>

### <span data-ttu-id="15a70-127">System. String</span><span class="sxs-lookup"><span data-stu-id="15a70-127">System.String</span></span>

## <span data-ttu-id="15a70-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15a70-128">OUTPUTS</span></span>

### <span data-ttu-id="15a70-129">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="15a70-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="15a70-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="15a70-130">NOTES</span></span>

## <span data-ttu-id="15a70-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15a70-131">RELATED LINKS</span></span>
