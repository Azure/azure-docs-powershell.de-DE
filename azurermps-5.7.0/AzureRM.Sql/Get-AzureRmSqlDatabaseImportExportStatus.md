---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
ms.openlocfilehash: 9a1c56f528b9865e1a68e74d35885fc6f8b24bf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476505"
---
# <span data-ttu-id="1cdd0-101">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="1cdd0-101">Get-AzureRmSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="1cdd0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1cdd0-102">SYNOPSIS</span></span>
<span data-ttu-id="1cdd0-103">Ruft die Details eines Imports oder Exports einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cdd0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cdd0-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseImportExportStatus [-OperationStatusLink] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cdd0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1cdd0-105">DESCRIPTION</span></span>
<span data-ttu-id="1cdd0-106">Das Cmdlet " **Get-AzureRmSqlDatabaseImportExportStatus** " ruft Details zu einem BacPac-Dateiimport von einem Speicherkonto in eine Azure SQL-Datenbank oder den Export einer Azure SQL-Datenbank als BacPac-Datei in ein Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-106">The **Get-AzureRmSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>

<span data-ttu-id="1cdd0-107">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1cdd0-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1cdd0-108">EXAMPLES</span></span>

### <span data-ttu-id="1cdd0-109">Beispiel 1: Abrufen des Import-und Exportstatus einer SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="1cdd0-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="1cdd0-110">Dieser Befehl ruft den Status einer Import-oder Exportanforderung für eine Datenbank unter der angegebenen URL ab.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="1cdd0-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cdd0-111">PARAMETERS</span></span>

### <span data-ttu-id="1cdd0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cdd0-112">-DefaultProfile</span></span>
<span data-ttu-id="1cdd0-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1cdd0-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1cdd0-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="1cdd0-114">-OperationStatusLink</span></span>
<span data-ttu-id="1cdd0-115">Gibt den Status Link an, der von den Cmdlets New-AzureRmSqlDatabaseExport oder New-AzureRmSqlDatabaseImport zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-115">Specifies the status link that is returned from the New-AzureRmSqlDatabaseExport or New-AzureRmSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="1cdd0-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1cdd0-116">-Confirm</span></span>
<span data-ttu-id="1cdd0-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cdd0-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cdd0-118">-WhatIf</span></span>
<span data-ttu-id="1cdd0-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cdd0-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cdd0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cdd0-121">CommonParameters</span></span>
<span data-ttu-id="1cdd0-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cdd0-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cdd0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cdd0-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1cdd0-124">INPUTS</span></span>

### <span data-ttu-id="1cdd0-125">Keine</span><span class="sxs-lookup"><span data-stu-id="1cdd0-125">None</span></span>
<span data-ttu-id="1cdd0-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1cdd0-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1cdd0-127">OUTPUTS</span></span>

## <span data-ttu-id="1cdd0-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="1cdd0-128">NOTES</span></span>
* <span data-ttu-id="1cdd0-129">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL</span><span class="sxs-lookup"><span data-stu-id="1cdd0-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="1cdd0-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1cdd0-130">RELATED LINKS</span></span>

[<span data-ttu-id="1cdd0-131">Neu – AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="1cdd0-131">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="1cdd0-132">Neu – AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="1cdd0-132">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="1cdd0-133">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="1cdd0-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
