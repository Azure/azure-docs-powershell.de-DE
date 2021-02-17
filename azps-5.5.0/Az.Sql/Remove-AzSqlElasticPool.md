---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: d751954a5c66d9220513017aa62b6797f8f1ea6f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164913"
---
# <span data-ttu-id="523a5-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="523a5-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="523a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="523a5-102">SYNOPSIS</span></span>
<span data-ttu-id="523a5-103">Löscht einen Datenbankpool mit Bändern.</span><span class="sxs-lookup"><span data-stu-id="523a5-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="523a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="523a5-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="523a5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="523a5-105">DESCRIPTION</span></span>
<span data-ttu-id="523a5-106">Das **Cmdlet "Remove-AzSqlElasticPool"** löscht einen Azure SQL Database-Pool.</span><span class="sxs-lookup"><span data-stu-id="523a5-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="523a5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="523a5-107">EXAMPLES</span></span>

### <span data-ttu-id="523a5-108">Beispiel 1: Löschen eines Pool im Pool</span><span class="sxs-lookup"><span data-stu-id="523a5-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="523a5-109">Mit diesem Befehl wird ein Pool mit dem Namen "PoolsPool01" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="523a5-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="523a5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="523a5-110">PARAMETERS</span></span>

### <span data-ttu-id="523a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="523a5-111">-DefaultProfile</span></span>
<span data-ttu-id="523a5-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="523a5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="523a5-113">-PoolName</span><span class="sxs-lookup"><span data-stu-id="523a5-113">-ElasticPoolName</span></span>
<span data-ttu-id="523a5-114">Gibt den Namen des Poolpools an, der von diesem Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="523a5-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="523a5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="523a5-115">-Force</span></span>
<span data-ttu-id="523a5-116">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="523a5-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="523a5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="523a5-117">-ResourceGroupName</span></span>
<span data-ttu-id="523a5-118">Gibt den Namen der Ressourcengruppe an, der der Pool "Pool" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="523a5-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="523a5-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="523a5-119">-ServerName</span></span>
<span data-ttu-id="523a5-120">Gibt den Namen des Servers an, auf dem sich der Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="523a5-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="523a5-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="523a5-121">-Confirm</span></span>
<span data-ttu-id="523a5-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="523a5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="523a5-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="523a5-123">-WhatIf</span></span>
<span data-ttu-id="523a5-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="523a5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="523a5-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="523a5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="523a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="523a5-126">CommonParameters</span></span>
<span data-ttu-id="523a5-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="523a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="523a5-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="523a5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="523a5-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="523a5-129">INPUTS</span></span>

### <span data-ttu-id="523a5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="523a5-130">System.String</span></span>

## <span data-ttu-id="523a5-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="523a5-131">OUTPUTS</span></span>

### <span data-ttu-id="523a5-132">Microsoft.Azure.Commands.Sql.Pool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="523a5-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="523a5-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="523a5-133">NOTES</span></span>

## <span data-ttu-id="523a5-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="523a5-134">RELATED LINKS</span></span>

[<span data-ttu-id="523a5-135">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="523a5-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="523a5-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="523a5-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="523a5-137">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="523a5-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="523a5-138">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="523a5-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="523a5-139">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="523a5-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="523a5-140">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="523a5-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


