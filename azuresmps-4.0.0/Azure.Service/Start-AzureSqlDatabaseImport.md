---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5EE936CA-DD9A-4BC6-B835-E22AE633B46D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc7c8f39f1bdbd35cfffeb59b3b4f184f30845e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005633"
---
# <span data-ttu-id="5d4fc-101">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="5d4fc-101">Start-AzureSqlDatabaseImport</span></span>

## <span data-ttu-id="5d4fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d4fc-102">SYNOPSIS</span></span>
<span data-ttu-id="5d4fc-103">Startet einen Importvorgang aus dem BLOB-Speicher in eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-103">Starts an import operation from blob storage to an Azure SQL Database.</span></span>

## <span data-ttu-id="5d4fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d4fc-104">SYNTAX</span></span>

### <span data-ttu-id="5d4fc-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="5d4fc-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5d4fc-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="5d4fc-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5d4fc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d4fc-107">DESCRIPTION</span></span>
<span data-ttu-id="5d4fc-108">Das Cmdlet **Start-AzureSqlDatabaseImport** startet einen Importvorgang aus Azure BLOB Storage in eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-108">The **Start-AzureSqlDatabaseImport** cmdlet starts an import operation from Azure Blob storage to an Azure SQL Database.</span></span>
<span data-ttu-id="5d4fc-109">Wenn die Datenbank nicht vorhanden ist, wird Sie von diesem Cmdlet mithilfe der von Ihnen angegebenen Größen-und Editions Werte erstellt.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-109">If the database does not exist, this cmdlet creates it by using the size and edition values that you specify.</span></span>
<span data-ttu-id="5d4fc-110">Der Vorgang erfordert einen Datenbankserver-Verbindungskontext.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-110">The operation requires a database server connection context.</span></span>
<span data-ttu-id="5d4fc-111">Verwenden Sie das Get-AzureSqlDatabaseImportExportStatus-Cmdlet, um den Status des Importvorgangs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-111">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the import operation.</span></span>

## <span data-ttu-id="5d4fc-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d4fc-112">EXAMPLES</span></span>

### <span data-ttu-id="5d4fc-113">Beispiel 1: Importieren einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="5d4fc-113">Example 1: Import a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credentials $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $ImportRequest = Start-AzureSqlDatabaseImport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="5d4fc-114">In diesem Beispiel wird ein Importvorgang aus dem BLOB-Speicher in der $BlobName Variablen in die Azure SQL-Datenbank namens DatabaseName initiiert.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-114">This example initiates an import process from the Blob storage in the $BlobName variable into the Azure SQL Database named DatabaseName.</span></span>

## <span data-ttu-id="5d4fc-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d4fc-115">PARAMETERS</span></span>

### <span data-ttu-id="5d4fc-116">-Blobname</span><span class="sxs-lookup"><span data-stu-id="5d4fc-116">-BlobName</span></span>
<span data-ttu-id="5d4fc-117">Gibt den Namen des Azure BLOB-Speichers an, aus dem dieses Cmdlet die Datenbank importiert.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-117">Specifies the name of the Azure Blob storage from which this cmdlet imports the database.</span></span>

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

### <span data-ttu-id="5d4fc-118">-DatabaseMaxSize</span><span class="sxs-lookup"><span data-stu-id="5d4fc-118">-DatabaseMaxSize</span></span>
<span data-ttu-id="5d4fc-119">Gibt die maximale Größe für die Datenbank in Gigabyte an.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-119">Specifies the maximum size, in gigabytes, for the database.</span></span>
<span data-ttu-id="5d4fc-120">Wenn die Datenbank nicht vorhanden ist, wird Sie von diesem Cmdlet basierend auf dieser maximalen Größe erstellt.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-120">If the database does not exist, this cmdlet creates it based on this maximum size.</span></span>
<span data-ttu-id="5d4fc-121">Die akzeptablen Werte unterscheiden sich je nach Edition.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-121">The acceptable values differ based on edition.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5d4fc-122">-DatabaseName</span></span>
<span data-ttu-id="5d4fc-123">Gibt einen Namen für die Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-123">Specifies a name for the database.</span></span>
<span data-ttu-id="5d4fc-124">Wenn die Datenbank nicht vorhanden ist, wird Sie von diesem Cmdlet erstellt, und der Name, den dieser Parameter angibt, wird zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-124">If the database does not exist, this cmdlet creates it, and assigns the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="5d4fc-125">-Edition</span><span class="sxs-lookup"><span data-stu-id="5d4fc-125">-Edition</span></span>
<span data-ttu-id="5d4fc-126">Gibt die Edition der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-126">Specifies the edition of the database.</span></span>
<span data-ttu-id="5d4fc-127">Wenn die Datenbank nicht vorhanden ist, wird Sie von diesem Cmdlet als diese Edition erstellt.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-127">If the database does not exist, this cmdlet creates it as this edition.</span></span>
<span data-ttu-id="5d4fc-128">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="5d4fc-128">Valid values are:</span></span> 

