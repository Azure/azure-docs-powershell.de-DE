---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 454aac300aa3b34cbc435df455100d64c5d0abdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665346"
---
# <span data-ttu-id="d4a68-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d4a68-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="d4a68-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4a68-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a68-103">Erstellt einen elastischen datenbankpool für eine SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d4a68-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4a68-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4a68-104">SYNTAX</span></span>

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4a68-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4a68-105">DESCRIPTION</span></span>
<span data-ttu-id="d4a68-106">Das Cmdlet **New-AzureRmSqlElasticPool** erstellt einen elastischen datenbankpool für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d4a68-106">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>

<span data-ttu-id="d4a68-107">Für verschiedene Parameter ( *-DTU,-DatabaseDtuMin und-DatabaseDtuMax* ) ist der festzusetzende Wert aus der Liste gültiger Werte für diesen Parameter erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d4a68-107">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="d4a68-108">Beispiel:-DatabaseDtuMax für einen Standard mäßigen 100-eDTU-Pool kann nur auf 10, 20, 50 oder 100 eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d4a68-108">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="d4a68-109">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="d4a68-109">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

## <span data-ttu-id="d4a68-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4a68-110">EXAMPLES</span></span>

### <span data-ttu-id="d4a68-111">Beispiel 1: Erstellen eines elastischen Pools</span><span class="sxs-lookup"><span data-stu-id="d4a68-111">Example 1: Create an elastic pool</span></span>
```
PS C:\>New-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
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

<span data-ttu-id="d4a68-112">Dieser Befehl erstellt einen elastischen Pool in der Standard Dienstebene mit dem Namen ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="d4a68-112">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="d4a68-113">Der Server mit dem Namen Server01, der einer Azure-Ressourcengruppe mit dem Namen ResourceGroup01 zugewiesen ist, hostet den elastischen Pool in.</span><span class="sxs-lookup"><span data-stu-id="d4a68-113">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="d4a68-114">Mit dem Befehl werden die DTU-Eigenschaftswerte für den Pool und die Datenbanken im Pool angegeben.</span><span class="sxs-lookup"><span data-stu-id="d4a68-114">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="d4a68-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4a68-115">PARAMETERS</span></span>

### <span data-ttu-id="d4a68-116">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="d4a68-116">-DatabaseDtuMax</span></span>
<span data-ttu-id="d4a68-117">Gibt die maximale Anzahl von Datenbankdurchsatz Einheiten (DTUs) an, die eine einzelne Datenbank im Pool nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="d4a68-117">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="d4a68-118">Die Standardwerte für die verschiedenen Editionen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d4a68-118">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="d4a68-119">Grundlegende.</span><span class="sxs-lookup"><span data-stu-id="d4a68-119">Basic.</span></span> <span data-ttu-id="d4a68-120">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="d4a68-120">5 DTUs</span></span>
- <span data-ttu-id="d4a68-121">Standard.</span><span class="sxs-lookup"><span data-stu-id="d4a68-121">Standard.</span></span> <span data-ttu-id="d4a68-122">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="d4a68-122">100 DTUs</span></span>
- <span data-ttu-id="d4a68-123">Premium.</span><span class="sxs-lookup"><span data-stu-id="d4a68-123">Premium.</span></span> <span data-ttu-id="d4a68-124">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="d4a68-124">125 DTUs</span></span>

<span data-ttu-id="d4a68-125">Informationen dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) .</span><span class="sxs-lookup"><span data-stu-id="d4a68-125">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span> 


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a68-126">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="d4a68-126">-DatabaseDtuMin</span></span>
<span data-ttu-id="d4a68-127">Gibt die minimale Anzahl von DTUs an, die der elastische Pool für alle Datenbanken im Pool garantiert.</span><span class="sxs-lookup"><span data-stu-id="d4a68-127">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="d4a68-128">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d4a68-128">The default value is zero (0).</span></span>

<span data-ttu-id="d4a68-129">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="d4a68-129">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a68-130">-DTU</span><span class="sxs-lookup"><span data-stu-id="d4a68-130">-Dtu</span></span>
<span data-ttu-id="d4a68-131">Gibt die Gesamtzahl der freigegebenen DTUs für den elastischen Pool an.</span><span class="sxs-lookup"><span data-stu-id="d4a68-131">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="d4a68-132">Die Standardwerte für die verschiedenen Editionen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d4a68-132">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="d4a68-133">Grundlegende.</span><span class="sxs-lookup"><span data-stu-id="d4a68-133">Basic.</span></span>
<span data-ttu-id="d4a68-134">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="d4a68-134">100 DTUs</span></span>
- <span data-ttu-id="d4a68-135">Standard.</span><span class="sxs-lookup"><span data-stu-id="d4a68-135">Standard.</span></span>
<span data-ttu-id="d4a68-136">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="d4a68-136">100 DTUs</span></span>
- <span data-ttu-id="d4a68-137">Premium.</span><span class="sxs-lookup"><span data-stu-id="d4a68-137">Premium.</span></span>
<span data-ttu-id="d4a68-138">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="d4a68-138">125 DTUs</span></span>

<span data-ttu-id="d4a68-139">Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="d4a68-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a68-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="d4a68-140">-Edition</span></span>
<span data-ttu-id="d4a68-141">Gibt die Edition der Azure SQL-Datenbank an, die für den elastischen Pool verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4a68-141">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="d4a68-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d4a68-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4a68-143">Premium</span><span class="sxs-lookup"><span data-stu-id="d4a68-143">Premium</span></span>
- <span data-ttu-id="d4a68-144">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="d4a68-144">Basic</span></span>
- <span data-ttu-id="d4a68-145">Standard</span><span class="sxs-lookup"><span data-stu-id="d4a68-145">Standard</span></span>
- <span data-ttu-id="d4a68-146">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="d4a68-146">DataWarehouse</span></span>
- <span data-ttu-id="d4a68-147">Stretch</span><span class="sxs-lookup"><span data-stu-id="d4a68-147">Stretch</span></span>
- <span data-ttu-id="d4a68-148">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="d4a68-148">Free</span></span>
- <span data-ttu-id="d4a68-149">Premiums</span><span class="sxs-lookup"><span data-stu-id="d4a68-149">PremiumRS</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a68-150">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d4a68-150">-ElasticPoolName</span></span>
<span data-ttu-id="d4a68-151">Gibt den Namen des von diesem Cmdlet erstellten elastischen Pools an.</span><span class="sxs-lookup"><span data-stu-id="d4a68-151">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a68-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4a68-152">-ResourceGroupName</span></span>
<span data-ttu-id="d4a68-153">Gibt den Namen der Ressourcengruppe an, der dieses Cmdlet den elastischen Pool zuweist.</span><span class="sxs-lookup"><span data-stu-id="d4a68-153">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="d4a68-154">-Servername</span><span class="sxs-lookup"><span data-stu-id="d4a68-154">-ServerName</span></span>
<span data-ttu-id="d4a68-155">Gibt den Namen des Servers an, der den elastischen Pool hostet.</span><span class="sxs-lookup"><span data-stu-id="d4a68-155">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="d4a68-156">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="d4a68-156">-StorageMB</span></span>
<span data-ttu-id="d4a68-157">Gibt den Speichergrenzwert für den elastischen Pool in Megabyte an.</span><span class="sxs-lookup"><span data-stu-id="d4a68-157">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="d4a68-158">Wenn Sie diesen Parameter nicht angeben, berechnet dieses Cmdlet einen Wert, der vom Wert des *DTU* -Parameters abhängt.</span><span class="sxs-lookup"><span data-stu-id="d4a68-158">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>

<span data-ttu-id="d4a68-159">Siehe [eDTU-und Speichergrenzwerte](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) für mögliche Werte.</span><span class="sxs-lookup"><span data-stu-id="d4a68-159">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a68-160">-Tags</span><span class="sxs-lookup"><span data-stu-id="d4a68-160">-Tags</span></span>
<span data-ttu-id="d4a68-161">Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren in Form einer Hashtabelle an, die dieses Cmdlet dem elastischen Pool zuordnet.</span><span class="sxs-lookup"><span data-stu-id="d4a68-161">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="d4a68-162">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d4a68-162">For example:</span></span>

<span data-ttu-id="d4a68-163">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="d4a68-163">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a68-164">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4a68-164">-Confirm</span></span>
<span data-ttu-id="d4a68-165">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4a68-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4a68-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4a68-166">-WhatIf</span></span>
<span data-ttu-id="d4a68-167">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4a68-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4a68-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4a68-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4a68-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a68-169">-DefaultProfile</span></span>
<span data-ttu-id="d4a68-170">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4a68-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4a68-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a68-171">CommonParameters</span></span>
<span data-ttu-id="d4a68-172">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4a68-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a68-173">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4a68-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a68-174">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4a68-174">INPUTS</span></span>

## <span data-ttu-id="d4a68-175">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4a68-175">OUTPUTS</span></span>

### <span data-ttu-id="d4a68-176">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="d4a68-176">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="d4a68-177">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4a68-177">NOTES</span></span>

## <span data-ttu-id="d4a68-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4a68-178">RELATED LINKS</span></span>

[<span data-ttu-id="d4a68-179">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d4a68-179">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="d4a68-180">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="d4a68-180">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="d4a68-181">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="d4a68-181">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="d4a68-182">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d4a68-182">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="d4a68-183">Satz-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d4a68-183">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="d4a68-184">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="d4a68-184">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
