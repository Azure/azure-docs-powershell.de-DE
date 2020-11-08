---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
ms.openlocfilehash: c64f726e8ff553aa42cb8580cee2349b35de519e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173470"
---
# <span data-ttu-id="1b86b-101">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="1b86b-101">Get-AzSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="1b86b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1b86b-102">SYNOPSIS</span></span>
<span data-ttu-id="1b86b-103">Ruft die Details eines Imports oder Exports einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="1b86b-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

## <span data-ttu-id="1b86b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b86b-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseImportExportStatus [-OperationStatusLink] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b86b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b86b-105">DESCRIPTION</span></span>
<span data-ttu-id="1b86b-106">Das Cmdlet " **Get-AzSqlDatabaseImportExportStatus** " ruft Details zu einem BacPac-Dateiimport von einem Speicherkonto in eine Azure SQL-Datenbank oder den Export einer Azure SQL-Datenbank als BacPac-Datei in ein Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="1b86b-106">The **Get-AzSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="1b86b-107">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1b86b-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1b86b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b86b-108">EXAMPLES</span></span>

### <span data-ttu-id="1b86b-109">Beispiel 1: Abrufen des Import-und Exportstatus einer SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="1b86b-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="1b86b-110">Dieser Befehl ruft den Status einer Import-oder Exportanforderung für eine Datenbank unter der angegebenen URL ab.</span><span class="sxs-lookup"><span data-stu-id="1b86b-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="1b86b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b86b-111">PARAMETERS</span></span>

### <span data-ttu-id="1b86b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b86b-112">-DefaultProfile</span></span>
<span data-ttu-id="1b86b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1b86b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b86b-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="1b86b-114">-OperationStatusLink</span></span>
<span data-ttu-id="1b86b-115">Gibt den Status Link an, der von den Cmdlets New-AzSqlDatabaseExport oder New-AzSqlDatabaseImport zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1b86b-115">Specifies the status link that is returned from the New-AzSqlDatabaseExport or New-AzSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="1b86b-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1b86b-116">-Confirm</span></span>
<span data-ttu-id="1b86b-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b86b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b86b-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b86b-118">-WhatIf</span></span>
<span data-ttu-id="1b86b-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b86b-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b86b-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b86b-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b86b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b86b-121">CommonParameters</span></span>
<span data-ttu-id="1b86b-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b86b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b86b-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b86b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b86b-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1b86b-124">INPUTS</span></span>

### <span data-ttu-id="1b86b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1b86b-125">System.String</span></span>

## <span data-ttu-id="1b86b-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1b86b-126">OUTPUTS</span></span>

### <span data-ttu-id="1b86b-127">Microsoft. Azure. Commands. SQL. DataObjects. Model. AzureSqlDatabaseImportExportStatusModel</span><span class="sxs-lookup"><span data-stu-id="1b86b-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="1b86b-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="1b86b-128">NOTES</span></span>
* <span data-ttu-id="1b86b-129">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL</span><span class="sxs-lookup"><span data-stu-id="1b86b-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="1b86b-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1b86b-130">RELATED LINKS</span></span>

[<span data-ttu-id="1b86b-131">Neu – AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="1b86b-131">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="1b86b-132">Neu – AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="1b86b-132">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="1b86b-133">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="1b86b-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
