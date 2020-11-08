---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006051"
---
# <span data-ttu-id="8396b-101">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8396b-101">Start-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="8396b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8396b-102">SYNOPSIS</span></span>
<span data-ttu-id="8396b-103">Startet einen Kopiervorgang einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8396b-103">Starts a copy operation of an Azure SQL Database.</span></span>

## <span data-ttu-id="8396b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8396b-104">SYNTAX</span></span>

### <span data-ttu-id="8396b-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8396b-105">ByInputObject</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8396b-106">ByInputObjectContinuous</span><span class="sxs-lookup"><span data-stu-id="8396b-106">ByInputObjectContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8396b-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8396b-107">ByDatabaseName</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8396b-108">ByDatabaseNameContinuous</span><span class="sxs-lookup"><span data-stu-id="8396b-108">ByDatabaseNameContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8396b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8396b-109">DESCRIPTION</span></span>
<span data-ttu-id="8396b-110">Das Cmdlet **Start-AzureSqlDatabaseCopy** startet einen einmaligen Kopiervorgang oder einen fortlaufenden Kopiervorgang einer bestimmten Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8396b-110">The **Start-AzureSqlDatabaseCopy** cmdlet starts a one-time copy operation or a continuous copy operation of a specific Azure SQL Database.</span></span>
<span data-ttu-id="8396b-111">Dieses Cmdlet ist nicht transaktional.</span><span class="sxs-lookup"><span data-stu-id="8396b-111">This cmdlet is not transactional.</span></span>

<span data-ttu-id="8396b-112">Die ursprüngliche Datenbank ist die Quelldatenbank.</span><span class="sxs-lookup"><span data-stu-id="8396b-112">The original database is the source database.</span></span>
<span data-ttu-id="8396b-113">Die Kopie ist die sekundäre oder Zieldatenbank.</span><span class="sxs-lookup"><span data-stu-id="8396b-113">The copy is the secondary or target database.</span></span>
<span data-ttu-id="8396b-114">Bei einer fortlaufenden Kopie können sich die Quell-und Zieldatenbanken nicht auf demselben Server befinden, und die Server, die die Quell-und Zieldatenbanken hosten, müssen Teil desselben Abonnements sein.</span><span class="sxs-lookup"><span data-stu-id="8396b-114">For a continuous copy, the source and target databases cannot reside on the same server, and the servers that host the source and target databases must be part of the same subscription.</span></span>

<span data-ttu-id="8396b-115">Wenn Sie den *ContinuousCopy* -Parameter nicht angeben, erstellt dieses Cmdlet eine einmalige Kopie der Quelldatenbank.</span><span class="sxs-lookup"><span data-stu-id="8396b-115">If you do not specify the *ContinuousCopy* parameter, this cmdlet creates a one-time copy of the source database.</span></span>
<span data-ttu-id="8396b-116">Wenn die Antwort empfangen wird, kann der Vorgang weiterhin ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8396b-116">When the response is received, the operation can still be in progress.</span></span>
<span data-ttu-id="8396b-117">Sie können den Vorgang mithilfe des Get-AzureSqlDatabaseCopy-oder Get-AzureSqlDatabaseOperation-Cmdlets überwachen.</span><span class="sxs-lookup"><span data-stu-id="8396b-117">You can monitor the operation by using the Get-AzureSqlDatabaseCopy or Get-AzureSqlDatabaseOperation cmdlet.</span></span>

<span data-ttu-id="8396b-118">Wenn Sie *ContinuousCopy* angeben, erstellt dieses Cmdlet eine fortlaufende Kopie der Quelldatenbank.</span><span class="sxs-lookup"><span data-stu-id="8396b-118">If you specify *ContinuousCopy* , this cmdlet creates a continuous copy of the source database.</span></span>
<span data-ttu-id="8396b-119">Wenn die Antwort empfangen wird, wird der Vorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8396b-119">When the response is received, the operation will be in progress.</span></span>
<span data-ttu-id="8396b-120">Sie können den Vorgang mithilfe von **Get-AzureSqlDatabaseCopy** oder **Get-AzureSqlDatabaseOperation** überwachen.</span><span class="sxs-lookup"><span data-stu-id="8396b-120">You can monitor the operation by using **Get-AzureSqlDatabaseCopy** or **Get-AzureSqlDatabaseOperation**.</span></span>

<span data-ttu-id="8396b-121">Sie können eine fortlaufende Kopie als Online-oder Offlinedatenbank erstellen.</span><span class="sxs-lookup"><span data-stu-id="8396b-121">You can create a continuous copy as an online or offline database.</span></span>
<span data-ttu-id="8396b-122">Die fortlaufende Onlinekopie wird verwendet, um Active Geo-Replication für Azure SQL-Datenbank zu konfigurieren https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ .</span><span class="sxs-lookup"><span data-stu-id="8396b-122">The online continuous copy is used to configure Active Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/.</span></span>
<span data-ttu-id="8396b-123">Die fortlaufende Offlinekopie wird verwendet, um die Standard Geo-Replication für Azure SQL-Datenbank zu konfigurieren https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ .</span><span class="sxs-lookup"><span data-stu-id="8396b-123">The offline continuous copy is used to configure Standard Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/.</span></span>

