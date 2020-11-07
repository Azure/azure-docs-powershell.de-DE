---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: f03d172db1a4e8952fea989499f1689d9e0b6a83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825775"
---
# <span data-ttu-id="b7350-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="b7350-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="b7350-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7350-102">SYNOPSIS</span></span>
<span data-ttu-id="b7350-103">Ruft elastische Datenbanken in einem elastischen Pool und deren Eigenschaftenwerten ab.</span><span class="sxs-lookup"><span data-stu-id="b7350-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="b7350-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7350-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7350-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7350-105">DESCRIPTION</span></span>
<span data-ttu-id="b7350-106">Das Cmdlet " **Get-AzSqlElasticPoolDatabase** " erhält elastische Datenbanken in einem elastischen Pool und deren Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="b7350-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="b7350-107">Sie können den Namen einer elastischen Datenbank in Azure SQL-Datenbank angeben, um die Eigenschaftswerte nur für diese Datenbank anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b7350-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="b7350-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7350-108">EXAMPLES</span></span>

### <span data-ttu-id="b7350-109">Beispiel 1: Abrufen aller Datenbanken in einem elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="b7350-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="b7350-110">Dieser Befehl ruft alle Datenbanken in einem elastischen Pool mit dem Namen ElasticPool01 ab.</span><span class="sxs-lookup"><span data-stu-id="b7350-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="b7350-111">Beispiel 2: Abrufen aller Datenbanken in einem elastischen Pool mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="b7350-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="b7350-112">Dieser Befehl ruft alle Datenbanken in einem elastischen Pool mit dem Namen "ElasticPool01" ab, die mit "Datenbank" beginnen.</span><span class="sxs-lookup"><span data-stu-id="b7350-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="b7350-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7350-113">PARAMETERS</span></span>

### <span data-ttu-id="b7350-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b7350-114">-DatabaseName</span></span>
<span data-ttu-id="b7350-115">Gibt den Namen der SQL-Datenbank an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b7350-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b7350-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7350-116">-DefaultProfile</span></span>
<span data-ttu-id="b7350-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b7350-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7350-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b7350-118">-ElasticPoolName</span></span>
<span data-ttu-id="b7350-119">Gibt den Namen eines elastischen Pools an.</span><span class="sxs-lookup"><span data-stu-id="b7350-119">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="b7350-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7350-120">-ResourceGroupName</span></span>
<span data-ttu-id="b7350-121">Gibt den Namen einer Ressourcengruppe an, der der elastische Pool zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b7350-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="b7350-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="b7350-122">-ServerName</span></span>
<span data-ttu-id="b7350-123">Gibt den Namen eines Servers an, der einen elastischen Pool enthält.</span><span class="sxs-lookup"><span data-stu-id="b7350-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="b7350-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b7350-124">-Confirm</span></span>
<span data-ttu-id="b7350-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b7350-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7350-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7350-126">-WhatIf</span></span>
<span data-ttu-id="b7350-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b7350-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7350-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7350-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7350-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7350-129">CommonParameters</span></span>
<span data-ttu-id="b7350-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7350-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7350-131">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7350-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7350-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7350-132">INPUTS</span></span>

### <span data-ttu-id="b7350-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b7350-133">System.String</span></span>

## <span data-ttu-id="b7350-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7350-134">OUTPUTS</span></span>

### <span data-ttu-id="b7350-135">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b7350-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="b7350-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7350-136">NOTES</span></span>

## <span data-ttu-id="b7350-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7350-137">RELATED LINKS</span></span>

[<span data-ttu-id="b7350-138">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b7350-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="b7350-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="b7350-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="b7350-140">Neu – AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b7350-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="b7350-141">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b7350-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="b7350-142">Satz-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b7350-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

