---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35e29655e8447644b6c5449309424595e45ca187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413063"
---
# <span data-ttu-id="17da5-101">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="17da5-101">Start-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="17da5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17da5-102">SYNOPSIS</span></span>
<span data-ttu-id="17da5-103">Startet einen Kopiervorgang einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="17da5-103">Starts a copy operation of an Azure SQL Database.</span></span>

## <span data-ttu-id="17da5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17da5-104">SYNTAX</span></span>

### <span data-ttu-id="17da5-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="17da5-105">ByInputObject</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17da5-106">ByInputObjectContinuous</span><span class="sxs-lookup"><span data-stu-id="17da5-106">ByInputObjectContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17da5-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="17da5-107">ByDatabaseName</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17da5-108">ByDatabaseNameContinuous</span><span class="sxs-lookup"><span data-stu-id="17da5-108">ByDatabaseNameContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17da5-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17da5-109">DESCRIPTION</span></span>
<span data-ttu-id="17da5-110">Das **Cmdlet "Start-AzureSqlDatabaseCopy"** startet einen einmaligen Kopiervorgang oder einen kontinuierlichen Kopiervorgang einer bestimmten Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="17da5-110">The **Start-AzureSqlDatabaseCopy** cmdlet starts a one-time copy operation or a continuous copy operation of a specific Azure SQL Database.</span></span>
<span data-ttu-id="17da5-111">Dieses Cmdlet ist keine Transaktion.</span><span class="sxs-lookup"><span data-stu-id="17da5-111">This cmdlet is not transactional.</span></span>

<span data-ttu-id="17da5-112">Die ursprüngliche Datenbank ist die Quelldatenbank.</span><span class="sxs-lookup"><span data-stu-id="17da5-112">The original database is the source database.</span></span>
<span data-ttu-id="17da5-113">Die Kopie ist die sekundäre Oder Zieldatenbank.</span><span class="sxs-lookup"><span data-stu-id="17da5-113">The copy is the secondary or target database.</span></span>
<span data-ttu-id="17da5-114">Bei einer fortlaufenden Kopie können sich die Quell- und Zieldatenbanken nicht auf demselben Server befinden, und die Server, die als Host für die Quell- und Zieldatenbanken verwendet werden, müssen Teil desselben Abonnements sein.</span><span class="sxs-lookup"><span data-stu-id="17da5-114">For a continuous copy, the source and target databases cannot reside on the same server, and the servers that host the source and target databases must be part of the same subscription.</span></span>

<span data-ttu-id="17da5-115">Wenn Sie den Parameter *"ContinuousCopy" nicht* angeben, erstellt dieses Cmdlet eine einmalkopie der Quelldatenbank.</span><span class="sxs-lookup"><span data-stu-id="17da5-115">If you do not specify the *ContinuousCopy* parameter, this cmdlet creates a one-time copy of the source database.</span></span>
<span data-ttu-id="17da5-116">Wenn die Antwort empfangen wird, kann der Vorgang noch ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="17da5-116">When the response is received, the operation can still be in progress.</span></span>
<span data-ttu-id="17da5-117">Sie können den Vorgang mithilfe des cmdlets Get-AzureSqlDatabaseCopy oder Get-AzureSqlDatabaseOperation überwachen.</span><span class="sxs-lookup"><span data-stu-id="17da5-117">You can monitor the operation by using the Get-AzureSqlDatabaseCopy or Get-AzureSqlDatabaseOperation cmdlet.</span></span>

<span data-ttu-id="17da5-118">Wenn Sie *"ContinuousCopy"* angeben, erstellt dieses Cmdlet eine fortlaufende Kopie der Quelldatenbank.</span><span class="sxs-lookup"><span data-stu-id="17da5-118">If you specify *ContinuousCopy*, this cmdlet creates a continuous copy of the source database.</span></span>
<span data-ttu-id="17da5-119">Wenn die Antwort empfangen wird, wird der Vorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17da5-119">When the response is received, the operation will be in progress.</span></span>
<span data-ttu-id="17da5-120">Sie können den Vorgang mithilfe von **"Get-AzureSqlDatabaseCopy"** oder **"Get-AzureSqlDatabaseOperation" überwachen.**</span><span class="sxs-lookup"><span data-stu-id="17da5-120">You can monitor the operation by using **Get-AzureSqlDatabaseCopy** or **Get-AzureSqlDatabaseOperation**.</span></span>

<span data-ttu-id="17da5-121">Sie können eine fortlaufende Kopie als Online- oder Offlinedatenbank erstellen.</span><span class="sxs-lookup"><span data-stu-id="17da5-121">You can create a continuous copy as an online or offline database.</span></span>
<span data-ttu-id="17da5-122">Die fortlaufende Onlinekopie wird zum Konfigurieren von active Geo-Replication für Azure SQL https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ verwendet.</span><span class="sxs-lookup"><span data-stu-id="17da5-122">The online continuous copy is used to configure Active Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/.</span></span>
<span data-ttu-id="17da5-123">Die fortlaufende Offlinekopie wird verwendet, um Standard-Geo-Replication für Azure SQL zu https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="17da5-123">The offline continuous copy is used to configure Standard Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/.</span></span>

