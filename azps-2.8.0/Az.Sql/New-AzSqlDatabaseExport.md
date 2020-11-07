---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: 85f74609fe4075ef42e2b417b2d8ac2099df721b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825476"
---
# <span data-ttu-id="4aefe-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="4aefe-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="4aefe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4aefe-102">SYNOPSIS</span></span>
<span data-ttu-id="4aefe-103">Exportiert eine Azure SQL-Datenbank als BacPac-Datei in ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="4aefe-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="4aefe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4aefe-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4aefe-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4aefe-105">DESCRIPTION</span></span>
<span data-ttu-id="4aefe-106">Das Cmdlet **New-AzSqlDatabaseExport** exportiert eine Azure SQL-Datenbank als BacPac-Datei in ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="4aefe-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="4aefe-107">Die Anforderung zum Abrufen des Exportdaten Bank Status wird möglicherweise gesendet, um Statusinformationen für diese Anforderung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4aefe-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="4aefe-108">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4aefe-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4aefe-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4aefe-109">EXAMPLES</span></span>

### <span data-ttu-id="4aefe-110">Beispiel 1: Erstellen einer Exportanforderung für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="4aefe-110">Example 1: Create an export request for a database</span></span>
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

<span data-ttu-id="4aefe-111">Mit diesem Befehl wird eine Exportanforderung für die angegebene Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="4aefe-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="4aefe-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4aefe-112">PARAMETERS</span></span>

### <span data-ttu-id="4aefe-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="4aefe-113">-AdministratorLogin</span></span>
<span data-ttu-id="4aefe-114">Gibt den Namen des SQL-Administrators an.</span><span class="sxs-lookup"><span data-stu-id="4aefe-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="4aefe-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="4aefe-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="4aefe-116">Gibt das Kennwort des SQL-Administrators an.</span><span class="sxs-lookup"><span data-stu-id="4aefe-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="4aefe-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="4aefe-117">-AuthenticationType</span></span>
<span data-ttu-id="4aefe-118">Gibt den Authentifizierungstyp an, der für den Zugriff auf den Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4aefe-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="4aefe-119">Der Standardwert ist SQL, wenn kein Authentifizierungstyp gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="4aefe-119">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="4aefe-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4aefe-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4aefe-121">SQL.</span><span class="sxs-lookup"><span data-stu-id="4aefe-121">Sql.</span></span>
<span data-ttu-id="4aefe-122">SQL-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="4aefe-122">SQL authentication.</span></span>
<span data-ttu-id="4aefe-123">Setzen Sie *AdministratorLogin* und *AdministratorLoginPassword* auf den Benutzernamen und das Kennwort des SQL-Administrators.</span><span class="sxs-lookup"><span data-stu-id="4aefe-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="4aefe-124">Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="4aefe-124">ADPassword.</span></span>
<span data-ttu-id="4aefe-125">Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="4aefe-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="4aefe-126">Setzen Sie *AdministratorLogin* und *AdministratorLoginPassword* auf den Namen und das Kennwort des Azure AD-Administrators.</span><span class="sxs-lookup"><span data-stu-id="4aefe-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="4aefe-127">Dieser Parameter steht nur auf SQL Database V12-Servern zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="4aefe-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="4aefe-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4aefe-128">-DatabaseName</span></span>
<span data-ttu-id="4aefe-129">Gibt den Namen der SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="4aefe-129">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="4aefe-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aefe-130">-DefaultProfile</span></span>
<span data-ttu-id="4aefe-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4aefe-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4aefe-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aefe-132">-ResourceGroupName</span></span>
<span data-ttu-id="4aefe-133">Gibt den Namen der Ressourcengruppe für den SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="4aefe-133">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="4aefe-134">-Servername</span><span class="sxs-lookup"><span data-stu-id="4aefe-134">-ServerName</span></span>
<span data-ttu-id="4aefe-135">Gibt den Namen des SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="4aefe-135">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="4aefe-136">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="4aefe-136">-StorageKey</span></span>
<span data-ttu-id="4aefe-137">Gibt die Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="4aefe-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="4aefe-138">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="4aefe-138">-StorageKeyType</span></span>
<span data-ttu-id="4aefe-139">Gibt den Typ der Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="4aefe-139">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="4aefe-140">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4aefe-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4aefe-141">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="4aefe-141">StorageAccessKey.</span></span>
<span data-ttu-id="4aefe-142">Dieser Wert verwendet einen speicherkontoschlüssel.</span><span class="sxs-lookup"><span data-stu-id="4aefe-142">This value uses a storage account key.</span></span> 
- <span data-ttu-id="4aefe-143">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="4aefe-143">SharedAccessKey.</span></span>
<span data-ttu-id="4aefe-144">Dieser Wert verwendet einen SAS-Schlüssel (Shared Access-Signatur).</span><span class="sxs-lookup"><span data-stu-id="4aefe-144">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="4aefe-145">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="4aefe-145">-StorageUri</span></span>
<span data-ttu-id="4aefe-146">Gibt den BLOB-Link als URL zur BacPac-Datei an.</span><span class="sxs-lookup"><span data-stu-id="4aefe-146">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="4aefe-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4aefe-147">-Confirm</span></span>
<span data-ttu-id="4aefe-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4aefe-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aefe-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aefe-149">-WhatIf</span></span>
<span data-ttu-id="4aefe-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4aefe-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aefe-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4aefe-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aefe-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aefe-152">CommonParameters</span></span>
<span data-ttu-id="4aefe-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aefe-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aefe-154">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4aefe-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aefe-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4aefe-155">INPUTS</span></span>

### <span data-ttu-id="4aefe-156">System. String</span><span class="sxs-lookup"><span data-stu-id="4aefe-156">System.String</span></span>

## <span data-ttu-id="4aefe-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4aefe-157">OUTPUTS</span></span>

### <span data-ttu-id="4aefe-158">Microsoft. Azure. Commands. SQL. DataObjects. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="4aefe-158">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="4aefe-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="4aefe-159">NOTES</span></span>
* <span data-ttu-id="4aefe-160">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL</span><span class="sxs-lookup"><span data-stu-id="4aefe-160">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="4aefe-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4aefe-161">RELATED LINKS</span></span>

[<span data-ttu-id="4aefe-162">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="4aefe-162">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="4aefe-163">Neu – AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="4aefe-163">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="4aefe-164">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="4aefe-164">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
