---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: 4a9e128fb8c67c44329dd2b99da8ce4722835323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943409"
---
# <span data-ttu-id="632db-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="632db-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="632db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="632db-102">SYNOPSIS</span></span>
<span data-ttu-id="632db-103">Ruft flexible Datenbanken in einem Pool für flexible Datenbanken und deren Eigenschaftswerte ab.</span><span class="sxs-lookup"><span data-stu-id="632db-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="632db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="632db-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="632db-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="632db-105">DESCRIPTION</span></span>
<span data-ttu-id="632db-106">Das **Get-AzSqlElasticPoolDatabase-Cmdlet** ruft flexible Datenbanken in einem Pool mit flexiblen Bändern und deren Eigenschaftswerten ab.</span><span class="sxs-lookup"><span data-stu-id="632db-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="632db-107">Sie können den Namen einer flexiblen Datenbank in Azure SQL-Datenbank angeben, um die Eigenschaftswerte nur für diese Datenbank zu sehen.</span><span class="sxs-lookup"><span data-stu-id="632db-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="632db-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="632db-108">EXAMPLES</span></span>

### <span data-ttu-id="632db-109">Beispiel 1: Alle Datenbanken in einem Pool mit einem Flexiblen Pool erhalten</span><span class="sxs-lookup"><span data-stu-id="632db-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="632db-110">Dieser Befehl ruft alle Datenbanken in einem Pool mit dem Namen "ElasticPool01" ab.</span><span class="sxs-lookup"><span data-stu-id="632db-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="632db-111">Beispiel 2: Holen Sie sich alle Datenbanken in einem Pool mit einem Flexiblen Pool mithilfe von Filtern.</span><span class="sxs-lookup"><span data-stu-id="632db-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="632db-112">Dieser Befehl ruft alle Datenbanken in einem Pool mit dem Namen "ElasticPool01" ab, der mit "Datenbank" beginnt.</span><span class="sxs-lookup"><span data-stu-id="632db-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="632db-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="632db-113">PARAMETERS</span></span>

### <span data-ttu-id="632db-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="632db-114">-DatabaseName</span></span>
<span data-ttu-id="632db-115">Gibt den Namen der datenbank SQL an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="632db-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="632db-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="632db-116">-DefaultProfile</span></span>
<span data-ttu-id="632db-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="632db-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="632db-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="632db-118">-ElasticPoolName</span></span>
<span data-ttu-id="632db-119">Gibt den Namen eines Pool für einen flexiblen Pool an.</span><span class="sxs-lookup"><span data-stu-id="632db-119">Specifies the name of an elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="632db-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="632db-120">-ResourceGroupName</span></span>
<span data-ttu-id="632db-121">Gibt den Namen einer Ressourcengruppe an, der der Pool für den Pool zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="632db-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="632db-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="632db-122">-ServerName</span></span>
<span data-ttu-id="632db-123">Gibt den Namen eines Servers an, der einen Pool für einen flexiblen Pool enthält.</span><span class="sxs-lookup"><span data-stu-id="632db-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="632db-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="632db-124">-Confirm</span></span>
<span data-ttu-id="632db-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="632db-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="632db-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="632db-126">-WhatIf</span></span>
<span data-ttu-id="632db-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="632db-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="632db-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="632db-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="632db-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="632db-129">CommonParameters</span></span>
<span data-ttu-id="632db-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="632db-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="632db-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="632db-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="632db-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="632db-132">INPUTS</span></span>

### <span data-ttu-id="632db-133">System.String</span><span class="sxs-lookup"><span data-stu-id="632db-133">System.String</span></span>

## <span data-ttu-id="632db-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="632db-134">OUTPUTS</span></span>

### <span data-ttu-id="632db-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="632db-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="632db-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="632db-136">NOTES</span></span>

## <span data-ttu-id="632db-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="632db-137">RELATED LINKS</span></span>

[<span data-ttu-id="632db-138">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="632db-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="632db-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="632db-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="632db-140">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="632db-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="632db-141">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="632db-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="632db-142">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="632db-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

