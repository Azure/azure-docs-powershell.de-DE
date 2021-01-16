---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: 737b7170b774be712fb316f5c76b95d326e22fdb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301123"
---
# <span data-ttu-id="419db-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="419db-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="419db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="419db-102">SYNOPSIS</span></span>
<span data-ttu-id="419db-103">Exportiert eine Azure SQL-Datenbank als BACPAC-Datei in ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="419db-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="419db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="419db-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="419db-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="419db-105">DESCRIPTION</span></span>
<span data-ttu-id="419db-106">Das **Cmdlet "New-AzSqlDatabaseExport"** exportiert eine Azure SQL-Datenbank als BACPAC-Datei in ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="419db-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="419db-107">Die Anforderung zum Exportstatus der Datenbank wird möglicherweise gesendet, um Statusinformationen für diese Anforderung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="419db-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="419db-108">Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="419db-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="419db-109">Um dieses Cmdlet verwenden zu können, muss die Firewall auf Azure SQL Server so konfiguriert werden, dass "Azure-Dienste und -Ressourcen den Zugriff auf diesen Server erlauben" konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="419db-109">In order to make use of this cmdlet the firewall on the Azure SQL Server will need to be configured to "Allow Azure services and resources to access this server".</span></span> <span data-ttu-id="419db-110">Wenn dies nicht konfiguriert ist, werden Fehler beim GatewayTimeout angezeigt.</span><span class="sxs-lookup"><span data-stu-id="419db-110">If this is not configured then GatewayTimeout errors will be experienced.</span></span>

## <span data-ttu-id="419db-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="419db-111">EXAMPLES</span></span>

### <span data-ttu-id="419db-112">Beispiel 1: Erstellen einer Exportanforderung für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="419db-112">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.azure.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="419db-113">Mit diesem Befehl wird eine Exportanforderung für die angegebene Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="419db-113">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="419db-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="419db-114">PARAMETERS</span></span>

### <span data-ttu-id="419db-115">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="419db-115">-AdministratorLogin</span></span>
<span data-ttu-id="419db-116">Gibt den Namen des SQL an.</span><span class="sxs-lookup"><span data-stu-id="419db-116">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="419db-117">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="419db-117">-AdministratorLoginPassword</span></span>
<span data-ttu-id="419db-118">Gibt das Kennwort des SQL an.</span><span class="sxs-lookup"><span data-stu-id="419db-118">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="419db-119">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="419db-119">-AuthenticationType</span></span>
<span data-ttu-id="419db-120">Gibt den Authentifizierungstyp an, der für den Zugriff auf den Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="419db-120">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="419db-121">Der Standardwert ist SQL, wenn kein Authentifizierungstyp festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="419db-121">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="419db-122">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="419db-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="419db-123">Sql.</span><span class="sxs-lookup"><span data-stu-id="419db-123">Sql.</span></span>
<span data-ttu-id="419db-124">SQL Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="419db-124">SQL authentication.</span></span>
<span data-ttu-id="419db-125">Legen Sie *"AdministratorLogin"* und *"AdministratorLoginPassword"* auf den SQL und das Kennwort des Administrators fest.</span><span class="sxs-lookup"><span data-stu-id="419db-125">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="419db-126">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="419db-126">ADPassword.</span></span>
<span data-ttu-id="419db-127">Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="419db-127">Azure Active Directory authentication.</span></span>
<span data-ttu-id="419db-128">Legen *Sie "AdministratorLogin"* und *"AdministratorLoginPassword"* auf den Azure AD-Administratorbenutzernamen und das Kennwort fest.</span><span class="sxs-lookup"><span data-stu-id="419db-128">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="419db-129">Dieser Parameter ist nur auf SQL Database V12-Servern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="419db-129">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="419db-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="419db-130">-DatabaseName</span></span>
<span data-ttu-id="419db-131">Gibt den Namen der datenbank SQL an.</span><span class="sxs-lookup"><span data-stu-id="419db-131">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="419db-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="419db-132">-DefaultProfile</span></span>
<span data-ttu-id="419db-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="419db-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="419db-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="419db-134">-ResourceGroupName</span></span>
<span data-ttu-id="419db-135">Gibt den Namen der Ressourcengruppe für den Datenbankserver SQL an.</span><span class="sxs-lookup"><span data-stu-id="419db-135">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="419db-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="419db-136">-ServerName</span></span>
<span data-ttu-id="419db-137">Gibt den Namen des SQL Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="419db-137">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="419db-138">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="419db-138">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="419db-139">Die SQL Server-Ressourcen-ID zum Erstellen eines privaten Links</span><span class="sxs-lookup"><span data-stu-id="419db-139">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="419db-140">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="419db-140">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="419db-141">Die Ressourcen-ID des Speicherkontos zum Erstellen eines privaten Links</span><span class="sxs-lookup"><span data-stu-id="419db-141">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="419db-142">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="419db-142">-StorageKey</span></span>
<span data-ttu-id="419db-143">Gibt den Zugriffsschlüssel für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="419db-143">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="419db-144">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="419db-144">-StorageKeyType</span></span>
<span data-ttu-id="419db-145">Gibt den Typ des Zugriffsschlüssels für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="419db-145">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="419db-146">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="419db-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="419db-147">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="419db-147">StorageAccessKey.</span></span>
<span data-ttu-id="419db-148">Für diesen Wert wird ein Speicherkontoschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="419db-148">This value uses a storage account key.</span></span> 
- <span data-ttu-id="419db-149">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="419db-149">SharedAccessKey.</span></span>
<span data-ttu-id="419db-150">Für diesen Wert wird ein SAS (Shared Access Signature)-Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="419db-150">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="419db-151">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="419db-151">-StorageUri</span></span>
<span data-ttu-id="419db-152">Gibt den BLOB-Link als URL zur Datei "BACPAC" an.</span><span class="sxs-lookup"><span data-stu-id="419db-152">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="419db-153">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="419db-153">-UseNetworkIsolation</span></span>
<span data-ttu-id="419db-154">Wenn dies festgelegt ist, wird ein privater Link für das Speicherkonto und/oder den SQL erstellt</span><span class="sxs-lookup"><span data-stu-id="419db-154">If set, will create private link for storage account and/or SQL server</span></span>

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

### <span data-ttu-id="419db-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="419db-155">-Confirm</span></span>
<span data-ttu-id="419db-156">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="419db-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="419db-157">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="419db-157">-WhatIf</span></span>
<span data-ttu-id="419db-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="419db-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="419db-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="419db-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="419db-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="419db-160">CommonParameters</span></span>
<span data-ttu-id="419db-161">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="419db-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="419db-162">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="419db-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="419db-163">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="419db-163">INPUTS</span></span>

### <span data-ttu-id="419db-164">System.String</span><span class="sxs-lookup"><span data-stu-id="419db-164">System.String</span></span>

## <span data-ttu-id="419db-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="419db-165">OUTPUTS</span></span>

### <span data-ttu-id="419db-166">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="419db-166">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="419db-167">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="419db-167">NOTES</span></span>
* <span data-ttu-id="419db-168">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="419db-168">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="419db-169">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="419db-169">RELATED LINKS</span></span>

[<span data-ttu-id="419db-170">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="419db-170">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="419db-171">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="419db-171">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="419db-172">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="419db-172">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
