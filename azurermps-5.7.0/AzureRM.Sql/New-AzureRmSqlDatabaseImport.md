---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
ms.openlocfilehash: 41a55fcb7d2ecb27a079f2fe26d46103235030e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662210"
---
# <span data-ttu-id="2579e-101">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="2579e-101">New-AzureRmSqlDatabaseImport</span></span>

## <span data-ttu-id="2579e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2579e-102">SYNOPSIS</span></span>
<span data-ttu-id="2579e-103">Importiert eine BacPac-Datei und erstellt eine neue Datenbank auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="2579e-103">Imports a .bacpac file and create a new database on the server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2579e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2579e-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2579e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2579e-105">DESCRIPTION</span></span>
<span data-ttu-id="2579e-106">Mit dem Cmdlet **New-AzureRmSqlDatabaseImport** wird eine BacPac-Datei aus einem Azure-Speicherkonto in eine neue Azure SQL-Datenbank importiert.</span><span class="sxs-lookup"><span data-stu-id="2579e-106">The **New-AzureRmSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="2579e-107">Die Anforderung zum Abrufen des Importdaten Bank Status wird möglicherweise gesendet, um Statusinformationen für diese Anforderung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2579e-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="2579e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2579e-108">EXAMPLES</span></span>

### <span data-ttu-id="2579e-109">Beispiel 1: Erstellen einer Importanforderung für eine BacPac-Datei</span><span class="sxs-lookup"><span data-stu-id="2579e-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzureRmSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="2579e-110">Mit diesem Befehl wird eine Importanforderung zum Importieren einer BacPac-Datei in eine neue Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="2579e-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="2579e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2579e-111">PARAMETERS</span></span>

### <span data-ttu-id="2579e-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="2579e-112">-AdministratorLogin</span></span>
<span data-ttu-id="2579e-113">Gibt den Namen des SQL-Administrators an.</span><span class="sxs-lookup"><span data-stu-id="2579e-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="2579e-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="2579e-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="2579e-115">Gibt das Kennwort des SQL-Administrators an.</span><span class="sxs-lookup"><span data-stu-id="2579e-115">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2579e-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="2579e-116">-AuthenticationType</span></span>
<span data-ttu-id="2579e-117">Gibt den Authentifizierungstyp an, der für den Zugriff auf den Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2579e-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="2579e-118">Dieser Parameter ist standardmäßig SQL, wenn kein Authentifizierungstyp gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="2579e-118">This parameter defaults to SQL if no authentication type is set.</span></span>

<span data-ttu-id="2579e-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2579e-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2579e-120">SQL.</span><span class="sxs-lookup"><span data-stu-id="2579e-120">SQL.</span></span>
<span data-ttu-id="2579e-121">SQL-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="2579e-121">SQL authentication.</span></span>
<span data-ttu-id="2579e-122">Setzen Sie die Parameter *AdministratorLogin* und *AdministratorLoginPassword* auf den Benutzernamen und das Kennwort des SQL-Administrators.</span><span class="sxs-lookup"><span data-stu-id="2579e-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="2579e-123">Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="2579e-123">ADPassword.</span></span>
<span data-ttu-id="2579e-124">Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="2579e-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="2579e-125">Setzen Sie *AdministratorLogin* und *AdministratorLoginPassword* auf den Azure Active Directory-Administratorbenutzernamen und das Kennwort.</span><span class="sxs-lookup"><span data-stu-id="2579e-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>

<span data-ttu-id="2579e-126">Dieser Parameter steht nur auf SQL Database V12-Servern zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="2579e-126">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: AuthenticationType
Parameter Sets: (All)
Aliases:
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2579e-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="2579e-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="2579e-128">Gibt die maximale Größe für die neu importierte Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="2579e-128">Specifies the maximum size for the newly imported database.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2579e-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2579e-129">-DatabaseName</span></span>
<span data-ttu-id="2579e-130">Gibt den Namen der SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="2579e-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="2579e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2579e-131">-DefaultProfile</span></span>
<span data-ttu-id="2579e-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2579e-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2579e-133">-Edition</span><span class="sxs-lookup"><span data-stu-id="2579e-133">-Edition</span></span>
<span data-ttu-id="2579e-134">Gibt die Edition der neuen Datenbank an, in die importiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2579e-134">Specifies the edition of the new database to import to.</span></span>

