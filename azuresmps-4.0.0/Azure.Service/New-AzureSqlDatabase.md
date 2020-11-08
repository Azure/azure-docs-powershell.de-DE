---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006179"
---
# <span data-ttu-id="cd825-101">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cd825-101">New-AzureSqlDatabase</span></span>

## <span data-ttu-id="cd825-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd825-102">SYNOPSIS</span></span>
<span data-ttu-id="cd825-103">Erstellt eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="cd825-103">Creates an Azure SQL Database.</span></span>

## <span data-ttu-id="cd825-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd825-104">SYNTAX</span></span>

### <span data-ttu-id="cd825-105">ByConnectionContext</span><span class="sxs-lookup"><span data-stu-id="cd825-105">ByConnectionContext</span></span>
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd825-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="cd825-106">ByServerName</span></span>
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd825-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd825-107">DESCRIPTION</span></span>
<span data-ttu-id="cd825-108">Das Cmdlet **New-AzureSqlDatabase** erstellt eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="cd825-108">The **New-AzureSqlDatabase** cmdlet creates an Azure SQL Database.</span></span>
<span data-ttu-id="cd825-109">Sie können den Server angeben, indem Sie einen Azure SQL-Datenbankserver-Verbindungskontext verwenden, den Sie mit dem Cmdlet **New-AzureSqlDatabaseServerContext** erstellen.</span><span class="sxs-lookup"><span data-stu-id="cd825-109">You can specify the server by using an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="cd825-110">Wenn Sie den Servernamen angeben, verwendet das Cmdlet die aktuellen Azure-Abonnementinformationen, um die Anforderung für den Zugriff auf den Server zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="cd825-110">Or, if you specify the server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="cd825-111">Wenn Sie eine neue Datenbank erstellen, indem Sie einen Azure SQL-Datenbankserver angeben, erstellt das Cmdlet **New-AzureSqlDatabase** einen temporären Verbindungskontext mit dem angegebenen Servernamen und den aktuellen Azure-Abonnementinformationen, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="cd825-111">When you create a new database by specifying an Azure SQL Database server, the **New-AzureSqlDatabase** cmdlet creates a temporary connection context using the specified server name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="cd825-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd825-112">EXAMPLES</span></span>

### <span data-ttu-id="cd825-113">Beispiel 1: Erstellen einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="cd825-113">Example 1: Create a database</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="cd825-114">Dieser Befehl erstellt eine Azure SQL-Datenbank mit dem Namen "Database1" für den Azure SQL-Datenbankserver-Verbindungskontext $Context.</span><span class="sxs-lookup"><span data-stu-id="cd825-114">This command creates an Azure SQL Database named Database1, for the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="cd825-115">Beispiel 2: Erstellen einer Datenbank im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="cd825-115">Example 2: Create a database in the current subscription</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="cd825-116">In diesem Beispiel wird eine Datenbank mit dem Namen Database1 im angegebenen Azure SQL-Datenbankserver mit dem Namen lpqd0zbr8y erstellt.</span><span class="sxs-lookup"><span data-stu-id="cd825-116">This example creates a database named Database1, in the specified Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="cd825-117">Das Cmdlet verwendet die aktuellen Azure-Abonnementinformationen, um die Anforderung für den Zugriff auf den Server zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="cd825-117">The cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

## <span data-ttu-id="cd825-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd825-118">PARAMETERS</span></span>

### <span data-ttu-id="cd825-119">-Sortierung</span><span class="sxs-lookup"><span data-stu-id="cd825-119">-Collation</span></span>
<span data-ttu-id="cd825-120">Gibt eine Sortierung für die neue Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="cd825-120">Specifies a collation for the new database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd825-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="cd825-121">-ConnectionContext</span></span>
<span data-ttu-id="cd825-122">Gibt den Verbindungskontext eines Servers an, auf dem dieses Cmdlet eine Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="cd825-122">Specifies the connection context of a server where this cmdlet creates a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd825-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cd825-123">-DatabaseName</span></span>
<span data-ttu-id="cd825-124">Gibt den Namen der neuen Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="cd825-124">Specifies the name of the new database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd825-125">-Edition</span><span class="sxs-lookup"><span data-stu-id="cd825-125">-Edition</span></span>
<span data-ttu-id="cd825-126">Gibt die Edition für die neue Azure SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="cd825-126">Specifies the edition for the new Azure SQL Database.</span></span>
<span data-ttu-id="cd825-127">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="cd825-127">Valid values are:</span></span> 

- <span data-ttu-id="cd825-128">Keine</span><span class="sxs-lookup"><span data-stu-id="cd825-128">None</span></span>
- <span data-ttu-id="cd825-129">Web</span><span class="sxs-lookup"><span data-stu-id="cd825-129">Web</span></span>
- <span data-ttu-id="cd825-130">Business</span><span class="sxs-lookup"><span data-stu-id="cd825-130">Business</span></span>
- <span data-ttu-id="cd825-131">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="cd825-131">Basic</span></span>
- <span data-ttu-id="cd825-132">Standard</span><span class="sxs-lookup"><span data-stu-id="cd825-132">Standard</span></span>
-  <span data-ttu-id="cd825-133">Premium</span><span class="sxs-lookup"><span data-stu-id="cd825-133">Premium</span></span>

<span data-ttu-id="cd825-134">Der Standardwert ist Web.</span><span class="sxs-lookup"><span data-stu-id="cd825-134">The default value is Web.</span></span>

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

