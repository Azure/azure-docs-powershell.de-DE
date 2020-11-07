---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
ms.openlocfilehash: f7ede8432f8e833b3d309925daab591889836257
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664960"
---
# <span data-ttu-id="f95df-101">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="f95df-101">New-AzureRmSqlDatabaseExport</span></span>

## <span data-ttu-id="f95df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f95df-102">SYNOPSIS</span></span>
<span data-ttu-id="f95df-103">Exportiert eine Azure SQL-Datenbank als BacPac-Datei in ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="f95df-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f95df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f95df-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f95df-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f95df-105">DESCRIPTION</span></span>
<span data-ttu-id="f95df-106">Das Cmdlet **New-AzureRmSqlDatabaseExport** exportiert eine Azure SQL-Datenbank als BacPac-Datei in ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="f95df-106">The **New-AzureRmSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="f95df-107">Die Anforderung zum Abrufen des Exportdaten Bank Status wird möglicherweise gesendet, um Statusinformationen für diese Anforderung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f95df-107">The get export database status request may be sent to retrieve status information for this request.</span></span>

<span data-ttu-id="f95df-108">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f95df-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f95df-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f95df-109">EXAMPLES</span></span>

### <span data-ttu-id="f95df-110">Beispiel 1: Erstellen einer Exportanforderung für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="f95df-110">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
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

<span data-ttu-id="f95df-111">Mit diesem Befehl wird eine Exportanforderung für die angegebene Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="f95df-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="f95df-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f95df-112">PARAMETERS</span></span>

### <span data-ttu-id="f95df-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="f95df-113">-AdministratorLogin</span></span>
<span data-ttu-id="f95df-114">Gibt den Namen des SQL-Administrators an.</span><span class="sxs-lookup"><span data-stu-id="f95df-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="f95df-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="f95df-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="f95df-116">Gibt das Kennwort des SQL-Administrators an.</span><span class="sxs-lookup"><span data-stu-id="f95df-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="f95df-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="f95df-117">-AuthenticationType</span></span>
<span data-ttu-id="f95df-118">Gibt den Authentifizierungstyp an, der für den Zugriff auf den Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f95df-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="f95df-119">Der Standardwert ist SQL, wenn kein Authentifizierungstyp gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="f95df-119">The default value is SQL if no authentication type is set.</span></span>

<span data-ttu-id="f95df-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f95df-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f95df-121">SQL.</span><span class="sxs-lookup"><span data-stu-id="f95df-121">Sql.</span></span>
<span data-ttu-id="f95df-122">SQL-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="f95df-122">SQL authentication.</span></span>
<span data-ttu-id="f95df-123">Setzen Sie *AdministratorLogin* und *AdministratorLoginPassword* auf den Benutzernamen und das Kennwort des SQL-Administrators.</span><span class="sxs-lookup"><span data-stu-id="f95df-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="f95df-124">Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="f95df-124">ADPassword.</span></span>
<span data-ttu-id="f95df-125">Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="f95df-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="f95df-126">Setzen Sie *AdministratorLogin* und *AdministratorLoginPassword* auf den Namen und das Kennwort des Azure AD-Administrators.</span><span class="sxs-lookup"><span data-stu-id="f95df-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>

<span data-ttu-id="f95df-127">Dieser Parameter steht nur auf SQL Database V12-Servern zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f95df-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="f95df-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f95df-128">-DatabaseName</span></span>
<span data-ttu-id="f95df-129">Gibt den Namen der SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="f95df-129">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="f95df-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f95df-130">-ResourceGroupName</span></span>
<span data-ttu-id="f95df-131">Gibt den Namen der Ressourcengruppe für den SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="f95df-131">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="f95df-132">-Servername</span><span class="sxs-lookup"><span data-stu-id="f95df-132">-ServerName</span></span>
<span data-ttu-id="f95df-133">Gibt den Namen des SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="f95df-133">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="f95df-134">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="f95df-134">-StorageKey</span></span>
<span data-ttu-id="f95df-135">Gibt die Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="f95df-135">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="f95df-136">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="f95df-136">-StorageKeyType</span></span>
<span data-ttu-id="f95df-137">Gibt den Typ der Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="f95df-137">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="f95df-138">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f95df-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f95df-139">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="f95df-139">StorageAccessKey.</span></span>
<span data-ttu-id="f95df-140">Dieser Wert verwendet einen speicherkontoschlüssel.</span><span class="sxs-lookup"><span data-stu-id="f95df-140">This value uses a storage account key.</span></span> 
- <span data-ttu-id="f95df-141">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="f95df-141">SharedAccessKey.</span></span>
<span data-ttu-id="f95df-142">Dieser Wert verwendet einen SAS-Schlüssel (Shared Access-Signatur).</span><span class="sxs-lookup"><span data-stu-id="f95df-142">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="f95df-143">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="f95df-143">-StorageUri</span></span>
<span data-ttu-id="f95df-144">Gibt den BLOB-Link als URL zur BacPac-Datei an.</span><span class="sxs-lookup"><span data-stu-id="f95df-144">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="f95df-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f95df-145">-Confirm</span></span>
<span data-ttu-id="f95df-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f95df-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f95df-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f95df-147">-WhatIf</span></span>
<span data-ttu-id="f95df-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f95df-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f95df-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f95df-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f95df-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95df-150">-DefaultProfile</span></span>
<span data-ttu-id="f95df-151">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f95df-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f95df-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95df-152">CommonParameters</span></span>
<span data-ttu-id="f95df-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f95df-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95df-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f95df-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95df-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f95df-155">INPUTS</span></span>

## <span data-ttu-id="f95df-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f95df-156">OUTPUTS</span></span>

### <span data-ttu-id="f95df-157">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="f95df-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="f95df-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="f95df-158">NOTES</span></span>
* <span data-ttu-id="f95df-159">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL</span><span class="sxs-lookup"><span data-stu-id="f95df-159">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="f95df-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f95df-160">RELATED LINKS</span></span>

[<span data-ttu-id="f95df-161">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="f95df-161">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="f95df-162">Neu – AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="f95df-162">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="f95df-163">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="f95df-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
