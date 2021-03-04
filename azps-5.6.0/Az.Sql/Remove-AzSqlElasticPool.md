---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: 565d22bc2860acc69f5d919bf000a564d9295ce5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920195"
---
# <span data-ttu-id="5055f-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5055f-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="5055f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5055f-102">SYNOPSIS</span></span>
<span data-ttu-id="5055f-103">Löscht einen pool für flexible Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="5055f-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="5055f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5055f-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5055f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5055f-105">DESCRIPTION</span></span>
<span data-ttu-id="5055f-106">Das **Cmdlet Remove-AzSqlElasticPool** löscht einen Azure SQL Database-Pool.</span><span class="sxs-lookup"><span data-stu-id="5055f-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="5055f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5055f-107">EXAMPLES</span></span>

### <span data-ttu-id="5055f-108">Beispiel 1: Löschen eines Pool für einen Flexiblen Pool</span><span class="sxs-lookup"><span data-stu-id="5055f-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="5055f-109">Mit diesem Befehl wird ein Pool mit dem Namen "ElasticPool01" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5055f-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="5055f-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5055f-110">PARAMETERS</span></span>

### <span data-ttu-id="5055f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5055f-111">-DefaultProfile</span></span>
<span data-ttu-id="5055f-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5055f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5055f-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5055f-113">-ElasticPoolName</span></span>
<span data-ttu-id="5055f-114">Gibt den Namen des Pool für den Bänder an, den dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="5055f-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5055f-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="5055f-115">-Force</span></span>
<span data-ttu-id="5055f-116">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="5055f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5055f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5055f-117">-ResourceGroupName</span></span>
<span data-ttu-id="5055f-118">Gibt den Namen der Ressourcengruppe an, der der Pool für den Pool zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5055f-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="5055f-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="5055f-119">-ServerName</span></span>
<span data-ttu-id="5055f-120">Gibt den Namen des Servers an, auf dem sich der Pool für die flexiblen Bänder befindet.</span><span class="sxs-lookup"><span data-stu-id="5055f-120">Specifies the name of the server that hosts the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5055f-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5055f-121">-Confirm</span></span>
<span data-ttu-id="5055f-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5055f-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5055f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5055f-123">-WhatIf</span></span>
<span data-ttu-id="5055f-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5055f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5055f-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5055f-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5055f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5055f-126">CommonParameters</span></span>
<span data-ttu-id="5055f-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5055f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5055f-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5055f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5055f-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5055f-129">INPUTS</span></span>

### <span data-ttu-id="5055f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5055f-130">System.String</span></span>

## <span data-ttu-id="5055f-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5055f-131">OUTPUTS</span></span>

### <span data-ttu-id="5055f-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="5055f-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="5055f-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5055f-133">NOTES</span></span>

## <span data-ttu-id="5055f-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5055f-134">RELATED LINKS</span></span>

[<span data-ttu-id="5055f-135">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5055f-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="5055f-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="5055f-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="5055f-137">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="5055f-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="5055f-138">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5055f-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="5055f-139">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5055f-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="5055f-140">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="5055f-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


