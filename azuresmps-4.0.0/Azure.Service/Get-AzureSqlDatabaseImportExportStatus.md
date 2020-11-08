---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006500"
---
# <span data-ttu-id="819f3-101">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="819f3-101">Get-AzureSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="819f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="819f3-102">SYNOPSIS</span></span>
<span data-ttu-id="819f3-103">Ruft den Status einer Import-oder Exportanforderung ab.</span><span class="sxs-lookup"><span data-stu-id="819f3-103">Gets the status of an import or export request.</span></span>

## <span data-ttu-id="819f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="819f3-104">SYNTAX</span></span>

### <span data-ttu-id="819f3-105">ByConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="819f3-105">ByConnectionInfo</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="819f3-106">ByRequestObject</span><span class="sxs-lookup"><span data-stu-id="819f3-106">ByRequestObject</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="819f3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="819f3-107">DESCRIPTION</span></span>
<span data-ttu-id="819f3-108">Das Cmdlet " **Get-AzureSqlDatabaseImportExportStatus** " Ruft den Status einer Import-oder Exportanforderung ab.</span><span class="sxs-lookup"><span data-stu-id="819f3-108">The **Get-AzureSqlDatabaseImportExportStatus** cmdlet gets the status of an import or export request.</span></span>
<span data-ttu-id="819f3-109">Das Start-AzureSqlDatabaseImport-oder Start-AzureSqlDatabaseExport-Cmdlet initiiert Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="819f3-109">The Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet initiates requests.</span></span>
<span data-ttu-id="819f3-110">Sie können das Request-Objekt mithilfe des *Request* -Parameters angeben, oder Sie können die Anforderung mithilfe des Parameters *Anforderungs* -Nr und der Parameter *username* , *Password* und *Servername* identifizieren.</span><span class="sxs-lookup"><span data-stu-id="819f3-110">You can specify the request object by using the *Request* parameter, or you can identify the request by using the *RequestId* parameter and the *Username* , *Password* , and *ServerName* parameters.</span></span>

## <span data-ttu-id="819f3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="819f3-111">EXAMPLES</span></span>

### <span data-ttu-id="819f3-112">Beispiel 1: Abrufen des Status einer Exportanforderung</span><span class="sxs-lookup"><span data-stu-id="819f3-112">Example 1: Get the status of an export request</span></span>
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

<span data-ttu-id="819f3-113">Der erste Befehl erstellt eine Exportanforderung und speichert Sie dann in der $ExportRequest-Variablen.</span><span class="sxs-lookup"><span data-stu-id="819f3-113">The first command creates an export request, and then stores it in the $ExportRequest variable.</span></span>

<span data-ttu-id="819f3-114">Der zweite Befehl ruft den Status der Exportanforderung ab, die in $ExportRequest gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="819f3-114">The second command gets the status of the export request stored in $ExportRequest.</span></span>

## <span data-ttu-id="819f3-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="819f3-115">PARAMETERS</span></span>

### <span data-ttu-id="819f3-116">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="819f3-116">-Password</span></span>
<span data-ttu-id="819f3-117">Gibt das Kennwort an, das zum Herstellen einer Verbindung mit dem Azure SQL-Datenbankserver erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="819f3-117">Specifies the password that is required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="819f3-118">Sie müssen diesen Parameter angeben, wenn Sie den Parameter *Requestor* angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="819f3-118">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819f3-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="819f3-119">-Profile</span></span>
<span data-ttu-id="819f3-120">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="819f3-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="819f3-121">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="819f3-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="819f3-122">-Anfrage</span><span class="sxs-lookup"><span data-stu-id="819f3-122">-Request</span></span>
<span data-ttu-id="819f3-123">Gibt ein **ImportExportRequest** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="819f3-123">Specifies an **ImportExportRequest** object.</span></span>
<span data-ttu-id="819f3-124">Verwenden Sie das Cmdlet Start-AzureSqlDatabaseImport oder Start-AzureSqlDatabaseExport, um ein Import-oder Export Anforderungsobjekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="819f3-124">To obtain an import or export request object, use the Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet.</span></span>

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819f3-125">-Anforderungs-Nr</span><span class="sxs-lookup"><span data-stu-id="819f3-125">-RequestId</span></span>
<span data-ttu-id="819f3-126">Gibt die GUID des Import-oder Exportvorgangs an, für den dieses Cmdlet den Status erhält.</span><span class="sxs-lookup"><span data-stu-id="819f3-126">Specifies the GUID of the import or export operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="819f3-127">Wenn Sie diesen Parameter angeben, müssen Sie die Parameter *username* , *Password* und *Servername* angeben.</span><span class="sxs-lookup"><span data-stu-id="819f3-127">If you specify this parameter, you must specify the *UserName* , *Password* , and *ServerName* parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819f3-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="819f3-128">-ServerName</span></span>
<span data-ttu-id="819f3-129">Gibt den Namen des Azure SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="819f3-129">Specifies the name of the Azure SQL Database server.</span></span>
<span data-ttu-id="819f3-130">Sie müssen diesen Parameter angeben, wenn Sie den Parameter *Requestor* angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="819f3-130">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819f3-131">-Username</span><span class="sxs-lookup"><span data-stu-id="819f3-131">-Username</span></span>
<span data-ttu-id="819f3-132">Gibt den Benutzernamen an, der für die Verbindung mit dem Azure SQL-Datenbankserver erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="819f3-132">Specifies the user name required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="819f3-133">Sie müssen diesen Parameter angeben, wenn Sie den Parameter *Requestor* angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="819f3-133">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819f3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="819f3-134">CommonParameters</span></span>
<span data-ttu-id="819f3-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="819f3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="819f3-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="819f3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="819f3-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="819f3-137">INPUTS</span></span>

## <span data-ttu-id="819f3-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="819f3-138">OUTPUTS</span></span>

### <span data-ttu-id="819f3-139">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. DataObjects. StatusInfo</span><span class="sxs-lookup"><span data-stu-id="819f3-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExport.StatusInfo</span></span>

## <span data-ttu-id="819f3-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="819f3-140">NOTES</span></span>

## <span data-ttu-id="819f3-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="819f3-141">RELATED LINKS</span></span>

[<span data-ttu-id="819f3-142">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="819f3-142">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="819f3-143">Abrufen des Status der Import Export Datenbank</span><span class="sxs-lookup"><span data-stu-id="819f3-143">Get Import Export Database Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[<span data-ttu-id="819f3-144">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="819f3-144">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="819f3-145">Anfang-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="819f3-145">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)

[<span data-ttu-id="819f3-146">Anfang-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="819f3-146">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


