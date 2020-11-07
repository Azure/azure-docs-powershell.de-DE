---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 8c680cf87deedf5fc4bd8671a60db4329a1f68ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665248"
---
# <span data-ttu-id="c985f-101">Remove-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c985f-101">Remove-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="c985f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c985f-102">SYNOPSIS</span></span>
<span data-ttu-id="c985f-103">Löscht eine Azure SQL Server-Regel für virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c985f-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c985f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c985f-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c985f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c985f-105">DESCRIPTION</span></span>
<span data-ttu-id="c985f-106">Mit diesem Befehl wird eine virtuelle Azure SQL Server-Netzwerkregel gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c985f-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="c985f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c985f-107">EXAMPLES</span></span>

### <span data-ttu-id="c985f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c985f-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="c985f-109">Löscht eine vorhandene virtuelle Azure SQL Server-Netzwerkregel</span><span class="sxs-lookup"><span data-stu-id="c985f-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="c985f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c985f-110">PARAMETERS</span></span>

### <span data-ttu-id="c985f-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c985f-111">-ResourceGroupName</span></span>
<span data-ttu-id="c985f-112">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c985f-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="c985f-113">-Servername</span><span class="sxs-lookup"><span data-stu-id="c985f-113">-ServerName</span></span>
<span data-ttu-id="c985f-114">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="c985f-114">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c985f-115">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="c985f-115">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="c985f-116">Name der virtuellen Azure SQL Server-Netzwerkregel</span><span class="sxs-lookup"><span data-stu-id="c985f-116">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="c985f-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c985f-117">-Confirm</span></span>
<span data-ttu-id="c985f-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c985f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c985f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c985f-119">-WhatIf</span></span>
<span data-ttu-id="c985f-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c985f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c985f-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c985f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c985f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c985f-122">-DefaultProfile</span></span>
<span data-ttu-id="c985f-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c985f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c985f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c985f-124">CommonParameters</span></span>
<span data-ttu-id="c985f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c985f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c985f-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c985f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c985f-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c985f-127">INPUTS</span></span>

### <span data-ttu-id="c985f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c985f-128">System.String</span></span>

## <span data-ttu-id="c985f-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c985f-129">OUTPUTS</span></span>

### <span data-ttu-id="c985f-130">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="c985f-130">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="c985f-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="c985f-131">NOTES</span></span>

## <span data-ttu-id="c985f-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c985f-132">RELATED LINKS</span></span>

