---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 355b8fdffd5d1e9e16fe9bfaf504d627a8b9b167
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665234"
---
# <span data-ttu-id="56795-101">Set-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="56795-101">Set-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="56795-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56795-102">SYNOPSIS</span></span>
<span data-ttu-id="56795-103">Ändert die Konfiguration einer virtuellen Azure SQL Server-Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="56795-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56795-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56795-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56795-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56795-105">DESCRIPTION</span></span>
<span data-ttu-id="56795-106">Mit diesem Befehl wird die Konfiguration einer virtuellen Azure SQL Server-Netzwerkregel geändert.</span><span class="sxs-lookup"><span data-stu-id="56795-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>


<span data-ttu-id="56795-107">Verwenden Sie stattdessen "Add-AzureRmSqlServerVirtualNetworkRule" und "Remove-AzureRmSqlServerVirtualNetworkRule", um den Satz virtueller Netzwerkregeln auf dem Server zu steuern.</span><span class="sxs-lookup"><span data-stu-id="56795-107">To control the set of virtual network rules in the server, use 'Add-AzureRmSqlServerVirtualNetworkRule' and 'Remove-AzureRmSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="56795-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56795-108">EXAMPLES</span></span>

### <span data-ttu-id="56795-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="56795-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="56795-110">Ändert eine vorhandene virtuelle Netzwerkregel mit der neuen virtuellen Netzwerk-Subnetz-ID, die Informationen zum neuen virtuellen Netzwerk enthält.</span><span class="sxs-lookup"><span data-stu-id="56795-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="56795-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="56795-111">PARAMETERS</span></span>

### <span data-ttu-id="56795-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56795-112">-ResourceGroupName</span></span>
<span data-ttu-id="56795-113">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="56795-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="56795-114">-Servername</span><span class="sxs-lookup"><span data-stu-id="56795-114">-ServerName</span></span>
<span data-ttu-id="56795-115">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="56795-115">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="56795-116">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="56795-116">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="56795-117">Der Name der virtuellen Azure SQL Server-Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="56795-117">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="56795-118">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="56795-118">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="56795-119">Die Subnetz-ID des virtuellen Netzwerks für die Regel.</span><span class="sxs-lookup"><span data-stu-id="56795-119">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="56795-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="56795-120">-Confirm</span></span>
<span data-ttu-id="56795-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56795-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56795-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56795-122">-WhatIf</span></span>
<span data-ttu-id="56795-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56795-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56795-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56795-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56795-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56795-125">-DefaultProfile</span></span>
<span data-ttu-id="56795-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="56795-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56795-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56795-127">CommonParameters</span></span>
<span data-ttu-id="56795-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56795-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56795-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56795-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56795-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56795-130">INPUTS</span></span>

### <span data-ttu-id="56795-131">System. String</span><span class="sxs-lookup"><span data-stu-id="56795-131">System.String</span></span>

## <span data-ttu-id="56795-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56795-132">OUTPUTS</span></span>

### <span data-ttu-id="56795-133">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="56795-133">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="56795-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="56795-134">NOTES</span></span>

## <span data-ttu-id="56795-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56795-135">RELATED LINKS</span></span>

