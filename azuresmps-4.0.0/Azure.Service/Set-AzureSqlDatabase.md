---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 82F4DB8F-8DAF-40D2-8031-3EDBF5D08417
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6274d3851042c15791707807471ae1bc6a2733ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006071"
---
# <span data-ttu-id="b9b66-101">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b9b66-101">Set-AzureSqlDatabase</span></span>

## <span data-ttu-id="b9b66-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9b66-102">SYNOPSIS</span></span>
<span data-ttu-id="b9b66-103">Legt Eigenschaften für eine Azure SQL-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="b9b66-103">Sets properties for an Azure SQL Database.</span></span>

## <span data-ttu-id="b9b66-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9b66-104">SYNTAX</span></span>

### <span data-ttu-id="b9b66-105">ByNameWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="b9b66-105">ByNameWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9b66-106">ByObjectWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="b9b66-106">ByObjectWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9b66-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="b9b66-107">ByNameWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9b66-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="b9b66-108">ByObjectWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -Database <Database> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9b66-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9b66-109">DESCRIPTION</span></span>
<span data-ttu-id="b9b66-110">Das Cmdlet " **Set-AzureSqlDatabase** " legt Eigenschaften für eine Azure SQL-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="b9b66-110">The **Set-AzureSqlDatabase** cmdlet sets properties for an Azure SQL Database.</span></span>
<span data-ttu-id="b9b66-111">Sie können die Datenbank nach Namen angeben oder ein Azure SQL-Datenbankobjekt über die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="b9b66-111">You can specify the database by name, or pass an Azure SQL Database object through the pipeline.</span></span>
<span data-ttu-id="b9b66-112">Sie können den Server nach Namen angeben oder einen Azure SQL-Datenbankserver-Verbindungskontext übergeben.</span><span class="sxs-lookup"><span data-stu-id="b9b66-112">You can specify the server by name, or pass an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="b9b66-113">Erstellen Sie einen Verbindungskontext, indem Sie das Cmdlet **New-AzureSqlDatabaseServerContext** ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9b66-113">Create a connection context by running the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="b9b66-114">Wenn Sie den Server nach Namen angeben, verwendet das Cmdlet die aktuellen Azure-Abonnementinformationen, um die Anforderung zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="b9b66-114">If you specify the server by name, the cmdlet uses the current Azure subscription information to authenticate the request.</span></span>

## <span data-ttu-id="b9b66-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9b66-115">EXAMPLES</span></span>

### <span data-ttu-id="b9b66-116">Beispiel 1: Ändern der Größe einer Datenbank mithilfe eines Verbindungskontexts</span><span class="sxs-lookup"><span data-stu-id="b9b66-116">Example 1: Change the size of a database by using a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ConnectionContext $Context -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="b9b66-117">In diesem Beispiel wird die Größe der Datenbank mit dem Namen Database01 auf 20 GB im Azure SQL-Datenbankserver-Verbindungskontext $Context geändert.</span><span class="sxs-lookup"><span data-stu-id="b9b66-117">This example changes the size of the database named Database01 to 20 GB, in the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="b9b66-118">Beispiel 2: Ändern der Größe einer Datenbank mit einem Servernamen</span><span class="sxs-lookup"><span data-stu-id="b9b66-118">Example 2: Change the size of a database by using a server name</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ServerName "lpqd0zbr8y" -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="b9b66-119">In diesem Beispiel wird die Größe der Datenbank mit dem Namen Database01 auf 20 GB auf dem Server mit dem Namen lpqd0zbr8y geändert.</span><span class="sxs-lookup"><span data-stu-id="b9b66-119">This example changes the size of the database named Database01 to 20 GB in the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="b9b66-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9b66-120">PARAMETERS</span></span>

### <span data-ttu-id="b9b66-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="b9b66-121">-ConnectionContext</span></span>
<span data-ttu-id="b9b66-122">Gibt den Verbindungskontext eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="b9b66-122">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9b66-123">-Datenbank</span><span class="sxs-lookup"><span data-stu-id="b9b66-123">-Database</span></span>
<span data-ttu-id="b9b66-124">Gibt ein Objekt an, das die Azure SQL-Datenbank darstellt, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="b9b66-124">Specifies an object that represents the Azure SQL Database that this cmdlet modifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9b66-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b9b66-125">-DatabaseName</span></span>
<span data-ttu-id="b9b66-126">Gibt den Namen der Datenbank an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="b9b66-126">Specifies the name of the database that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b66-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="b9b66-127">-Edition</span></span>
<span data-ttu-id="b9b66-128">Gibt die neue Edition für die Azure SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="b9b66-128">Specifies the new edition for the Azure SQL Database.</span></span>
<span data-ttu-id="b9b66-129">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b9b66-129">Valid values are:</span></span> 

