---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
ms.openlocfilehash: 8ebe1cecc42d8ee01c270b994e1e10de4f402c1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483269"
---
# <span data-ttu-id="79b08-101">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="79b08-101">New-AzureRmSqlDatabaseImport</span></span>

## <span data-ttu-id="79b08-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79b08-102">SYNOPSIS</span></span>
<span data-ttu-id="79b08-103">Importiert eine BacPac-Datei und erstellt eine neue Datenbank auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="79b08-103">Imports a .bacpac file and create a new database on the server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79b08-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79b08-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79b08-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79b08-105">DESCRIPTION</span></span>
<span data-ttu-id="79b08-106">Mit dem Cmdlet **New-AzureRmSqlDatabaseImport** wird eine BacPac-Datei aus einem Azure-Speicherkonto in eine neue Azure SQL-Datenbank importiert.</span><span class="sxs-lookup"><span data-stu-id="79b08-106">The **New-AzureRmSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="79b08-107">Die Anforderung zum Abrufen des Importdaten Bank Status wird möglicherweise gesendet, um Statusinformationen für diese Anforderung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="79b08-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="79b08-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79b08-108">EXAMPLES</span></span>

### <span data-ttu-id="79b08-109">Beispiel 1: Erstellen einer Importanforderung für eine BacPac-Datei</span><span class="sxs-lookup"><span data-stu-id="79b08-109">Example 1: Create an import request for a bacpac file</span></span>
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

<span data-ttu-id="79b08-110">Mit diesem Befehl wird eine Importanforderung zum Importieren einer BacPac-Datei in eine neue Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="79b08-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="79b08-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="79b08-111">PARAMETERS</span></span>

### <span data-ttu-id="79b08-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="79b08-112">-AdministratorLogin</span></span>
<span data-ttu-id="79b08-113">Gibt den Namen des SQL-Administrators an.</span><span class="sxs-lookup"><span data-stu-id="79b08-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="79b08-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="79b08-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="79b08-115">Gibt das Kennwort des SQL-Administrators an.</span><span class="sxs-lookup"><span data-stu-id="79b08-115">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79b08-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="79b08-116">-AuthenticationType</span></span>
<span data-ttu-id="79b08-117">Gibt den Authentifizierungstyp an, der für den Zugriff auf den Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="79b08-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="79b08-118">Dieser Parameter ist standardmäßig SQL, wenn kein Authentifizierungstyp gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="79b08-118">This parameter defaults to SQL if no authentication type is set.</span></span>

<span data-ttu-id="79b08-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="79b08-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79b08-120">SQL.</span><span class="sxs-lookup"><span data-stu-id="79b08-120">SQL.</span></span>
<span data-ttu-id="79b08-121">SQL-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="79b08-121">SQL authentication.</span></span>
<span data-ttu-id="79b08-122">Setzen Sie die Parameter *AdministratorLogin* und *AdministratorLoginPassword* auf den Benutzernamen und das Kennwort des SQL-Administrators.</span><span class="sxs-lookup"><span data-stu-id="79b08-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="79b08-123">Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="79b08-123">ADPassword.</span></span>
<span data-ttu-id="79b08-124">Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="79b08-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="79b08-125">Setzen Sie *AdministratorLogin* und *AdministratorLoginPassword* auf den Azure Active Directory-Administratorbenutzernamen und das Kennwort.</span><span class="sxs-lookup"><span data-stu-id="79b08-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>

<span data-ttu-id="79b08-126">Dieser Parameter steht nur auf SQL Database V12-Servern zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="79b08-126">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.AuthenticationType
Parameter Sets: (All)
Aliases: 
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79b08-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="79b08-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="79b08-128">Gibt die maximale Größe für die neu importierte Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="79b08-128">Specifies the maximum size for the newly imported database.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79b08-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="79b08-129">-DatabaseName</span></span>
<span data-ttu-id="79b08-130">Gibt den Namen der SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="79b08-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="79b08-131">-Edition</span><span class="sxs-lookup"><span data-stu-id="79b08-131">-Edition</span></span>
<span data-ttu-id="79b08-132">Gibt die Edition der neuen Datenbank an, in die importiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="79b08-132">Specifies the edition of the new database to import to.</span></span>

