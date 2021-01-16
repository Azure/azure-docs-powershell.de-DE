---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
ms.openlocfilehash: ab1fcfa9b050f795a464488df51768b95996eb8c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460736"
---
# <span data-ttu-id="d9f0f-101">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="d9f0f-101">New-AzSqlDatabaseImport</span></span>

## <span data-ttu-id="d9f0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="d9f0f-103">Importiert eine BACPAC-Datei, und erstellt eine neue Datenbank auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-103">Imports a .bacpac file and create a new database on the server.</span></span>

## <span data-ttu-id="d9f0f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9f0f-104">SYNTAX</span></span>

```
New-AzSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9f0f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9f0f-105">DESCRIPTION</span></span>
<span data-ttu-id="d9f0f-106">Das **Cmdlet "New-AzSqlDatabaseImport"** importiert eine Bacpac-Datei aus einem Azure -Speicherkonto in eine neue Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-106">The **New-AzSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="d9f0f-107">Die Anforderung zum Importstatus der Datenbank wird möglicherweise gesendet, um Statusinformationen für diese Anforderung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="d9f0f-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d9f0f-108">EXAMPLES</span></span>

### <span data-ttu-id="d9f0f-109">Beispiel 1: Erstellen einer Importanforderung für eine Bacpac-Datei</span><span class="sxs-lookup"><span data-stu-id="d9f0f-109">Example 1: Create an import request for a bacpac file</span></span>
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

<span data-ttu-id="d9f0f-110">Mit diesem Befehl wird eine Importanforderung zum Importieren einer Bacpac in eine neue Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="d9f0f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9f0f-111">PARAMETERS</span></span>

### <span data-ttu-id="d9f0f-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="d9f0f-112">-AdministratorLogin</span></span>
<span data-ttu-id="d9f0f-113">Gibt den Namen des SQL an.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="d9f0f-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="d9f0f-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="d9f0f-115">Gibt das Kennwort des SQL an.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-115">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="d9f0f-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="d9f0f-116">-AuthenticationType</span></span>
<span data-ttu-id="d9f0f-117">Gibt den Authentifizierungstyp an, der für den Zugriff auf den Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="d9f0f-118">Dieser Parameter wird standardmäßig auf SQL, wenn kein Authentifizierungstyp festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="d9f0f-119">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="d9f0f-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d9f0f-120">SQL.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-120">SQL.</span></span>
<span data-ttu-id="d9f0f-121">SQL Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-121">SQL authentication.</span></span>
<span data-ttu-id="d9f0f-122">Legen Sie *die Parameter "AdministratorLogin"* und *"AdministratorLoginPassword"* auf den SQL und das Kennwort des Administrators fest.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="d9f0f-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-123">ADPassword.</span></span>
<span data-ttu-id="d9f0f-124">Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="d9f0f-125">Legen *Sie "AdministratorLogin"* und *"AdministratorLoginPassword"* auf den Benutzernamen und das Kennwort des Azure Active Directory-Administrators fest.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="d9f0f-126">Dieser Parameter ist nur auf SQL Datenbank-V12-Servern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-126">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="d9f0f-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="d9f0f-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="d9f0f-128">Gibt die maximale Größe für die neu importierte Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-128">Specifies the maximum size for the newly imported database.</span></span>

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

### <span data-ttu-id="d9f0f-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d9f0f-129">-DatabaseName</span></span>
<span data-ttu-id="d9f0f-130">Gibt den Namen der datenbank SQL an.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="d9f0f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9f0f-131">-DefaultProfile</span></span>
<span data-ttu-id="d9f0f-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d9f0f-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9f0f-133">-Edition</span><span class="sxs-lookup"><span data-stu-id="d9f0f-133">-Edition</span></span>
<span data-ttu-id="d9f0f-134">Gibt die Edition der neuen Datenbank an, in die importiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="d9f0f-135">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="d9f0f-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d9f0f-136">Premium</span><span class="sxs-lookup"><span data-stu-id="d9f0f-136">Premium</span></span>
- <span data-ttu-id="d9f0f-137">Standard</span><span class="sxs-lookup"><span data-stu-id="d9f0f-137">Basic</span></span>
- <span data-ttu-id="d9f0f-138">Standard</span><span class="sxs-lookup"><span data-stu-id="d9f0f-138">Standard</span></span>
- <span data-ttu-id="d9f0f-139">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="d9f0f-139">DataWarehouse</span></span>
- <span data-ttu-id="d9f0f-140">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="d9f0f-140">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS, GeneralPurpose, BusinessCritical, Hyperscale

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9f0f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9f0f-141">-ResourceGroupName</span></span>
<span data-ttu-id="d9f0f-142">Gibt den Namen der Ressourcengruppe für den Datenbankserver SQL an.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="d9f0f-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d9f0f-143">-ServerName</span></span>
<span data-ttu-id="d9f0f-144">Gibt den Namen des SQL Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="d9f0f-145">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="d9f0f-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="d9f0f-146">Gibt den Namen des Dienstziels an, das der Azure SQL werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d9f0f-147">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="d9f0f-147">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="d9f0f-148">Die SQL Server-Ressourcen-ID zum Erstellen eines privaten Links</span><span class="sxs-lookup"><span data-stu-id="d9f0f-148">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="d9f0f-149">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="d9f0f-149">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="d9f0f-150">Die Ressourcen-ID des Speicherkontos zum Erstellen eines privaten Links</span><span class="sxs-lookup"><span data-stu-id="d9f0f-150">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="d9f0f-151">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="d9f0f-151">-StorageKey</span></span>
<span data-ttu-id="d9f0f-152">Gibt den Zugriffsschlüssel für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-152">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="d9f0f-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="d9f0f-153">-StorageKeyType</span></span>
<span data-ttu-id="d9f0f-154">Gibt den Typ des Zugriffsschlüssels für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-154">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="d9f0f-155">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="d9f0f-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d9f0f-156">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-156">StorageAccessKey.</span></span>
<span data-ttu-id="d9f0f-157">Verwendet den Speicherkontoschlüssel.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-157">Uses the storage account key.</span></span> 
- <span data-ttu-id="d9f0f-158">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-158">SharedAccessKey.</span></span>
<span data-ttu-id="d9f0f-159">Verwendet den Schlüssel "Shared Access Signature (SAS)".</span><span class="sxs-lookup"><span data-stu-id="d9f0f-159">Uses the Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="d9f0f-160">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="d9f0f-160">-StorageUri</span></span>
<span data-ttu-id="d9f0f-161">Gibt den BLOB-URI der Datei "BACPAC" an.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-161">Specifies the blob URI of the .bacpac file.</span></span>

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

### <span data-ttu-id="d9f0f-162">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="d9f0f-162">-UseNetworkIsolation</span></span>
<span data-ttu-id="d9f0f-163">Wenn dies festgelegt ist, wird ein privater Link für das Speicherkonto und/oder den SQL erstellt</span><span class="sxs-lookup"><span data-stu-id="d9f0f-163">If set, will create private link for storage account and/or SQL server</span></span>

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

### <span data-ttu-id="d9f0f-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9f0f-164">-Confirm</span></span>
<span data-ttu-id="d9f0f-165">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9f0f-166">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d9f0f-166">-WhatIf</span></span>
<span data-ttu-id="d9f0f-167">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9f0f-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9f0f-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9f0f-169">CommonParameters</span></span>
<span data-ttu-id="d9f0f-170">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9f0f-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9f0f-171">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9f0f-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9f0f-172">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d9f0f-172">INPUTS</span></span>

### <span data-ttu-id="d9f0f-173">System.String</span><span class="sxs-lookup"><span data-stu-id="d9f0f-173">System.String</span></span>

## <span data-ttu-id="d9f0f-174">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d9f0f-174">OUTPUTS</span></span>

### <span data-ttu-id="d9f0f-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="d9f0f-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="d9f0f-176">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d9f0f-176">NOTES</span></span>
* <span data-ttu-id="d9f0f-177">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="d9f0f-177">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="d9f0f-178">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d9f0f-178">RELATED LINKS</span></span>

[<span data-ttu-id="d9f0f-179">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="d9f0f-179">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="d9f0f-180">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="d9f0f-180">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="d9f0f-181">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="d9f0f-181">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