- <span data-ttu-id="b9b66-130">Keine</span><span class="sxs-lookup"><span data-stu-id="b9b66-130">None</span></span>
- <span data-ttu-id="b9b66-131">Web</span><span class="sxs-lookup"><span data-stu-id="b9b66-131">Web</span></span>
- <span data-ttu-id="b9b66-132">Business</span><span class="sxs-lookup"><span data-stu-id="b9b66-132">Business</span></span>
- <span data-ttu-id="b9b66-133">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="b9b66-133">Basic</span></span>
- <span data-ttu-id="b9b66-134">Standard</span><span class="sxs-lookup"><span data-stu-id="b9b66-134">Standard</span></span>
-  <span data-ttu-id="b9b66-135">Premium</span><span class="sxs-lookup"><span data-stu-id="b9b66-135">Premium</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b66-136">-Force</span><span class="sxs-lookup"><span data-stu-id="b9b66-136">-Force</span></span>
<span data-ttu-id="b9b66-137">Ermöglicht die Ausführung der Aktion, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="b9b66-137">Allows the action to complete without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="b9b66-138">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="b9b66-138">-MaxSizeBytes</span></span>
<span data-ttu-id="b9b66-139">Gibt die neue maximale Größe für die Datenbank in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="b9b66-139">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="b9b66-140">Sie können entweder diesen Parameter oder den *MaxSizeGB* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="b9b66-140">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="b9b66-141">Sehen Sie sich den *MaxSizeGB* -Parameter für akzeptable Werte auf der Grundlage der Edition an.</span><span class="sxs-lookup"><span data-stu-id="b9b66-141">See the *MaxSizeGB* parameter for acceptable values based on edition.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b66-142">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="b9b66-142">-MaxSizeGB</span></span>
<span data-ttu-id="b9b66-143">Gibt die neue maximale Größe für die Datenbank in Gigabyte an.</span><span class="sxs-lookup"><span data-stu-id="b9b66-143">Specifies the new maximum size for the database in gigabytes.</span></span>
<span data-ttu-id="b9b66-144">Sie können entweder diesen Parameter oder den *MaxSizeBytes* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="b9b66-144">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="b9b66-145">Die akzeptablen Werte unterscheiden sich je nach Edition.</span><span class="sxs-lookup"><span data-stu-id="b9b66-145">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="b9b66-146">Grundlegende Editions Werte: 1 oder 2</span><span class="sxs-lookup"><span data-stu-id="b9b66-146">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="b9b66-147">Standard Editions Werte: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 oder 250</span><span class="sxs-lookup"><span data-stu-id="b9b66-147">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="b9b66-148">Premium Edition-Werte: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 oder 500</span><span class="sxs-lookup"><span data-stu-id="b9b66-148">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="b9b66-149">Web Edition-Werte: 1 oder 5</span><span class="sxs-lookup"><span data-stu-id="b9b66-149">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="b9b66-150">Business Edition-Werte: 10, 20, 30, 40, 50, 100 oder 150</span><span class="sxs-lookup"><span data-stu-id="b9b66-150">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b66-151">-Datenbankname</span><span class="sxs-lookup"><span data-stu-id="b9b66-151">-NewDatabaseName</span></span>
<span data-ttu-id="b9b66-152">Gibt den neuen Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="b9b66-152">Specifies the new name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b66-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9b66-153">-PassThru</span></span>
<span data-ttu-id="b9b66-154">Gibt die aktualisierte Azure SQL-Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="b9b66-154">Returns the updated Azure SQL Database.</span></span>

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

### <span data-ttu-id="b9b66-155">-Profil</span><span class="sxs-lookup"><span data-stu-id="b9b66-155">-Profile</span></span>
<span data-ttu-id="b9b66-156">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b9b66-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b9b66-157">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b9b66-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b9b66-158">-Servername</span><span class="sxs-lookup"><span data-stu-id="b9b66-158">-ServerName</span></span>
<span data-ttu-id="b9b66-159">Gibt den Namen des Servers an, der die Datenbank enthält, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="b9b66-159">Specifies the name of the server that contains the database that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9b66-160">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="b9b66-160">-ServiceObjective</span></span>
<span data-ttu-id="b9b66-161">Gibt ein Objekt an, das das neue Dienst Ziel (Leistungsstufe) für diese Datenbank darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9b66-161">Specifies an object representing the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="b9b66-162">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b9b66-162">Valid values are:</span></span> 

- <span data-ttu-id="b9b66-163">Standard: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="b9b66-163">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="b9b66-164">Standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="b9b66-164">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="b9b66-165">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="b9b66-165">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="b9b66-166">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="b9b66-166">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="b9b66-167">\* Standard (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="b9b66-167">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="b9b66-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="b9b66-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="b9b66-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="b9b66-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="b9b66-170">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="b9b66-170">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="b9b66-171">\* Standard (S3) ist Teil des neuesten SQL-Datenbankupdates V12 (Preview).</span><span class="sxs-lookup"><span data-stu-id="b9b66-171">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="b9b66-172">Weitere Informationen finden Sie unter Neuerungen in der Azure SQL Database V12 Preview https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .</span><span class="sxs-lookup"><span data-stu-id="b9b66-172">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b66-173">-Sync</span><span class="sxs-lookup"><span data-stu-id="b9b66-173">-Sync</span></span>
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

### <span data-ttu-id="b9b66-174">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b9b66-174">-Confirm</span></span>
<span data-ttu-id="b9b66-175">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9b66-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9b66-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9b66-176">-WhatIf</span></span>
<span data-ttu-id="b9b66-177">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9b66-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9b66-178">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9b66-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9b66-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9b66-179">CommonParameters</span></span>
<span data-ttu-id="b9b66-180">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9b66-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9b66-181">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9b66-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9b66-182">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9b66-182">INPUTS</span></span>

### <span data-ttu-id="b9b66-183">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="b9b66-183">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="b9b66-184">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9b66-184">OUTPUTS</span></span>

### <span data-ttu-id="b9b66-185">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="b9b66-185">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="b9b66-186">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9b66-186">NOTES</span></span>

## <span data-ttu-id="b9b66-187">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9b66-187">RELATED LINKS</span></span>

[<span data-ttu-id="b9b66-188">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="b9b66-188">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="b9b66-189">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="b9b66-189">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="b9b66-190">Datenbank aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b9b66-190">Update Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505718.aspx)

[<span data-ttu-id="b9b66-191">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b9b66-191">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="b9b66-192">Neu – AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b9b66-192">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="b9b66-193">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b9b66-193">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="b9b66-194">Neu – AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="b9b66-194">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


