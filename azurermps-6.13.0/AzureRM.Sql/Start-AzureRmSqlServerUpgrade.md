---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 279216ad20783017f091143a7c440873c8e04946
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481946"
---
# <span data-ttu-id="1a392-101">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="1a392-101">Start-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="1a392-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a392-102">SYNOPSIS</span></span>
<span data-ttu-id="1a392-103">Startet das Upgrade eines SQL-Datenbankservers.</span><span class="sxs-lookup"><span data-stu-id="1a392-103">Starts the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a392-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a392-104">SYNTAX</span></span>

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a392-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a392-105">DESCRIPTION</span></span>
<span data-ttu-id="1a392-106">Das Cmdlet **Start-AzureRmSqlServerUpgrade** startet das Upgrade eines Azure SQL-Datenbankservers, Version 11, auf Version 12.</span><span class="sxs-lookup"><span data-stu-id="1a392-106">The **Start-AzureRmSqlServerUpgrade** cmdlet starts the upgrade of an Azure SQL Database server version 11 to version 12.</span></span>
<span data-ttu-id="1a392-107">Mithilfe des Get-AzureRmSqlServerUpgrade-Cmdlets können Sie den Fortschritt eines Upgrades überwachen.</span><span class="sxs-lookup"><span data-stu-id="1a392-107">You can monitor the progress of an upgrade by using the Get-AzureRmSqlServerUpgrade cmdlet.</span></span>

## <span data-ttu-id="1a392-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a392-108">EXAMPLES</span></span>

### <span data-ttu-id="1a392-109">Beispiel 1: Aktualisieren eines Servers</span><span class="sxs-lookup"><span data-stu-id="1a392-109">Example 1: Upgrade a server</span></span>
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

<span data-ttu-id="1a392-110">Mit diesem Befehl wird der Server namens SERVER01 aktualisiert, der der Ressourcengruppe TesourceGroup01 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1a392-110">This command upgrades the server named server01 assigned to resource group TesourceGroup01.</span></span>

### <span data-ttu-id="1a392-111">Beispiel 2: Aktualisieren eines Servers mithilfe von Planungszeit und Daten Bank Empfehlung</span><span class="sxs-lookup"><span data-stu-id="1a392-111">Example 2: Upgrade a server by using schedule time and database recommendation</span></span>
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

<span data-ttu-id="1a392-112">Der erste Befehl erstellt in Zukunft fünf Minuten mit dem Get-Date-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a392-112">The first command creates a time five minutes in the future by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="1a392-113">Der Befehl speichert das Datum in der Variablen $ScheduleTime.</span><span class="sxs-lookup"><span data-stu-id="1a392-113">The command stores the date in the variable $ScheduleTime.</span></span>
<span data-ttu-id="1a392-114">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="1a392-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="1a392-115">Der zweite Befehl erstellt ein **RecommendedDatabaseProperties** -Objekt und speichert dieses Objekt dann in der Variablen $DatabaseMap.</span><span class="sxs-lookup"><span data-stu-id="1a392-115">The second command creates a **RecommendedDatabaseProperties** object, and then stores that object in the variable $DatabaseMap.</span></span>
<span data-ttu-id="1a392-116">In den nächsten drei Befehlen werden Eigenschaften des Objekts, das in $DatabaseMap gespeichert ist, Werte zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="1a392-116">The next three commands assign values to properties of the object stored in $DatabaseMap.</span></span>
<span data-ttu-id="1a392-117">Mit dem letzten Befehl wird der vorhandene Server Server01 auf Version 12,0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1a392-117">The final command upgrades the existing server named Server01 to version 12.0.</span></span>
<span data-ttu-id="1a392-118">Der früheste Aktualisierungszeitpunkt ist fünf Minuten nach der Ausführung des Befehls, wie durch die $ScheduleTime-Variable angegeben.</span><span class="sxs-lookup"><span data-stu-id="1a392-118">The earliest time to upgrade is five minutes after you run the command, as specified by the $ScheduleTime variable.</span></span>
<span data-ttu-id="1a392-119">Nach dem Upgrade wird in der Datenbank-contosodb die Standard Edition ausgeführt und der Service Level-Ziel-S0-Wert bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1a392-119">After the upgrade, the database contosodb will be running the Standard edition and have the Service Level Objective S0.</span></span>