## <span data-ttu-id="8396b-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8396b-124">EXAMPLES</span></span>

### <span data-ttu-id="8396b-125">Beispiel 1: Planen einer fortlaufenden Datenbankkopie</span><span class="sxs-lookup"><span data-stu-id="8396b-125">Example 1: Schedule a continuous database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

<span data-ttu-id="8396b-126">Dieser Befehl plant eine fortlaufende Kopie der Datenbank mit dem Namen "Aufträge" auf dem Server mit dem Namen lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="8396b-126">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="8396b-127">Der Befehl erstellt eine Zieldatenbank auf dem Server mit dem Namen bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="8396b-127">The command creates a target database on the server named bk0b8kf658.</span></span>

### <span data-ttu-id="8396b-128">Beispiel 2: Erstellen einer einmaligen Kopie auf dem gleichen Server</span><span class="sxs-lookup"><span data-stu-id="8396b-128">Example 2: Create a one-time copy on the same server</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

<span data-ttu-id="8396b-129">Mit diesem Befehl wird eine einmalige Kopie der Datenbank mit dem Namen "Aufträge" auf dem Server mit dem Namen "lpqd0zbr8y" erstellt.</span><span class="sxs-lookup"><span data-stu-id="8396b-129">This command creates a one-time copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="8396b-130">Der Befehl erstellt eine Kopie mit dem Namen OrdersCopy auf demselben Server.</span><span class="sxs-lookup"><span data-stu-id="8396b-130">The command creates a copy named OrdersCopy on the same server.</span></span>

### <span data-ttu-id="8396b-131">Beispiel 3: Planen einer fortlaufenden Offline-Datenbankkopie</span><span class="sxs-lookup"><span data-stu-id="8396b-131">Example 3: Schedule a continuous offline database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

<span data-ttu-id="8396b-132">Dieser Befehl plant eine fortlaufende Kopie der Datenbank mit dem Namen "Aufträge" auf dem Server mit dem Namen lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="8396b-132">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="8396b-133">Dieser Befehl erstellt eine Offline Zieldatenbank auf dem Server mit dem Namen bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="8396b-133">This command creates an offline target database on the server named bk0b8kf658.</span></span>

## <span data-ttu-id="8396b-134">Parameter</span><span class="sxs-lookup"><span data-stu-id="8396b-134">PARAMETERS</span></span>

