---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
ms.openlocfilehash: 074261adf9c2f5501ca12753971fac08783ab36f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008865"
---
# <span data-ttu-id="7da23-101">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="7da23-101">New-AzSqlDatabaseImport</span></span>

## <span data-ttu-id="7da23-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7da23-102">SYNOPSIS</span></span>
<span data-ttu-id="7da23-103">Importiert eine BacPac-Datei und erstellt eine neue Datenbank auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="7da23-103">Imports a .bacpac file and create a new database on the server.</span></span>

## <span data-ttu-id="7da23-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7da23-104">SYNTAX</span></span>

```
New-AzSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7da23-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7da23-105">DESCRIPTION</span></span>
<span data-ttu-id="7da23-106">Mit dem Cmdlet **New-AzSqlDatabaseImport** wird eine BacPac-Datei aus einem Azure-Speicherkonto in eine neue Azure SQL-Datenbank importiert.</span><span class="sxs-lookup"><span data-stu-id="7da23-106">The **New-AzSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="7da23-107">Die Anforderung zum Abrufen des Importdaten Bank Status wird möglicherweise gesendet, um Statusinformationen für diese Anforderung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7da23-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="7da23-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7da23-108">EXAMPLES</span></span>

### <span data-ttu-id="7da23-109">Beispiel 1: Erstellen einer Importanforderung für eine BacPac-Datei</span><span class="sxs-lookup"><span data-stu-id="7da23-109">Example 1: Create an import request for a bacpac file</span></span>
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

<span data-ttu-id="7da23-110">Mit diesem Befehl wird eine Importanforderung zum Importieren einer BacPac-Datei in eine neue Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="7da23-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="7da23-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7da23-111">PARAMETERS</span></span>

### <span data-ttu-id="7da23-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="7da23-112">-AdministratorLogin</span></span>
<span data-ttu-id="7da23-113">Gibt den Namen des SQL-Administrators an.</span><span class="sxs-lookup"><span data-stu-id="7da23-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="7da23-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="7da23-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="7da23-115">Gibt das Kennwort des SQL-Administrators an.</span><span class="sxs-lookup"><span data-stu-id="7da23-115">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="7da23-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="7da23-116">-AuthenticationType</span></span>
<span data-ttu-id="7da23-117">Gibt den Authentifizierungstyp an, der für den Zugriff auf den Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7da23-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="7da23-118">Dieser Parameter ist standardmäßig SQL, wenn kein Authentifizierungstyp gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="7da23-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="7da23-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7da23-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7da23-120">SQL.</span><span class="sxs-lookup"><span data-stu-id="7da23-120">SQL.</span></span>
<span data-ttu-id="7da23-121">SQL-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="7da23-121">SQL authentication.</span></span>
<span data-ttu-id="7da23-122">Setzen Sie die Parameter *AdministratorLogin* und *AdministratorLoginPassword* auf den Benutzernamen und das Kennwort des SQL-Administrators.</span><span class="sxs-lookup"><span data-stu-id="7da23-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="7da23-123">Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="7da23-123">ADPassword.</span></span>
<span data-ttu-id="7da23-124">Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="7da23-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="7da23-125">Setzen Sie *AdministratorLogin* und *AdministratorLoginPassword* auf den Azure Active Directory-Administratorbenutzernamen und das Kennwort.</span><span class="sxs-lookup"><span data-stu-id="7da23-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="7da23-126">Dieser Parameter steht nur auf SQL Database V12-Servern zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="7da23-126">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="7da23-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="7da23-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="7da23-128">Gibt die maximale Größe für die neu importierte Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="7da23-128">Specifies the maximum size for the newly imported database.</span></span>

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

### <span data-ttu-id="7da23-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7da23-129">-DatabaseName</span></span>
<span data-ttu-id="7da23-130">Gibt den Namen der SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="7da23-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="7da23-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da23-131">-DefaultProfile</span></span>
<span data-ttu-id="7da23-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7da23-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7da23-133">-Edition</span><span class="sxs-lookup"><span data-stu-id="7da23-133">-Edition</span></span>
<span data-ttu-id="7da23-134">Gibt die Edition der neuen Datenbank an, in die importiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7da23-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="7da23-135">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7da23-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7da23-136">Premium</span><span class="sxs-lookup"><span data-stu-id="7da23-136">Premium</span></span>
- <span data-ttu-id="7da23-137">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="7da23-137">Basic</span></span>
- <span data-ttu-id="7da23-138">Standard</span><span class="sxs-lookup"><span data-stu-id="7da23-138">Standard</span></span>
- <span data-ttu-id="7da23-139">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="7da23-139">DataWarehouse</span></span>
- <span data-ttu-id="7da23-140">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="7da23-140">Free</span></span>

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

### <span data-ttu-id="7da23-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7da23-141">-ResourceGroupName</span></span>
<span data-ttu-id="7da23-142">Gibt den Namen der Ressourcengruppe für den SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="7da23-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="7da23-143">-Servername</span><span class="sxs-lookup"><span data-stu-id="7da23-143">-ServerName</span></span>
<span data-ttu-id="7da23-144">Gibt den Namen des SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="7da23-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="7da23-145">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="7da23-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="7da23-146">Gibt den Namen des Dienst Ziels an, das der Azure SQL-Datenbank zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7da23-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="7da23-147">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="7da23-147">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="7da23-148">Die SQL Server-Ressourcen-ID zum Erstellen eines privaten Links</span><span class="sxs-lookup"><span data-stu-id="7da23-148">The sql server resource id to create private link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7da23-149">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="7da23-149">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="7da23-150">Die Ressourcen-ID des speicherkontos zum Erstellen eines privaten Links</span><span class="sxs-lookup"><span data-stu-id="7da23-150">The storage account resource id to create private link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7da23-151">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="7da23-151">-StorageKey</span></span>
<span data-ttu-id="7da23-152">Gibt die Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="7da23-152">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="7da23-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="7da23-153">-StorageKeyType</span></span>
<span data-ttu-id="7da23-154">Gibt den Typ der Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="7da23-154">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="7da23-155">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7da23-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7da23-156">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="7da23-156">StorageAccessKey.</span></span>
<span data-ttu-id="7da23-157">Verwendet den speicherkontoschlüssel.</span><span class="sxs-lookup"><span data-stu-id="7da23-157">Uses the storage account key.</span></span> 
- <span data-ttu-id="7da23-158">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="7da23-158">SharedAccessKey.</span></span>
<span data-ttu-id="7da23-159">Verwendet den SAS-Schlüssel (Shared Access-Signatur).</span><span class="sxs-lookup"><span data-stu-id="7da23-159">Uses the Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="7da23-160">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="7da23-160">-StorageUri</span></span>
<span data-ttu-id="7da23-161">Gibt den BLOB-URI der BacPac-Datei an.</span><span class="sxs-lookup"><span data-stu-id="7da23-161">Specifies the blob URI of the .bacpac file.</span></span>

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

### <span data-ttu-id="7da23-162">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="7da23-162">-UseNetworkIsolation</span></span>
<span data-ttu-id="7da23-163">Wenn gesetzt, wird privater Link für das Speicherkonto und/oder SQL Server erstellt</span><span class="sxs-lookup"><span data-stu-id="7da23-163">If set, will create private link for storage account and/or SQL server</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7da23-164">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7da23-164">-Confirm</span></span>
<span data-ttu-id="7da23-165">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7da23-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7da23-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7da23-166">-WhatIf</span></span>
<span data-ttu-id="7da23-167">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7da23-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7da23-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7da23-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7da23-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da23-169">CommonParameters</span></span>
<span data-ttu-id="7da23-170">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7da23-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da23-171">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7da23-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da23-172">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7da23-172">INPUTS</span></span>

### <span data-ttu-id="7da23-173">System. String</span><span class="sxs-lookup"><span data-stu-id="7da23-173">System.String</span></span>

## <span data-ttu-id="7da23-174">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7da23-174">OUTPUTS</span></span>

### <span data-ttu-id="7da23-175">Microsoft. Azure. Commands. SQL. DataObjects. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="7da23-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="7da23-176">Notizen</span><span class="sxs-lookup"><span data-stu-id="7da23-176">NOTES</span></span>
* <span data-ttu-id="7da23-177">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL</span><span class="sxs-lookup"><span data-stu-id="7da23-177">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="7da23-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7da23-178">RELATED LINKS</span></span>

[<span data-ttu-id="7da23-179">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="7da23-179">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="7da23-180">Neu – AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="7da23-180">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="7da23-181">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="7da23-181">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