<span data-ttu-id="79b08-133">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="79b08-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79b08-134">Premium</span><span class="sxs-lookup"><span data-stu-id="79b08-134">Premium</span></span>
- <span data-ttu-id="79b08-135">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="79b08-135">Basic</span></span>
- <span data-ttu-id="79b08-136">Standard</span><span class="sxs-lookup"><span data-stu-id="79b08-136">Standard</span></span>
- <span data-ttu-id="79b08-137">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="79b08-137">DataWarehouse</span></span>
- <span data-ttu-id="79b08-138">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="79b08-138">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79b08-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79b08-139">-ResourceGroupName</span></span>
<span data-ttu-id="79b08-140">Gibt den Namen der Ressourcengruppe für den SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="79b08-140">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="79b08-141">-Servername</span><span class="sxs-lookup"><span data-stu-id="79b08-141">-ServerName</span></span>
<span data-ttu-id="79b08-142">Gibt den Namen des SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="79b08-142">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="79b08-143">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="79b08-143">-ServiceObjectiveName</span></span>
<span data-ttu-id="79b08-144">Gibt den Namen des Dienst Ziels an, das der Azure SQL-Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="79b08-144">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="79b08-145">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="79b08-145">-StorageKey</span></span>
<span data-ttu-id="79b08-146">Gibt die Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="79b08-146">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="79b08-147">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="79b08-147">-StorageKeyType</span></span>
<span data-ttu-id="79b08-148">Gibt den Typ der Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="79b08-148">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="79b08-149">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="79b08-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79b08-150">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="79b08-150">StorageAccessKey.</span></span>
<span data-ttu-id="79b08-151">Verwendet den speicherkontoschlüssel.</span><span class="sxs-lookup"><span data-stu-id="79b08-151">Uses the storage account key.</span></span> 
- <span data-ttu-id="79b08-152">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="79b08-152">SharedAccessKey.</span></span>
<span data-ttu-id="79b08-153">Verwendet den SAS-Schlüssel (Shared Access-Signatur).</span><span class="sxs-lookup"><span data-stu-id="79b08-153">Uses the Shared Access Signature (SAS) key.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.StorageKeyType
Parameter Sets: (All)
Aliases: 
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79b08-154">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="79b08-154">-StorageUri</span></span>
<span data-ttu-id="79b08-155">Gibt den BLOB-URI der BacPac-Datei an.</span><span class="sxs-lookup"><span data-stu-id="79b08-155">Specifies the blob URI of the .bacpac file.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79b08-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79b08-156">-Confirm</span></span>
<span data-ttu-id="79b08-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79b08-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79b08-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79b08-158">-WhatIf</span></span>
<span data-ttu-id="79b08-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79b08-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79b08-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79b08-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79b08-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79b08-161">-DefaultProfile</span></span>
<span data-ttu-id="79b08-162">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="79b08-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79b08-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b08-163">CommonParameters</span></span>
<span data-ttu-id="79b08-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79b08-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b08-165">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79b08-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b08-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79b08-166">INPUTS</span></span>

## <span data-ttu-id="79b08-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79b08-167">OUTPUTS</span></span>

### <span data-ttu-id="79b08-168">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="79b08-168">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="79b08-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="79b08-169">NOTES</span></span>
* <span data-ttu-id="79b08-170">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL</span><span class="sxs-lookup"><span data-stu-id="79b08-170">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="79b08-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79b08-171">RELATED LINKS</span></span>

[<span data-ttu-id="79b08-172">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="79b08-172">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="79b08-173">Neu – AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="79b08-173">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="79b08-174">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="79b08-174">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

