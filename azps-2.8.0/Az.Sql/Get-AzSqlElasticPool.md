---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
ms.openlocfilehash: 12abc93747452ad379e235ec70f3ddb4bbd2e638
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825579"
---
# <span data-ttu-id="c827e-101">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c827e-101">Get-AzSqlElasticPool</span></span>

## <span data-ttu-id="c827e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c827e-102">SYNOPSIS</span></span>
<span data-ttu-id="c827e-103">Ruft elastische Pools und ihre Eigenschaftswerte in einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="c827e-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

## <span data-ttu-id="c827e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c827e-104">SYNTAX</span></span>

```
Get-AzSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c827e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c827e-105">DESCRIPTION</span></span>
<span data-ttu-id="c827e-106">Das Cmdlet " **Get-AzSqlElasticPool** " erhält elastische Pools und ihre Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="c827e-106">The **Get-AzSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="c827e-107">Geben Sie den Namen eines vorhandenen elastischen Pools an, um die Eigenschaftswerte nur für diesen Pool anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c827e-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="c827e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c827e-108">EXAMPLES</span></span>

### <span data-ttu-id="c827e-109">Beispiel 1: Abrufen aller elastischen Pools</span><span class="sxs-lookup"><span data-stu-id="c827e-109">Example 1: Get all elastic pools</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              : 

ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool02
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool02
Location          : Central US
CreationDate      : 8/26/2015 11:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="c827e-110">Dieser Befehl ruft alle elastischen Pools auf dem Server mit dem Namen "Server01" ab.</span><span class="sxs-lookup"><span data-stu-id="c827e-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="c827e-111">Beispiel 2: Abrufen eines bestimmten elastischen Pools</span><span class="sxs-lookup"><span data-stu-id="c827e-111">Example 2: Get a specific elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool27"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="c827e-112">Dieser Befehl ruft den elastischen Pool mit dem Namen ElasticPool0127 auf dem Server mit dem Namen SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="c827e-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="c827e-113">Beispiel 3: Abrufen von Metriken für einen Azure SQL Elastic-Daten Bank Pool</span><span class="sxs-lookup"><span data-stu-id="c827e-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" | Get-AzMetric -TimeGrain 0:5:0 -MetricName storage_percent
DimensionName  : 
DimensionValue : 
Name           : cpu_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : physical_data_read_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : log_write_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : dtu_consumption_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : storage_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent
```

<span data-ttu-id="c827e-114">Dieser Befehl gibt Metriken für einen Azure SQL Elastic-datenbankpool mit dem Namen ElasticPool01 zurück.</span><span class="sxs-lookup"><span data-stu-id="c827e-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

### <span data-ttu-id="c827e-115">Beispiel 4: Abrufen aller elastischen Pools mit Filter-ElasticPoolName "ElasticPool \*"</span><span class="sxs-lookup"><span data-stu-id="c827e-115">Example 4: Get all elastic pools using filtering -ElasticPoolName "ElasticPool\*"</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              : 

ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool02
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool02
Location          : Central US
CreationDate      : 8/26/2015 11:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="c827e-116">Dieser Befehl ruft alle elastischen Pools auf dem Server mit dem Namen "Server01" ab, die mit "ElasticPool" beginnen.</span><span class="sxs-lookup"><span data-stu-id="c827e-116">This command gets all of the elastic pools on the server named Server01 that start with "ElasticPool".</span></span>

## <span data-ttu-id="c827e-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="c827e-117">PARAMETERS</span></span>

### <span data-ttu-id="c827e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c827e-118">-DefaultProfile</span></span>
<span data-ttu-id="c827e-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c827e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c827e-120">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="c827e-120">-ElasticPoolName</span></span>
<span data-ttu-id="c827e-121">Gibt den Namen des elastischen Pools an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="c827e-121">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c827e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c827e-122">-ResourceGroupName</span></span>
<span data-ttu-id="c827e-123">Gibt den Namen der Ressourcengruppe an, die den elastischen Pool enthält, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="c827e-123">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c827e-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="c827e-124">-ServerName</span></span>
<span data-ttu-id="c827e-125">Gibt den Namen des Servers an, der den elastischen Pool enthält, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="c827e-125">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c827e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c827e-126">CommonParameters</span></span>
<span data-ttu-id="c827e-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c827e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c827e-128">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c827e-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c827e-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c827e-129">INPUTS</span></span>

### <span data-ttu-id="c827e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c827e-130">System.String</span></span>

## <span data-ttu-id="c827e-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c827e-131">OUTPUTS</span></span>

### <span data-ttu-id="c827e-132">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="c827e-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="c827e-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c827e-133">NOTES</span></span>

## <span data-ttu-id="c827e-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c827e-134">RELATED LINKS</span></span>

[<span data-ttu-id="c827e-135">Neu – AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c827e-135">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="c827e-136">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c827e-136">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="c827e-137">Satz-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c827e-137">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