## <span data-ttu-id="17da5-124">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="17da5-124">EXAMPLES</span></span>

### <span data-ttu-id="17da5-125">Beispiel 1: Planen einer fortlaufenden Datenbankkopie</span><span class="sxs-lookup"><span data-stu-id="17da5-125">Example 1: Schedule a continuous database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

<span data-ttu-id="17da5-126">Mit diesem Befehl wird eine fortlaufende Kopie der Datenbank mit dem Namen "Orders" auf dem Server mit dem Namen "lpqd0zbr8y" geplant.</span><span class="sxs-lookup"><span data-stu-id="17da5-126">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="17da5-127">Der Befehl erstellt eine Zieldatenbank auf dem Server mit dem Namen bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="17da5-127">The command creates a target database on the server named bk0b8kf658.</span></span>

### <span data-ttu-id="17da5-128">Beispiel 2: Erstellen einer Einmalkopie auf demselben Server</span><span class="sxs-lookup"><span data-stu-id="17da5-128">Example 2: Create a one-time copy on the same server</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

<span data-ttu-id="17da5-129">Mit diesem Befehl wird eine Einmalkopie der Datenbank mit dem Namen "Orders" auf dem Server mit dem Namen "lpqd0zbr8y" erstellt.</span><span class="sxs-lookup"><span data-stu-id="17da5-129">This command creates a one-time copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="17da5-130">Mit dem Befehl wird eine Kopie mit dem Namen "OrdersCopy" auf demselben Server erstellt.</span><span class="sxs-lookup"><span data-stu-id="17da5-130">The command creates a copy named OrdersCopy on the same server.</span></span>

### <span data-ttu-id="17da5-131">Beispiel 3: Planen einer fortlaufenden Offlinedatenbankkopie</span><span class="sxs-lookup"><span data-stu-id="17da5-131">Example 3: Schedule a continuous offline database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

<span data-ttu-id="17da5-132">Mit diesem Befehl wird eine fortlaufende Kopie der Datenbank mit dem Namen "Orders" auf dem Server mit dem Namen "lpqd0zbr8y" geplant.</span><span class="sxs-lookup"><span data-stu-id="17da5-132">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="17da5-133">Mit diesem Befehl wird eine Offlinezieldatenbank auf dem Server mit dem Namen bk0b8kf658 erstellt.</span><span class="sxs-lookup"><span data-stu-id="17da5-133">This command creates an offline target database on the server named bk0b8kf658.</span></span>

## <span data-ttu-id="17da5-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17da5-134">PARAMETERS</span></span>

### <span data-ttu-id="17da5-135">-ContinuousCopy</span><span class="sxs-lookup"><span data-stu-id="17da5-135">-ContinuousCopy</span></span>
<span data-ttu-id="17da5-136">Gibt an, dass die Datenbankkopie eine fortlaufende Kopie (eine Replikatdatenbank) ist.</span><span class="sxs-lookup"><span data-stu-id="17da5-136">Indicates that the database copy will be a continuous-copy (a replica database).</span></span>
<span data-ttu-id="17da5-137">Kontinuierliches Kopieren wird auf demselben Server nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="17da5-137">Continuous copy is not supported within the same server.</span></span>
<span data-ttu-id="17da5-138">Wenn dieser Parameter nicht angegeben wird, wird eine Einmalkopie ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17da5-138">If this parameter is not specified, then a one-time copy is performed.</span></span>
<span data-ttu-id="17da5-139">Bei einer einmal erstellten Kopie müssen sich die Quell- und Partnerdatenbank auf demselben Server befinden.</span><span class="sxs-lookup"><span data-stu-id="17da5-139">For a one-time copy, the source and partner databases must be on the same server.</span></span>

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

### <span data-ttu-id="17da5-140">-Database</span><span class="sxs-lookup"><span data-stu-id="17da5-140">-Database</span></span>
<span data-ttu-id="17da5-141">Gibt ein Objekt an, das die Azure SQL darstellt.</span><span class="sxs-lookup"><span data-stu-id="17da5-141">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="17da5-142">Dieser Parameter akzeptiert die Pipelineeingabe.</span><span class="sxs-lookup"><span data-stu-id="17da5-142">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="17da5-143">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="17da5-143">-DatabaseName</span></span>
<span data-ttu-id="17da5-144">Gibt den Namen der Quelldatenbank an.</span><span class="sxs-lookup"><span data-stu-id="17da5-144">Specifies the name of the source database.</span></span>

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