### <span data-ttu-id="8396b-135">-ContinuousCopy</span><span class="sxs-lookup"><span data-stu-id="8396b-135">-ContinuousCopy</span></span>
<span data-ttu-id="8396b-136">Gibt an, dass es sich bei der Datenbankkopie um eine fortlaufende Kopie (eine Replikatdatenbank) handelt.</span><span class="sxs-lookup"><span data-stu-id="8396b-136">Indicates that the database copy will be a continuous-copy (a replica database).</span></span>
<span data-ttu-id="8396b-137">Die fortlaufende Kopie wird nicht innerhalb desselben Servers unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8396b-137">Continuous copy is not supported within the same server.</span></span>
<span data-ttu-id="8396b-138">Wenn dieser Parameter nicht angegeben wird, wird eine einmalige Kopie ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8396b-138">If this parameter is not specified, then a one-time copy is performed.</span></span>
<span data-ttu-id="8396b-139">Bei einer einmaligen Kopie müssen sich die Quell-und Partner Datenbanken auf demselben Server befinden.</span><span class="sxs-lookup"><span data-stu-id="8396b-139">For a one-time copy, the source and partner databases must be on the same server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8396b-140">-Datenbank</span><span class="sxs-lookup"><span data-stu-id="8396b-140">-Database</span></span>
<span data-ttu-id="8396b-141">Gibt ein Objekt an, das die Azure SQL-Quelldatenbank darstellt.</span><span class="sxs-lookup"><span data-stu-id="8396b-141">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="8396b-142">Dieser Parameter akzeptiert Pipelineeingaben.</span><span class="sxs-lookup"><span data-stu-id="8396b-142">This parameter accepts pipeline input.</span></span>

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8396b-143">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8396b-143">-DatabaseName</span></span>
<span data-ttu-id="8396b-144">Gibt den Namen der Quelldatenbank an.</span><span class="sxs-lookup"><span data-stu-id="8396b-144">Specifies the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8396b-145">-Force</span><span class="sxs-lookup"><span data-stu-id="8396b-145">-Force</span></span>
<span data-ttu-id="8396b-146">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8396b-146">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8396b-147">-OfflineSecondary</span><span class="sxs-lookup"><span data-stu-id="8396b-147">-OfflineSecondary</span></span>
<span data-ttu-id="8396b-148">Gibt an, dass eine fortlaufende Kopie eine passive Kopie und keine aktive Kopie ist.</span><span class="sxs-lookup"><span data-stu-id="8396b-148">Specifies that a continuous copy is a passive copy rather than an active copy.</span></span>
<span data-ttu-id="8396b-149">Wenn es sich bei der Quelldatenbank um eine Standard Edition-Datenbank handelt, ist dieser Parameter erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8396b-149">If the source database is a Standard edition database, then this parameter is required.</span></span>
<span data-ttu-id="8396b-150">Wenn dieser Parameter angegeben wird, muss auch *ContinuousCopy* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8396b-150">If this parameter is specified then *ContinuousCopy* must also be specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8396b-151">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="8396b-151">-PartnerDatabase</span></span>
<span data-ttu-id="8396b-152">Gibt den Namen der Zieldatenbank an.</span><span class="sxs-lookup"><span data-stu-id="8396b-152">Specifies name of the target database.</span></span>
<span data-ttu-id="8396b-153">Wenn Sie den *ContinuousCopy* -Parameter angeben, muss der Wert für *PartnerDatabase* mit dem Namen der Quelldatenbank übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="8396b-153">If you specify the *ContinuousCopy* parameter, the value for *PartnerDatabase* must match the name of the source database.</span></span>
<span data-ttu-id="8396b-154">Wenn Sie *ContinuousCopy* nicht angeben, müssen Sie einen Namen für die Zieldatenbank angeben, der vom Namen der Quelldatenbank abweichen kann.</span><span class="sxs-lookup"><span data-stu-id="8396b-154">If you do not specify *ContinuousCopy* , you must specify a name for the target database, which can be different from the source database name.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8396b-155">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="8396b-155">-PartnerServer</span></span>
<span data-ttu-id="8396b-156">Gibt den Namen des Servers an, der die Zieldatenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="8396b-156">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="8396b-157">Dieser Server muss sich im gleichen Azure-Abonnement wie der Quelldatenbankserver befinden.</span><span class="sxs-lookup"><span data-stu-id="8396b-157">This server must be in the same Azure subscription as the source database server.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8396b-158">-Profil</span><span class="sxs-lookup"><span data-stu-id="8396b-158">-Profile</span></span>
<span data-ttu-id="8396b-159">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8396b-159">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8396b-160">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8396b-160">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8396b-161">-Servername</span><span class="sxs-lookup"><span data-stu-id="8396b-161">-ServerName</span></span>
<span data-ttu-id="8396b-162">Gibt den Namen des Servers an, auf dem sich die Quelldatenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="8396b-162">Specifies the name of the server on which the source database resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8396b-163">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8396b-163">-Confirm</span></span>
<span data-ttu-id="8396b-164">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8396b-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8396b-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8396b-165">-WhatIf</span></span>
<span data-ttu-id="8396b-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8396b-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8396b-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8396b-167">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8396b-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8396b-168">CommonParameters</span></span>
<span data-ttu-id="8396b-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8396b-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8396b-170">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8396b-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8396b-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8396b-171">INPUTS</span></span>

### <span data-ttu-id="8396b-172">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="8396b-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="8396b-173">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8396b-173">OUTPUTS</span></span>

### <span data-ttu-id="8396b-174">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8396b-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="8396b-175">Notizen</span><span class="sxs-lookup"><span data-stu-id="8396b-175">NOTES</span></span>
* <span data-ttu-id="8396b-176">Authentifizierung: Dieses Cmdlet erfordert zertifikatbasierte Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="8396b-176">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="8396b-177">Ein Beispiel für die Verwendung der zertifikatbasierten Authentifizierung zum Einrichten des aktuellen Abonnements finden Sie unter New-AzureSqlDatabaseServerContext-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="8396b-177">For an example of how to use certificate-based authentication to set the current subscription, see New-AzureSqlDatabaseServerContext cmdlet.</span></span>
* <span data-ttu-id="8396b-178">Überwachung: Verwenden Sie das Cmdlet " **Get-AzureSqlDatabaseCopy** ", um den Status einer oder mehrerer kontinuierlicher Kopier Beziehungen zu überprüfen, die auf dem Server aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="8396b-178">Monitoring: To check for the status of one or more continuous copy relationships that are active on the server, use the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span> <span data-ttu-id="8396b-179">Verwenden Sie das Cmdlet **Get-AzureSqlDatabaseOperation** , um den Status der Vorgänge sowohl auf Quelle als auch auf Ziel der fortlaufenden Kopie-Beziehung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8396b-179">To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="8396b-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8396b-180">RELATED LINKS</span></span>

[<span data-ttu-id="8396b-181">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="8396b-181">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="8396b-182">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="8396b-182">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="8396b-183">Datenbankkopie starten</span><span class="sxs-lookup"><span data-stu-id="8396b-183">Start Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[<span data-ttu-id="8396b-184">Azure SQL-Datenbank-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8396b-184">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="8396b-185">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8396b-185">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="8396b-186">Stopp-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8396b-186">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