- <span data-ttu-id="5d4fc-129">Keine</span><span class="sxs-lookup"><span data-stu-id="5d4fc-129">None</span></span>
- <span data-ttu-id="5d4fc-130">Web</span><span class="sxs-lookup"><span data-stu-id="5d4fc-130">Web</span></span> 
- <span data-ttu-id="5d4fc-131">Business</span><span class="sxs-lookup"><span data-stu-id="5d4fc-131">Business</span></span> 
- <span data-ttu-id="5d4fc-132">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="5d4fc-132">Basic</span></span>
- <span data-ttu-id="5d4fc-133">Standard</span><span class="sxs-lookup"><span data-stu-id="5d4fc-133">Standard</span></span>
- <span data-ttu-id="5d4fc-134">Premium</span><span class="sxs-lookup"><span data-stu-id="5d4fc-134">Premium</span></span>

<span data-ttu-id="5d4fc-135">Der Standardwert ist Web.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-135">The default is Web.</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="5d4fc-136">-Profile</span></span>
<span data-ttu-id="5d4fc-137">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5d4fc-138">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-139">-SqlConnection</span><span class="sxs-lookup"><span data-stu-id="5d4fc-139">-SqlConnectionContext</span></span>
<span data-ttu-id="5d4fc-140">Gibt den Verbindungskontext eines Servers an, der die Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-140">Specifies the connection context of a server that contains the database.</span></span>

```yaml
Type: ISqlServerConnectionInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-141">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="5d4fc-141">-StorageContainer</span></span>
<span data-ttu-id="5d4fc-142">Gibt den Speichercontainer an, der das BLOB enthält, aus dem dieses Cmdlet eine Datenbank importiert.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-142">Specifies the storage container that contains the Blob from which this cmdlet imports a database.</span></span>

```yaml
Type: AzureStorageContainer
Parameter Sets: ByContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-143">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="5d4fc-143">-StorageContainerName</span></span>
<span data-ttu-id="5d4fc-144">Gibt den Namen des BLOB-Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-144">Specifies the name of the Blob storage container.</span></span>

```yaml
Type: String
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-145">-Storagecontext</span><span class="sxs-lookup"><span data-stu-id="5d4fc-145">-StorageContext</span></span>
<span data-ttu-id="5d4fc-146">Gibt den Kontext des BLOB-Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-146">Specifies the context of the Blob storage container.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d4fc-147">CommonParameters</span></span>
<span data-ttu-id="5d4fc-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d4fc-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d4fc-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d4fc-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d4fc-150">INPUTS</span></span>

## <span data-ttu-id="5d4fc-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d4fc-151">OUTPUTS</span></span>

### <span data-ttu-id="5d4fc-152">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. ImportExportRequest</span><span class="sxs-lookup"><span data-stu-id="5d4fc-152">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="5d4fc-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d4fc-153">NOTES</span></span>

## <span data-ttu-id="5d4fc-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d4fc-154">RELATED LINKS</span></span>

[<span data-ttu-id="5d4fc-155">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="5d4fc-155">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="5d4fc-156">Datenbank importieren</span><span class="sxs-lookup"><span data-stu-id="5d4fc-156">Import Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781284.aspx)

[<span data-ttu-id="5d4fc-157">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="5d4fc-157">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="5d4fc-158">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="5d4fc-158">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="5d4fc-159">Anfang-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="5d4fc-159">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)