### <span data-ttu-id="17da5-145">-Force</span><span class="sxs-lookup"><span data-stu-id="17da5-145">-Force</span></span>
<span data-ttu-id="17da5-146">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="17da5-146">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="17da5-147">-OfflineSecondary</span><span class="sxs-lookup"><span data-stu-id="17da5-147">-OfflineSecondary</span></span>
<span data-ttu-id="17da5-148">Gibt an, dass eine fortlaufende Kopie keine aktive Kopie, sondern eine passive Kopie ist.</span><span class="sxs-lookup"><span data-stu-id="17da5-148">Specifies that a continuous copy is a passive copy rather than an active copy.</span></span>
<span data-ttu-id="17da5-149">Wenn es sich bei der Quelldatenbank um eine Standardeditionsdatenbank handelt, ist dieser Parameter erforderlich.</span><span class="sxs-lookup"><span data-stu-id="17da5-149">If the source database is a Standard edition database, then this parameter is required.</span></span>
<span data-ttu-id="17da5-150">Wenn dieser Parameter angegeben wird, muss *auch "ContinuousCopy"* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="17da5-150">If this parameter is specified then *ContinuousCopy* must also be specified.</span></span>

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

### <span data-ttu-id="17da5-151">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="17da5-151">-PartnerDatabase</span></span>
<span data-ttu-id="17da5-152">Gibt den Namen der Zieldatenbank an.</span><span class="sxs-lookup"><span data-stu-id="17da5-152">Specifies name of the target database.</span></span>
<span data-ttu-id="17da5-153">Wenn Sie den Parameter *"ContinuousCopy"* angeben, muss der Wert für *"PartnerDatabase"* mit dem Namen der Quelldatenbank übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="17da5-153">If you specify the *ContinuousCopy* parameter, the value for *PartnerDatabase* must match the name of the source database.</span></span>
<span data-ttu-id="17da5-154">Wenn Sie *"ContinuousCopy" nicht* angeben, müssen Sie einen Namen für die Zieldatenbank angeben, der sich vom Quelldatenbanknamen unterscheiden kann.</span><span class="sxs-lookup"><span data-stu-id="17da5-154">If you do not specify *ContinuousCopy*, you must specify a name for the target database, which can be different from the source database name.</span></span>

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

### <span data-ttu-id="17da5-155">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="17da5-155">-PartnerServer</span></span>
<span data-ttu-id="17da5-156">Gibt den Namen des Servers an, der die Zieldatenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="17da5-156">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="17da5-157">Dieser Server muss im selben Abonnement wie der Quelldatenbankserver vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="17da5-157">This server must be in the same Azure subscription as the source database server.</span></span>

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

### <span data-ttu-id="17da5-158">-Profile</span><span class="sxs-lookup"><span data-stu-id="17da5-158">-Profile</span></span>
<span data-ttu-id="17da5-159">Gibt das Azure-Profil an, aus dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="17da5-159">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="17da5-160">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="17da5-160">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="17da5-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="17da5-161">-ServerName</span></span>
<span data-ttu-id="17da5-162">Gibt den Namen des Servers an, auf dem sich die Quelldatenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="17da5-162">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="17da5-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17da5-163">-Confirm</span></span>
<span data-ttu-id="17da5-164">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="17da5-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17da5-165">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="17da5-165">-WhatIf</span></span>
<span data-ttu-id="17da5-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="17da5-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17da5-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17da5-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17da5-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17da5-168">CommonParameters</span></span>
<span data-ttu-id="17da5-169">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17da5-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17da5-170">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17da5-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17da5-171">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="17da5-171">INPUTS</span></span>

### <span data-ttu-id="17da5-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="17da5-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="17da5-173">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="17da5-173">OUTPUTS</span></span>

### <span data-ttu-id="17da5-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="17da5-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="17da5-175">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="17da5-175">NOTES</span></span>
* <span data-ttu-id="17da5-176">Authentifizierung: Für dieses Cmdlet ist zertifikatbasierte Authentifizierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="17da5-176">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="17da5-177">Ein Beispiel für die Verwendung der zertifikatbasierten Authentifizierung zum Festlegen des aktuellen Abonnements finden Sie unter New-AzureSqlDatabaseServerContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17da5-177">For an example of how to use certificate-based authentication to set the current subscription, see New-AzureSqlDatabaseServerContext cmdlet.</span></span>
* <span data-ttu-id="17da5-178">Überwachung: Verwenden Sie das **Cmdlet "Get-AzureSqlDatabaseCopy",** um den Status einer oder mehreren kontinuierlichen Kopierbeziehungen zu überprüfen, die auf dem Server aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="17da5-178">Monitoring: To check for the status of one or more continuous copy relationships that are active on the server, use the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span> <span data-ttu-id="17da5-179">Verwenden Sie das Cmdlet **"Get-AzureSqlDatabaseOperation",** um den Status der Vorgänge sowohl an der Quelle als auch an dem Ziel der fortlaufenden Kopierbeziehung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="17da5-179">To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="17da5-180">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="17da5-180">RELATED LINKS</span></span>

[<span data-ttu-id="17da5-181">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="17da5-181">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="17da5-182">Vorgänge für Azure SQL Datenbanken</span><span class="sxs-lookup"><span data-stu-id="17da5-182">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="17da5-183">Starten einer Datenbankkopie</span><span class="sxs-lookup"><span data-stu-id="17da5-183">Start Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)



[<span data-ttu-id="17da5-184">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="17da5-184">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="17da5-185">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="17da5-185">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


