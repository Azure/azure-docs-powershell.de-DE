---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
ms.openlocfilehash: 324686ace908235e3b48fb150249d2bad22c169b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476469"
---
# <span data-ttu-id="44eec-101">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="44eec-101">New-AzureRmSqlDatabaseExport</span></span>

## <span data-ttu-id="44eec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="44eec-102">SYNOPSIS</span></span>
<span data-ttu-id="44eec-103">Exportiert eine Azure SQL-Datenbank als BacPac-Datei in ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="44eec-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44eec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="44eec-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44eec-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44eec-105">DESCRIPTION</span></span>
<span data-ttu-id="44eec-106">Das Cmdlet **New-AzureRmSqlDatabaseExport** exportiert eine Azure SQL-Datenbank als BacPac-Datei in ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="44eec-106">The **New-AzureRmSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="44eec-107">Die Anforderung zum Abrufen des Exportdaten Bank Status wird möglicherweise gesendet, um Statusinformationen für diese Anforderung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="44eec-107">The get export database status request may be sent to retrieve status information for this request.</span></span>

<span data-ttu-id="44eec-108">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="44eec-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="44eec-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44eec-109">EXAMPLES</span></span>

### <span data-ttu-id="44eec-110">Beispiel 1: Erstellen einer Exportanforderung für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="44eec-110">Example 1: Create an export request for a database</span></span>
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

<span data-ttu-id="44eec-111">Mit diesem Befehl wird eine Exportanforderung für die angegebene Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="44eec-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="44eec-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="44eec-112">PARAMETERS</span></span>

### <span data-ttu-id="44eec-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="44eec-113">-AdministratorLogin</span></span>
<span data-ttu-id="44eec-114">Gibt den Namen des SQL-Administrators an.</span><span class="sxs-lookup"><span data-stu-id="44eec-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="44eec-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="44eec-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="44eec-116">Gibt das Kennwort des SQL-Administrators an.</span><span class="sxs-lookup"><span data-stu-id="44eec-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="44eec-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="44eec-117">-AuthenticationType</span></span>
<span data-ttu-id="44eec-118">Gibt den Authentifizierungstyp an, der für den Zugriff auf den Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="44eec-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="44eec-119">Der Standardwert ist SQL, wenn kein Authentifizierungstyp gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="44eec-119">The default value is SQL if no authentication type is set.</span></span>

<span data-ttu-id="44eec-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="44eec-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="44eec-121">SQL.</span><span class="sxs-lookup"><span data-stu-id="44eec-121">Sql.</span></span>
<span data-ttu-id="44eec-122">SQL-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="44eec-122">SQL authentication.</span></span>
<span data-ttu-id="44eec-123">Setzen Sie *AdministratorLogin* und *AdministratorLoginPassword* auf den Benutzernamen und das Kennwort des SQL-Administrators.</span><span class="sxs-lookup"><span data-stu-id="44eec-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="44eec-124">Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="44eec-124">ADPassword.</span></span>
<span data-ttu-id="44eec-125">Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="44eec-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="44eec-126">Setzen Sie *AdministratorLogin* und *AdministratorLoginPassword* auf den Namen und das Kennwort des Azure AD-Administrators.</span><span class="sxs-lookup"><span data-stu-id="44eec-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>

<span data-ttu-id="44eec-127">Dieser Parameter steht nur auf SQL Database V12-Servern zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="44eec-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="44eec-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="44eec-128">-DatabaseName</span></span>
<span data-ttu-id="44eec-129">Gibt den Namen der SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="44eec-129">Specifies the name of the SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44eec-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44eec-130">-DefaultProfile</span></span>
<span data-ttu-id="44eec-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="44eec-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44eec-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44eec-132">-ResourceGroupName</span></span>
<span data-ttu-id="44eec-133">Gibt den Namen der Ressourcengruppe für den SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="44eec-133">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="44eec-134">-Servername</span><span class="sxs-lookup"><span data-stu-id="44eec-134">-ServerName</span></span>
<span data-ttu-id="44eec-135">Gibt den Namen des SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="44eec-135">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="44eec-136">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="44eec-136">-StorageKey</span></span>
<span data-ttu-id="44eec-137">Gibt die Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="44eec-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="44eec-138">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="44eec-138">-StorageKeyType</span></span>
<span data-ttu-id="44eec-139">Gibt den Typ der Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="44eec-139">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="44eec-140">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="44eec-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="44eec-141">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="44eec-141">StorageAccessKey.</span></span>
<span data-ttu-id="44eec-142">Dieser Wert verwendet einen speicherkontoschlüssel.</span><span class="sxs-lookup"><span data-stu-id="44eec-142">This value uses a storage account key.</span></span> 
- <span data-ttu-id="44eec-143">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="44eec-143">SharedAccessKey.</span></span>
<span data-ttu-id="44eec-144">Dieser Wert verwendet einen SAS-Schlüssel (Shared Access-Signatur).</span><span class="sxs-lookup"><span data-stu-id="44eec-144">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="44eec-145">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="44eec-145">-StorageUri</span></span>
<span data-ttu-id="44eec-146">Gibt den BLOB-Link als URL zur BacPac-Datei an.</span><span class="sxs-lookup"><span data-stu-id="44eec-146">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="44eec-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="44eec-147">-Confirm</span></span>
<span data-ttu-id="44eec-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="44eec-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44eec-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44eec-149">-WhatIf</span></span>
<span data-ttu-id="44eec-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44eec-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44eec-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44eec-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44eec-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44eec-152">CommonParameters</span></span>
<span data-ttu-id="44eec-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44eec-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44eec-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44eec-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44eec-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="44eec-155">INPUTS</span></span>

### <span data-ttu-id="44eec-156">Keine</span><span class="sxs-lookup"><span data-stu-id="44eec-156">None</span></span>
<span data-ttu-id="44eec-157">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="44eec-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="44eec-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="44eec-158">OUTPUTS</span></span>

### <span data-ttu-id="44eec-159">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="44eec-159">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="44eec-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="44eec-160">NOTES</span></span>
* <span data-ttu-id="44eec-161">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL</span><span class="sxs-lookup"><span data-stu-id="44eec-161">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="44eec-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="44eec-162">RELATED LINKS</span></span>

[<span data-ttu-id="44eec-163">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="44eec-163">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="44eec-164">Neu – AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="44eec-164">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="44eec-165">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="44eec-165">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