## <span data-ttu-id="1a392-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a392-120">PARAMETERS</span></span>

### <span data-ttu-id="1a392-121">-DatabaseCollection</span><span class="sxs-lookup"><span data-stu-id="1a392-121">-DatabaseCollection</span></span>
<span data-ttu-id="1a392-122">Gibt ein Array von **RecommendedDatabaseProperties** -Objekten an, die dieses Cmdlet für das Server Upgrade verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a392-122">Specifies an array of **RecommendedDatabaseProperties** objects that this cmdlet uses for the server upgrade.</span></span>

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a392-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a392-123">-DefaultProfile</span></span>
<span data-ttu-id="1a392-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1a392-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a392-125">-ElasticPoolCollection</span><span class="sxs-lookup"><span data-stu-id="1a392-125">-ElasticPoolCollection</span></span>
<span data-ttu-id="1a392-126">Gibt ein Array von **UpgradeRecommendedElasticPoolProperties** -Objekten an, die für das Server Upgrade verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1a392-126">Specifies an array of **UpgradeRecommendedElasticPoolProperties** objects to use for the server upgrade.</span></span>

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a392-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a392-127">-ResourceGroupName</span></span>
<span data-ttu-id="1a392-128">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="1a392-128">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="1a392-129">-ScheduleUpgradeAfterUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="1a392-129">-ScheduleUpgradeAfterUtcDateTime</span></span>
<span data-ttu-id="1a392-130">Gibt den frühesten Zeitpunkt als **DateTime** -Objekt an, um den Server zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1a392-130">Specifies the earliest time, as a **DateTime** object, to upgrade the server.</span></span>
<span data-ttu-id="1a392-131">Geben Sie einen Wert im ISO8601-Format in koordinierter Weltzeit (Coordinated Universal Time, UTC) an.</span><span class="sxs-lookup"><span data-stu-id="1a392-131">Specify a value in the ISO8601 format, in Coordinated Universal Time (UTC).</span></span>
<span data-ttu-id="1a392-132">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="1a392-132">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a392-133">-Servername</span><span class="sxs-lookup"><span data-stu-id="1a392-133">-ServerName</span></span>
<span data-ttu-id="1a392-134">Gibt den Namen des Servers an, der vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="1a392-134">Specifies the name of the server that this cmdlet upgrades.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a392-135">-Server Version vom</span><span class="sxs-lookup"><span data-stu-id="1a392-135">-ServerVersion</span></span>
<span data-ttu-id="1a392-136">Gibt die Version an, auf die das Cmdlet den Server aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1a392-136">Specifies the version to which this cmdlet upgrades the server.</span></span>
<span data-ttu-id="1a392-137">Der einzige gültige Wert ist 12,0.</span><span class="sxs-lookup"><span data-stu-id="1a392-137">The only valid value is 12.0.</span></span>

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

### <span data-ttu-id="1a392-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a392-138">CommonParameters</span></span>
<span data-ttu-id="1a392-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a392-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a392-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a392-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a392-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a392-141">INPUTS</span></span>

### <span data-ttu-id="1a392-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1a392-142">System.String</span></span>

## <span data-ttu-id="1a392-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a392-143">OUTPUTS</span></span>

### <span data-ttu-id="1a392-144">Microsoft. Azure. Commands. SQL. Serverupgrade. Model. AzureSqlServerUpgradeStartModel</span><span class="sxs-lookup"><span data-stu-id="1a392-144">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeStartModel</span></span>

## <span data-ttu-id="1a392-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a392-145">NOTES</span></span>

## <span data-ttu-id="1a392-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a392-146">RELATED LINKS</span></span>

[<span data-ttu-id="1a392-147">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="1a392-147">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="1a392-148">Stopp-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="1a392-148">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="1a392-149">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="1a392-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