<span data-ttu-id="2579e-135">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2579e-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2579e-136">Premium</span><span class="sxs-lookup"><span data-stu-id="2579e-136">Premium</span></span>
- <span data-ttu-id="2579e-137">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="2579e-137">Basic</span></span>
- <span data-ttu-id="2579e-138">Standard</span><span class="sxs-lookup"><span data-stu-id="2579e-138">Standard</span></span>
- <span data-ttu-id="2579e-139">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="2579e-139">DataWarehouse</span></span>
- <span data-ttu-id="2579e-140">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="2579e-140">Free</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2579e-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2579e-141">-ResourceGroupName</span></span>
<span data-ttu-id="2579e-142">Gibt den Namen der Ressourcengruppe für den SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="2579e-142">Specifies the name of the resource group for the SQL Database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2579e-143">-Servername</span><span class="sxs-lookup"><span data-stu-id="2579e-143">-ServerName</span></span>
<span data-ttu-id="2579e-144">Gibt den Namen des SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="2579e-144">Specifies the name of the SQL Database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2579e-145">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="2579e-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="2579e-146">Gibt den Namen des Dienst Ziels an, das der Azure SQL-Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2579e-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="2579e-147">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="2579e-147">-StorageKey</span></span>
<span data-ttu-id="2579e-148">Gibt die Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="2579e-148">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="2579e-149">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="2579e-149">-StorageKeyType</span></span>
<span data-ttu-id="2579e-150">Gibt den Typ der Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="2579e-150">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="2579e-151">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2579e-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2579e-152">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="2579e-152">StorageAccessKey.</span></span>
<span data-ttu-id="2579e-153">Verwendet den speicherkontoschlüssel.</span><span class="sxs-lookup"><span data-stu-id="2579e-153">Uses the storage account key.</span></span> 
- <span data-ttu-id="2579e-154">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="2579e-154">SharedAccessKey.</span></span>
<span data-ttu-id="2579e-155">Verwendet den SAS-Schlüssel (Shared Access-Signatur).</span><span class="sxs-lookup"><span data-stu-id="2579e-155">Uses the Shared Access Signature (SAS) key.</span></span>

```yaml
Type: StorageKeyType
Parameter Sets: (All)
Aliases:
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2579e-156">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="2579e-156">-StorageUri</span></span>
<span data-ttu-id="2579e-157">Gibt den BLOB-URI der BacPac-Datei an.</span><span class="sxs-lookup"><span data-stu-id="2579e-157">Specifies the blob URI of the .bacpac file.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2579e-158">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2579e-158">-Confirm</span></span>
<span data-ttu-id="2579e-159">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2579e-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2579e-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2579e-160">-WhatIf</span></span>
<span data-ttu-id="2579e-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2579e-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2579e-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2579e-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2579e-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2579e-163">CommonParameters</span></span>
<span data-ttu-id="2579e-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2579e-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2579e-165">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2579e-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2579e-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2579e-166">INPUTS</span></span>

### <span data-ttu-id="2579e-167">Keine</span><span class="sxs-lookup"><span data-stu-id="2579e-167">None</span></span>
<span data-ttu-id="2579e-168">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2579e-168">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2579e-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2579e-169">OUTPUTS</span></span>

### <span data-ttu-id="2579e-170">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="2579e-170">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="2579e-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="2579e-171">NOTES</span></span>
* <span data-ttu-id="2579e-172">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL</span><span class="sxs-lookup"><span data-stu-id="2579e-172">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="2579e-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2579e-173">RELATED LINKS</span></span>

[<span data-ttu-id="2579e-174">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="2579e-174">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="2579e-175">Neu – AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="2579e-175">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="2579e-176">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="2579e-176">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

