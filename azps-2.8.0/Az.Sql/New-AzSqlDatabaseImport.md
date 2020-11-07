---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
ms.openlocfilehash: a571621f7129b5d402521462f3d8273f55d9303d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825471"
---
# <span data-ttu-id="7634a-101">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="7634a-101">New-AzSqlDatabaseImport</span></span>

## <span data-ttu-id="7634a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7634a-102">SYNOPSIS</span></span>
<span data-ttu-id="7634a-103">Importiert eine BacPac-Datei und erstellt eine neue Datenbank auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="7634a-103">Imports a .bacpac file and create a new database on the server.</span></span>

## <span data-ttu-id="7634a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7634a-104">SYNTAX</span></span>

```
New-AzSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7634a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7634a-105">DESCRIPTION</span></span>
<span data-ttu-id="7634a-106">Mit dem Cmdlet **New-AzSqlDatabaseImport** wird eine BacPac-Datei aus einem Azure-Speicherkonto in eine neue Azure SQL-Datenbank importiert.</span><span class="sxs-lookup"><span data-stu-id="7634a-106">The **New-AzSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="7634a-107">Die Anforderung zum Abrufen des Importdaten Bank Status wird möglicherweise gesendet, um Statusinformationen für diese Anforderung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7634a-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="7634a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7634a-108">EXAMPLES</span></span>

### <span data-ttu-id="7634a-109">Beispiel 1: Erstellen einer Importanforderung für eine BacPac-Datei</span><span class="sxs-lookup"><span data-stu-id="7634a-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
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

<span data-ttu-id="7634a-110">Mit diesem Befehl wird eine Importanforderung zum Importieren einer BacPac-Datei in eine neue Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="7634a-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="7634a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7634a-111">PARAMETERS</span></span>

### <span data-ttu-id="7634a-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="7634a-112">-AdministratorLogin</span></span>
<span data-ttu-id="7634a-113">Gibt den Namen des SQL-Administrators an.</span><span class="sxs-lookup"><span data-stu-id="7634a-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="7634a-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="7634a-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="7634a-115">Gibt das Kennwort des SQL-Administrators an.</span><span class="sxs-lookup"><span data-stu-id="7634a-115">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="7634a-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="7634a-116">-AuthenticationType</span></span>
<span data-ttu-id="7634a-117">Gibt den Authentifizierungstyp an, der für den Zugriff auf den Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7634a-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="7634a-118">Dieser Parameter ist standardmäßig SQL, wenn kein Authentifizierungstyp gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="7634a-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="7634a-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7634a-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7634a-120">SQL.</span><span class="sxs-lookup"><span data-stu-id="7634a-120">SQL.</span></span>
<span data-ttu-id="7634a-121">SQL-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="7634a-121">SQL authentication.</span></span>
<span data-ttu-id="7634a-122">Setzen Sie die Parameter *AdministratorLogin* und *AdministratorLoginPassword* auf den Benutzernamen und das Kennwort des SQL-Administrators.</span><span class="sxs-lookup"><span data-stu-id="7634a-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="7634a-123">Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="7634a-123">ADPassword.</span></span>
<span data-ttu-id="7634a-124">Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="7634a-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="7634a-125">Setzen Sie *AdministratorLogin* und *AdministratorLoginPassword* auf den Azure Active Directory-Administratorbenutzernamen und das Kennwort.</span><span class="sxs-lookup"><span data-stu-id="7634a-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="7634a-126">Dieser Parameter steht nur auf SQL Database V12-Servern zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="7634a-126">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="7634a-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="7634a-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="7634a-128">Gibt die maximale Größe für die neu importierte Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="7634a-128">Specifies the maximum size for the newly imported database.</span></span>

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

### <span data-ttu-id="7634a-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7634a-129">-DatabaseName</span></span>
<span data-ttu-id="7634a-130">Gibt den Namen der SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="7634a-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="7634a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7634a-131">-DefaultProfile</span></span>
<span data-ttu-id="7634a-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7634a-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7634a-133">-Edition</span><span class="sxs-lookup"><span data-stu-id="7634a-133">-Edition</span></span>
<span data-ttu-id="7634a-134">Gibt die Edition der neuen Datenbank an, in die importiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7634a-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="7634a-135">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7634a-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7634a-136">Premium</span><span class="sxs-lookup"><span data-stu-id="7634a-136">Premium</span></span>
- <span data-ttu-id="7634a-137">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="7634a-137">Basic</span></span>
- <span data-ttu-id="7634a-138">Standard</span><span class="sxs-lookup"><span data-stu-id="7634a-138">Standard</span></span>
- <span data-ttu-id="7634a-139">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="7634a-139">DataWarehouse</span></span>
- <span data-ttu-id="7634a-140">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="7634a-140">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS, GeneralPurpose, BusinessCritical

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7634a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7634a-141">-ResourceGroupName</span></span>
<span data-ttu-id="7634a-142">Gibt den Namen der Ressourcengruppe für den SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="7634a-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="7634a-143">-Servername</span><span class="sxs-lookup"><span data-stu-id="7634a-143">-ServerName</span></span>
<span data-ttu-id="7634a-144">Gibt den Namen des SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="7634a-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="7634a-145">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="7634a-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="7634a-146">Gibt den Namen des Dienst Ziels an, das der Azure SQL-Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7634a-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="7634a-147">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="7634a-147">-StorageKey</span></span>
<span data-ttu-id="7634a-148">Gibt die Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="7634a-148">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="7634a-149">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="7634a-149">-StorageKeyType</span></span>
<span data-ttu-id="7634a-150">Gibt den Typ der Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="7634a-150">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="7634a-151">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7634a-151">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7634a-152">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="7634a-152">StorageAccessKey.</span></span>
<span data-ttu-id="7634a-153">Verwendet den speicherkontoschlüssel.</span><span class="sxs-lookup"><span data-stu-id="7634a-153">Uses the storage account key.</span></span> 
- <span data-ttu-id="7634a-154">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="7634a-154">SharedAccessKey.</span></span>
<span data-ttu-id="7634a-155">Verwendet den SAS-Schlüssel (Shared Access-Signatur).</span><span class="sxs-lookup"><span data-stu-id="7634a-155">Uses the Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="7634a-156">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="7634a-156">-StorageUri</span></span>
<span data-ttu-id="7634a-157">Gibt den BLOB-URI der BacPac-Datei an.</span><span class="sxs-lookup"><span data-stu-id="7634a-157">Specifies the blob URI of the .bacpac file.</span></span>

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

### <span data-ttu-id="7634a-158">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7634a-158">-Confirm</span></span>
<span data-ttu-id="7634a-159">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7634a-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7634a-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7634a-160">-WhatIf</span></span>
<span data-ttu-id="7634a-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7634a-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7634a-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7634a-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7634a-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7634a-163">CommonParameters</span></span>
<span data-ttu-id="7634a-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7634a-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7634a-165">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7634a-165">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7634a-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7634a-166">INPUTS</span></span>

### <span data-ttu-id="7634a-167">System. String</span><span class="sxs-lookup"><span data-stu-id="7634a-167">System.String</span></span>

## <span data-ttu-id="7634a-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7634a-168">OUTPUTS</span></span>

### <span data-ttu-id="7634a-169">Microsoft. Azure. Commands. SQL. DataObjects. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="7634a-169">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="7634a-170">Notizen</span><span class="sxs-lookup"><span data-stu-id="7634a-170">NOTES</span></span>
* <span data-ttu-id="7634a-171">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL</span><span class="sxs-lookup"><span data-stu-id="7634a-171">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="7634a-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7634a-172">RELATED LINKS</span></span>

[<span data-ttu-id="7634a-173">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="7634a-173">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="7634a-174">Neu – AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="7634a-174">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="7634a-175">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="7634a-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

