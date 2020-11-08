---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 3005E411-9466-4602-8E07-F4EF8804AB2A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22bff485bf49e0ec5f482e1325af661862583605
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005958"
---
# <span data-ttu-id="82d00-101">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="82d00-101">Start-AzureSqlDatabaseExport</span></span>

## <span data-ttu-id="82d00-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="82d00-102">SYNOPSIS</span></span>
<span data-ttu-id="82d00-103">Startet einen Exportvorgang aus einer Azure SQL-Datenbank in den BLOB-Speicher.</span><span class="sxs-lookup"><span data-stu-id="82d00-103">Starts an export operation from an Azure SQL Database to Blob storage.</span></span>

## <span data-ttu-id="82d00-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="82d00-104">SYNTAX</span></span>

### <span data-ttu-id="82d00-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="82d00-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="82d00-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="82d00-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="82d00-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="82d00-107">DESCRIPTION</span></span>
<span data-ttu-id="82d00-108">Das Cmdlet **Start-AzureSqlDatabaseExport** startet einen Exportvorgang aus einer Azure SQL-Datenbank in den BLOB-Speicher.</span><span class="sxs-lookup"><span data-stu-id="82d00-108">The **Start-AzureSqlDatabaseExport** cmdlet starts an export operation from an Azure SQL Database to Blob storage.</span></span>
<span data-ttu-id="82d00-109">Der Vorgang erfordert einen Datenbankserver-Verbindungskontext.</span><span class="sxs-lookup"><span data-stu-id="82d00-109">The operation requires a database server connection context.</span></span>
<span data-ttu-id="82d00-110">Verwenden Sie das Get-AzureSqlDatabaseImportExportStatus-Cmdlet, um den Status des Exportvorgangs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="82d00-110">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the export operation.</span></span>

## <span data-ttu-id="82d00-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="82d00-111">EXAMPLES</span></span>

### <span data-ttu-id="82d00-112">Beispiel 1: Exportieren einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="82d00-112">Example 1: Export a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credential $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $exportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="82d00-113">In diesem Beispiel wird ein Exportvorgang aus der Azure SQL-Datenbank initiiert, in dem der in der $DatabaseName-Variable gespeicherte Name des in der $BlobName Variablen gespeicherten BLOB-Speichers gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="82d00-113">This example initiates an export process from the Azure SQL Database that has the name stored in the $DatabaseName variable to the Blob storage stored in the $BlobName variable.</span></span>

## <span data-ttu-id="82d00-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="82d00-114">PARAMETERS</span></span>

### <span data-ttu-id="82d00-115">-Blobname</span><span class="sxs-lookup"><span data-stu-id="82d00-115">-BlobName</span></span>
<span data-ttu-id="82d00-116">Gibt den Namen des Azure BLOB-Speichers an, in dem dieses Cmdlet die Datenbank exportiert.</span><span class="sxs-lookup"><span data-stu-id="82d00-116">Specifies the name of the Azure Blob storage into which this cmdlet exports the database.</span></span>

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

### <span data-ttu-id="82d00-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="82d00-117">-DatabaseName</span></span>
<span data-ttu-id="82d00-118">Gibt den Namen der Datenbank an, aus der mit diesem Cmdlet Daten exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="82d00-118">Specifies the name of the database from which this cmdlet exports data.</span></span>

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

### <span data-ttu-id="82d00-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="82d00-119">-Profile</span></span>
<span data-ttu-id="82d00-120">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="82d00-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="82d00-121">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="82d00-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="82d00-122">-SqlConnection</span><span class="sxs-lookup"><span data-stu-id="82d00-122">-SqlConnectionContext</span></span>
<span data-ttu-id="82d00-123">Gibt den Verbindungskontext eines Servers an, der die Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="82d00-123">Specifies the connection context of a server that contains the database.</span></span>

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

### <span data-ttu-id="82d00-124">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="82d00-124">-StorageContainer</span></span>
<span data-ttu-id="82d00-125">Gibt den Speichercontainer an, der das BLOB enthält, in das dieses Cmdlet eine Datenbank exportiert.</span><span class="sxs-lookup"><span data-stu-id="82d00-125">Specifies the storage container that contains the Blob into which this cmdlet export a database.</span></span>

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

### <span data-ttu-id="82d00-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="82d00-126">-StorageContainerName</span></span>
<span data-ttu-id="82d00-127">Gibt den Namen des Speichercontainers an, der das BLOB enthält, in das dieses Cmdlet eine Datenbank exportiert.</span><span class="sxs-lookup"><span data-stu-id="82d00-127">Specifies the name of the storage container that contains the Blob into which this cmdlet exports a database.</span></span>

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

### <span data-ttu-id="82d00-128">-Storagecontext</span><span class="sxs-lookup"><span data-stu-id="82d00-128">-StorageContext</span></span>
<span data-ttu-id="82d00-129">Gibt den Kontext des BLOB-Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="82d00-129">Specifies the context of the Blob storage container.</span></span>

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

### <span data-ttu-id="82d00-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82d00-130">CommonParameters</span></span>
<span data-ttu-id="82d00-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82d00-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82d00-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82d00-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82d00-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="82d00-133">INPUTS</span></span>

## <span data-ttu-id="82d00-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="82d00-134">OUTPUTS</span></span>

### <span data-ttu-id="82d00-135">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. ImportExportRequest</span><span class="sxs-lookup"><span data-stu-id="82d00-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="82d00-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="82d00-136">NOTES</span></span>

## <span data-ttu-id="82d00-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="82d00-137">RELATED LINKS</span></span>

[<span data-ttu-id="82d00-138">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="82d00-138">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="82d00-139">Datenbank exportieren</span><span class="sxs-lookup"><span data-stu-id="82d00-139">Export Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781282.aspx)

[<span data-ttu-id="82d00-140">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="82d00-140">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="82d00-141">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="82d00-141">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="82d00-142">Anfang-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="82d00-142">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


