---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: c5b0295458d0efe443dc20ab069ccfb62a44eb49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165519"
---
# <span data-ttu-id="b3795-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="b3795-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="b3795-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b3795-102">SYNOPSIS</span></span>
<span data-ttu-id="b3795-103">Exportiert eine Azure SQL-Datenbank als BacPac-Datei in ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="b3795-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="b3795-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3795-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3795-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3795-105">DESCRIPTION</span></span>
<span data-ttu-id="b3795-106">Das Cmdlet **New-AzSqlDatabaseExport** exportiert eine Azure SQL-Datenbank als BacPac-Datei in ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="b3795-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="b3795-107">Die Anforderung zum Abrufen des Exportdaten Bank Status wird möglicherweise gesendet, um Statusinformationen für diese Anforderung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b3795-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="b3795-108">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b3795-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b3795-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3795-109">EXAMPLES</span></span>

### <span data-ttu-id="b3795-110">Beispiel 1: Erstellen einer Exportanforderung für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="b3795-110">Example 1: Create an export request for a database</span></span>
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

<span data-ttu-id="b3795-111">Mit diesem Befehl wird eine Exportanforderung für die angegebene Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3795-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="b3795-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3795-112">PARAMETERS</span></span>

### <span data-ttu-id="b3795-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="b3795-113">-AdministratorLogin</span></span>
<span data-ttu-id="b3795-114">Gibt den Namen des SQL-Administrators an.</span><span class="sxs-lookup"><span data-stu-id="b3795-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="b3795-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="b3795-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="b3795-116">Gibt das Kennwort des SQL-Administrators an.</span><span class="sxs-lookup"><span data-stu-id="b3795-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="b3795-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="b3795-117">-AuthenticationType</span></span>
<span data-ttu-id="b3795-118">Gibt den Authentifizierungstyp an, der für den Zugriff auf den Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b3795-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="b3795-119">Der Standardwert ist SQL, wenn kein Authentifizierungstyp gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="b3795-119">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="b3795-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b3795-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b3795-121">SQL.</span><span class="sxs-lookup"><span data-stu-id="b3795-121">Sql.</span></span>
<span data-ttu-id="b3795-122">SQL-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="b3795-122">SQL authentication.</span></span>
<span data-ttu-id="b3795-123">Setzen Sie *AdministratorLogin* und *AdministratorLoginPassword* auf den Benutzernamen und das Kennwort des SQL-Administrators.</span><span class="sxs-lookup"><span data-stu-id="b3795-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="b3795-124">Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="b3795-124">ADPassword.</span></span>
<span data-ttu-id="b3795-125">Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="b3795-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="b3795-126">Setzen Sie *AdministratorLogin* und *AdministratorLoginPassword* auf den Namen und das Kennwort des Azure AD-Administrators.</span><span class="sxs-lookup"><span data-stu-id="b3795-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="b3795-127">Dieser Parameter steht nur auf SQL Database V12-Servern zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="b3795-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="b3795-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b3795-128">-DatabaseName</span></span>
<span data-ttu-id="b3795-129">Gibt den Namen der SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="b3795-129">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="b3795-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3795-130">-DefaultProfile</span></span>
<span data-ttu-id="b3795-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b3795-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3795-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3795-132">-ResourceGroupName</span></span>
<span data-ttu-id="b3795-133">Gibt den Namen der Ressourcengruppe für den SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="b3795-133">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="b3795-134">-Servername</span><span class="sxs-lookup"><span data-stu-id="b3795-134">-ServerName</span></span>
<span data-ttu-id="b3795-135">Gibt den Namen des SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="b3795-135">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="b3795-136">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="b3795-136">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="b3795-137">Die SQL Server-Ressourcen-ID zum Erstellen eines privaten Links</span><span class="sxs-lookup"><span data-stu-id="b3795-137">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="b3795-138">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="b3795-138">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="b3795-139">Die Ressourcen-ID des speicherkontos zum Erstellen eines privaten Links</span><span class="sxs-lookup"><span data-stu-id="b3795-139">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="b3795-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="b3795-140">-StorageKey</span></span>
<span data-ttu-id="b3795-141">Gibt die Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="b3795-141">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="b3795-142">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="b3795-142">-StorageKeyType</span></span>
<span data-ttu-id="b3795-143">Gibt den Typ der Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="b3795-143">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="b3795-144">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b3795-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b3795-145">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="b3795-145">StorageAccessKey.</span></span>
<span data-ttu-id="b3795-146">Dieser Wert verwendet einen speicherkontoschlüssel.</span><span class="sxs-lookup"><span data-stu-id="b3795-146">This value uses a storage account key.</span></span> 
- <span data-ttu-id="b3795-147">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="b3795-147">SharedAccessKey.</span></span>
<span data-ttu-id="b3795-148">Dieser Wert verwendet einen SAS-Schlüssel (Shared Access-Signatur).</span><span class="sxs-lookup"><span data-stu-id="b3795-148">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="b3795-149">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="b3795-149">-StorageUri</span></span>
<span data-ttu-id="b3795-150">Gibt den BLOB-Link als URL zur BacPac-Datei an.</span><span class="sxs-lookup"><span data-stu-id="b3795-150">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="b3795-151">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="b3795-151">-UseNetworkIsolation</span></span>
<span data-ttu-id="b3795-152">Wenn gesetzt, wird privater Link für das Speicherkonto und/oder SQL Server erstellt</span><span class="sxs-lookup"><span data-stu-id="b3795-152">If set, will create private link for storage account and/or SQL server</span></span>

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

### <span data-ttu-id="b3795-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b3795-153">-Confirm</span></span>
<span data-ttu-id="b3795-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b3795-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3795-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3795-155">-WhatIf</span></span>
<span data-ttu-id="b3795-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3795-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3795-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3795-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3795-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3795-158">CommonParameters</span></span>
<span data-ttu-id="b3795-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3795-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3795-160">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3795-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3795-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b3795-161">INPUTS</span></span>

### <span data-ttu-id="b3795-162">System. String</span><span class="sxs-lookup"><span data-stu-id="b3795-162">System.String</span></span>

## <span data-ttu-id="b3795-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b3795-163">OUTPUTS</span></span>

### <span data-ttu-id="b3795-164">Microsoft. Azure. Commands. SQL. DataObjects. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="b3795-164">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="b3795-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="b3795-165">NOTES</span></span>
* <span data-ttu-id="b3795-166">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL</span><span class="sxs-lookup"><span data-stu-id="b3795-166">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="b3795-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b3795-167">RELATED LINKS</span></span>

[<span data-ttu-id="b3795-168">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="b3795-168">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="b3795-169">Neu – AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="b3795-169">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="b3795-170">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="b3795-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
