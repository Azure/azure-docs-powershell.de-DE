---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: 2e24dc80b93d72722d05a7dced05cbea02751a05
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995574"
---
# <span data-ttu-id="f097d-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="f097d-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="f097d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f097d-102">SYNOPSIS</span></span>
<span data-ttu-id="f097d-103">Ruft elastische Datenbanken in einem elastischen Pool und deren Eigenschaftenwerten ab.</span><span class="sxs-lookup"><span data-stu-id="f097d-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="f097d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f097d-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f097d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f097d-105">DESCRIPTION</span></span>
<span data-ttu-id="f097d-106">Das Cmdlet " **Get-AzSqlElasticPoolDatabase** " erhält elastische Datenbanken in einem elastischen Pool und deren Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="f097d-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="f097d-107">Sie können den Namen einer elastischen Datenbank in Azure SQL-Datenbank angeben, um die Eigenschaftswerte nur für diese Datenbank anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f097d-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="f097d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f097d-108">EXAMPLES</span></span>

### <span data-ttu-id="f097d-109">Beispiel 1: Abrufen aller Datenbanken in einem elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="f097d-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="f097d-110">Dieser Befehl ruft alle Datenbanken in einem elastischen Pool mit dem Namen ElasticPool01 ab.</span><span class="sxs-lookup"><span data-stu-id="f097d-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="f097d-111">Beispiel 2: Abrufen aller Datenbanken in einem elastischen Pool mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="f097d-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="f097d-112">Dieser Befehl ruft alle Datenbanken in einem elastischen Pool mit dem Namen "ElasticPool01" ab, die mit "Datenbank" beginnen.</span><span class="sxs-lookup"><span data-stu-id="f097d-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="f097d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f097d-113">PARAMETERS</span></span>

### <span data-ttu-id="f097d-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f097d-114">-DatabaseName</span></span>
<span data-ttu-id="f097d-115">Gibt den Namen der SQL-Datenbank an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f097d-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f097d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f097d-116">-DefaultProfile</span></span>
<span data-ttu-id="f097d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f097d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f097d-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f097d-118">-ElasticPoolName</span></span>
<span data-ttu-id="f097d-119">Gibt den Namen eines elastischen Pools an.</span><span class="sxs-lookup"><span data-stu-id="f097d-119">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="f097d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f097d-120">-ResourceGroupName</span></span>
<span data-ttu-id="f097d-121">Gibt den Namen einer Ressourcengruppe an, der der elastische Pool zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f097d-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="f097d-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="f097d-122">-ServerName</span></span>
<span data-ttu-id="f097d-123">Gibt den Namen eines Servers an, der einen elastischen Pool enthält.</span><span class="sxs-lookup"><span data-stu-id="f097d-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="f097d-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f097d-124">-Confirm</span></span>
<span data-ttu-id="f097d-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f097d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f097d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f097d-126">-WhatIf</span></span>
<span data-ttu-id="f097d-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f097d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f097d-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f097d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f097d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f097d-129">CommonParameters</span></span>
<span data-ttu-id="f097d-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f097d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f097d-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f097d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f097d-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f097d-132">INPUTS</span></span>

### <span data-ttu-id="f097d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f097d-133">System.String</span></span>

## <span data-ttu-id="f097d-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f097d-134">OUTPUTS</span></span>

### <span data-ttu-id="f097d-135">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f097d-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f097d-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="f097d-136">NOTES</span></span>

## <span data-ttu-id="f097d-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f097d-137">RELATED LINKS</span></span>

[<span data-ttu-id="f097d-138">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f097d-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="f097d-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="f097d-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="f097d-140">Neu – AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f097d-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="f097d-141">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f097d-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="f097d-142">Satz-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f097d-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

