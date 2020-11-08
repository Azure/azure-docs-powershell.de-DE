---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 265600b201a6333b8dcd7c14f0cefe429f92619e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003374"
---
# <span data-ttu-id="91770-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="91770-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="91770-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91770-102">SYNOPSIS</span></span>
<span data-ttu-id="91770-103">Löscht eine Azure SQL Server-Regel für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="91770-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="91770-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91770-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91770-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91770-105">DESCRIPTION</span></span>
<span data-ttu-id="91770-106">Mit diesem Befehl wird eine virtuelle Azure SQL Server-Netzwerkregel gelöscht.</span><span class="sxs-lookup"><span data-stu-id="91770-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="91770-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91770-107">EXAMPLES</span></span>

### <span data-ttu-id="91770-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="91770-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="91770-109">Löscht eine vorhandene virtuelle Azure SQL Server-Netzwerkregel</span><span class="sxs-lookup"><span data-stu-id="91770-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="91770-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="91770-110">PARAMETERS</span></span>

### <span data-ttu-id="91770-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91770-111">-AsJob</span></span>
<span data-ttu-id="91770-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="91770-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91770-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91770-113">-DefaultProfile</span></span>
<span data-ttu-id="91770-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="91770-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91770-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91770-115">-ResourceGroupName</span></span>
<span data-ttu-id="91770-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="91770-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="91770-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="91770-117">-ServerName</span></span>
<span data-ttu-id="91770-118">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="91770-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="91770-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="91770-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="91770-120">Name der virtuellen Azure SQL Server-Netzwerkregel</span><span class="sxs-lookup"><span data-stu-id="91770-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="91770-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="91770-121">-Confirm</span></span>
<span data-ttu-id="91770-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91770-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91770-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91770-123">-WhatIf</span></span>
<span data-ttu-id="91770-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91770-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91770-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91770-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91770-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91770-126">CommonParameters</span></span>
<span data-ttu-id="91770-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91770-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91770-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91770-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91770-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91770-129">INPUTS</span></span>

### <span data-ttu-id="91770-130">System. String</span><span class="sxs-lookup"><span data-stu-id="91770-130">System.String</span></span>

## <span data-ttu-id="91770-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91770-131">OUTPUTS</span></span>

### <span data-ttu-id="91770-132">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="91770-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="91770-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="91770-133">NOTES</span></span>

## <span data-ttu-id="91770-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91770-134">RELATED LINKS</span></span>
