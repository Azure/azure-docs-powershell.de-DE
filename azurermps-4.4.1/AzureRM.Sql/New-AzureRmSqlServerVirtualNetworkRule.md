---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 08d14217cff370557009167e09cd7e5396df4e2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478857"
---
# <span data-ttu-id="0ef66-101">New-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0ef66-101">New-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="0ef66-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ef66-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef66-103">Erstellt eine Azure SQL Server-Regel für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0ef66-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ef66-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ef66-104">SYNTAX</span></span>

```
New-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ef66-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ef66-105">DESCRIPTION</span></span>
<span data-ttu-id="0ef66-106">Erstellt eine Azure SQL Server-Regel für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0ef66-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="0ef66-107">Es werden virtuelle Netzwerkregeln verwendet, um den Azure SQL Server mit einem bestimmten virtuellen Netzwerk zu verbinden, um den Zugriff auf Azure SQL Server so zu beschränken, dass er nur im virtuellen Netzwerk zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="0ef66-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="0ef66-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ef66-108">EXAMPLES</span></span>

### <span data-ttu-id="0ef66-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0ef66-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="0ef66-110">Erstellt eine virtuelle Azure SQL Server-Netzwerkregel</span><span class="sxs-lookup"><span data-stu-id="0ef66-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="0ef66-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ef66-111">PARAMETERS</span></span>

### <span data-ttu-id="0ef66-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ef66-112">-ResourceGroupName</span></span>
<span data-ttu-id="0ef66-113">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0ef66-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="0ef66-114">-Servername</span><span class="sxs-lookup"><span data-stu-id="0ef66-114">-ServerName</span></span>
<span data-ttu-id="0ef66-115">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="0ef66-115">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="0ef66-116">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="0ef66-116">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="0ef66-117">Azure SQL Server-Regel Name für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="0ef66-117">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="0ef66-118">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="0ef66-118">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="0ef66-119">Die Subnetz-ID des virtuellen Netzwerks, die die Microsoft. Network-Details angibt</span><span class="sxs-lookup"><span data-stu-id="0ef66-119">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="0ef66-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0ef66-120">-Confirm</span></span>
<span data-ttu-id="0ef66-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0ef66-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ef66-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ef66-122">-WhatIf</span></span>
<span data-ttu-id="0ef66-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ef66-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ef66-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ef66-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ef66-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ef66-125">-DefaultProfile</span></span>
<span data-ttu-id="0ef66-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ef66-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ef66-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef66-127">CommonParameters</span></span>
<span data-ttu-id="0ef66-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ef66-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef66-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ef66-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef66-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ef66-130">INPUTS</span></span>

### <span data-ttu-id="0ef66-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0ef66-131">System.String</span></span>

## <span data-ttu-id="0ef66-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ef66-132">OUTPUTS</span></span>

### <span data-ttu-id="0ef66-133">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="0ef66-133">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="0ef66-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ef66-134">NOTES</span></span>

## <span data-ttu-id="0ef66-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ef66-135">RELATED LINKS</span></span>