### <span data-ttu-id="cd825-135">-Force</span><span class="sxs-lookup"><span data-stu-id="cd825-135">-Force</span></span>
<span data-ttu-id="cd825-136">Ermöglicht die Ausführung der Aktion, ohne dass der Benutzer zur Bestätigung aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="cd825-136">Allows the action to complete without prompting the user for confirmation.</span></span>

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

### <span data-ttu-id="cd825-137">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="cd825-137">-MaxSizeBytes</span></span>
<span data-ttu-id="cd825-138">Gibt die maximale Größe der Datenbank in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="cd825-138">Specifies the maximum size of the database in bytes.</span></span>
<span data-ttu-id="cd825-139">Sie können entweder diesen Parameter oder den *MaxSizeGB* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="cd825-139">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="cd825-140">Lesen Sie die Beschreibung des *MaxSizeGB* -Parameters für akzeptable Werte auf der Grundlage der Edition.</span><span class="sxs-lookup"><span data-stu-id="cd825-140">See the *MaxSizeGB* parameter description for acceptable values based on edition.</span></span>

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

### <span data-ttu-id="cd825-141">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="cd825-141">-MaxSizeGB</span></span>
<span data-ttu-id="cd825-142">Gibt die maximale Größe der Datenbank in Gigabyte an.</span><span class="sxs-lookup"><span data-stu-id="cd825-142">Specifies the maximum size of the database in gigabytes.</span></span>
<span data-ttu-id="cd825-143">Sie können entweder diesen Parameter oder den *MaxSizeBytes* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="cd825-143">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="cd825-144">Die akzeptablen Werte unterscheiden sich je nach Edition.</span><span class="sxs-lookup"><span data-stu-id="cd825-144">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="cd825-145">Grundlegende Editions Werte: 1 oder 2</span><span class="sxs-lookup"><span data-stu-id="cd825-145">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="cd825-146">Standard Editions Werte: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 oder 250</span><span class="sxs-lookup"><span data-stu-id="cd825-146">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="cd825-147">Premium Edition-Werte: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 oder 500</span><span class="sxs-lookup"><span data-stu-id="cd825-147">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="cd825-148">Web Edition-Werte: 1 oder 5</span><span class="sxs-lookup"><span data-stu-id="cd825-148">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="cd825-149">Business Edition-Werte: 10, 20, 30, 40, 50, 100 oder 150</span><span class="sxs-lookup"><span data-stu-id="cd825-149">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

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

### <span data-ttu-id="cd825-150">-Profil</span><span class="sxs-lookup"><span data-stu-id="cd825-150">-Profile</span></span>
<span data-ttu-id="cd825-151">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="cd825-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cd825-152">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="cd825-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cd825-153">-Servername</span><span class="sxs-lookup"><span data-stu-id="cd825-153">-ServerName</span></span>
<span data-ttu-id="cd825-154">Gibt den Namen des Azure SQL-Datenbankservers an, der die neue Datenbank enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="cd825-154">Specifies the name of the Azure SQL Database server to contain the new database.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd825-155">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="cd825-155">-ServiceObjective</span></span>
<span data-ttu-id="cd825-156">Gibt ein Objekt an, das das neue Dienst Ziel (Leistungsstufe) für diese Datenbank darstellt.</span><span class="sxs-lookup"><span data-stu-id="cd825-156">Specifies an object that represent the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="cd825-157">Dieser Wert stellt die Ebene der Ressourcen dar, die dieser Datenbank zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="cd825-157">This value represents the level of resources assigned to this database.</span></span>
<span data-ttu-id="cd825-158">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="cd825-158">Valid values are:</span></span> 

<span data-ttu-id="cd825-159">Standard: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c-Standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b-Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928-Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 \* Standard (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="cd825-159">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 \*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="cd825-160">\* Standard (S3) ist Teil des neuesten SQL-Datenbankupdates V12 (Preview).</span><span class="sxs-lookup"><span data-stu-id="cd825-160">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="cd825-161">Weitere Informationen finden Sie unter Neuerungen in der Azure SQL Database V12 Preview https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .</span><span class="sxs-lookup"><span data-stu-id="cd825-161">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

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

### <span data-ttu-id="cd825-162">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cd825-162">-Confirm</span></span>
<span data-ttu-id="cd825-163">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd825-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd825-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd825-164">-WhatIf</span></span>
<span data-ttu-id="cd825-165">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd825-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd825-166">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd825-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd825-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd825-167">CommonParameters</span></span>
<span data-ttu-id="cd825-168">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd825-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd825-169">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd825-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd825-170">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd825-170">INPUTS</span></span>

## <span data-ttu-id="cd825-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd825-171">OUTPUTS</span></span>

### <span data-ttu-id="cd825-172">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="cd825-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="cd825-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd825-173">NOTES</span></span>
* <span data-ttu-id="cd825-174">Verwenden Sie das Remove-AzureSqlDatabase-Cmdlet, um eine von **New-AzureSqlDatabase** erstellte Datenbank zu löschen.</span><span class="sxs-lookup"><span data-stu-id="cd825-174">To delete a database that was created by **New-AzureSqlDatabase** , use the Remove-AzureSqlDatabase cmdlet.</span></span>

## <span data-ttu-id="cd825-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd825-175">RELATED LINKS</span></span>

[<span data-ttu-id="cd825-176">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="cd825-176">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="cd825-177">Datenbank erstellen</span><span class="sxs-lookup"><span data-stu-id="cd825-177">Create Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[<span data-ttu-id="cd825-178">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="cd825-178">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="cd825-179">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cd825-179">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="cd825-180">Neu – AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="cd825-180">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="cd825-181">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cd825-181">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="cd825-182">Satz-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cd825-182">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


