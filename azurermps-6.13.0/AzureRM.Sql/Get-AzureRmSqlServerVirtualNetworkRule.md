---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 68fb8bac3a492bec915af6aea7df5d67fc3668dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477653"
---
# <span data-ttu-id="d56e0-101">Get-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d56e0-101">Get-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="d56e0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d56e0-102">SYNOPSIS</span></span>
<span data-ttu-id="d56e0-103">Ruft die virtuelle Azure SQL Server-Netzwerkregel ab oder listet Sie auf.</span><span class="sxs-lookup"><span data-stu-id="d56e0-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d56e0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d56e0-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d56e0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d56e0-105">DESCRIPTION</span></span>
<span data-ttu-id="d56e0-106">Dieser Befehl ruft eine bestimmte Azure SQL Server-Regel für virtuelles Netzwerk oder eine Liste von virtuellen Azure SQL Server-Netzwerkregeln unter einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="d56e0-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="d56e0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d56e0-107">EXAMPLES</span></span>

### <span data-ttu-id="d56e0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d56e0-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="d56e0-109">Ruft eine einzelne Azure SQL Server-Regel für virtuelles Netzwerk ab</span><span class="sxs-lookup"><span data-stu-id="d56e0-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="d56e0-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d56e0-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="d56e0-111">Ruft die Liste der virtuellen Azure SQL Server-Netzwerkregeln unter dem angegebenen Server ab.</span><span class="sxs-lookup"><span data-stu-id="d56e0-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

## <span data-ttu-id="d56e0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d56e0-112">PARAMETERS</span></span>

### <span data-ttu-id="d56e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d56e0-113">-DefaultProfile</span></span>
<span data-ttu-id="d56e0-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d56e0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d56e0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d56e0-115">-ResourceGroupName</span></span>
<span data-ttu-id="d56e0-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d56e0-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="d56e0-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="d56e0-117">-ServerName</span></span>
<span data-ttu-id="d56e0-118">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="d56e0-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="d56e0-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="d56e0-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="d56e0-120">Der Name der virtuellen Azure SQL Server-Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="d56e0-120">The Azure Sql Server Virtual Network Rule name.</span></span>

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

### <span data-ttu-id="d56e0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d56e0-121">CommonParameters</span></span>
<span data-ttu-id="d56e0-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d56e0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d56e0-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d56e0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d56e0-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d56e0-124">INPUTS</span></span>

### <span data-ttu-id="d56e0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d56e0-125">System.String</span></span>

## <span data-ttu-id="d56e0-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d56e0-126">OUTPUTS</span></span>

### <span data-ttu-id="d56e0-127">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="d56e0-127">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="d56e0-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="d56e0-128">NOTES</span></span>

## <span data-ttu-id="d56e0-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d56e0-129">RELATED LINKS</span></span>
