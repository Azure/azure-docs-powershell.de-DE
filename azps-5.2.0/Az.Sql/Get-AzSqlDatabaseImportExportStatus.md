---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
ms.openlocfilehash: c64f726e8ff553aa42cb8580cee2349b35de519e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302152"
---
# <span data-ttu-id="88bb2-101">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="88bb2-101">Get-AzSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="88bb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="88bb2-103">Ruft die Details eines Imports oder Exports einer Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="88bb2-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

## <span data-ttu-id="88bb2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88bb2-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseImportExportStatus [-OperationStatusLink] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88bb2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88bb2-105">DESCRIPTION</span></span>
<span data-ttu-id="88bb2-106">Das **Cmdlet "Get-AzSqlDatabaseImportExportStatus"** ruft Details eines Bacpac-Dateiimports aus einem Speicherkonto in eine Azure SQL-Datenbank oder einen Export einer Azure SQL-Datenbank als Bacpac-Datei in ein Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="88bb2-106">The **Get-AzSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="88bb2-107">Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88bb2-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="88bb2-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="88bb2-108">EXAMPLES</span></span>

### <span data-ttu-id="88bb2-109">Beispiel 1: Anzeigen des Import- und Exportstatus einer SQL Datenbank</span><span class="sxs-lookup"><span data-stu-id="88bb2-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="88bb2-110">Dieser Befehl ruft den Status einer Import- oder Exportanforderung für eine Datenbank unter der angegebenen URL ab.</span><span class="sxs-lookup"><span data-stu-id="88bb2-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="88bb2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88bb2-111">PARAMETERS</span></span>

### <span data-ttu-id="88bb2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88bb2-112">-DefaultProfile</span></span>
<span data-ttu-id="88bb2-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="88bb2-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88bb2-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="88bb2-114">-OperationStatusLink</span></span>
<span data-ttu-id="88bb2-115">Gibt die Statusverknüpfung an, die von den cmdlets New-AzSqlDatabaseExport oder New-AzSqlDatabaseImport zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="88bb2-115">Specifies the status link that is returned from the New-AzSqlDatabaseExport or New-AzSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="88bb2-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88bb2-116">-Confirm</span></span>
<span data-ttu-id="88bb2-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="88bb2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88bb2-118">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="88bb2-118">-WhatIf</span></span>
<span data-ttu-id="88bb2-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88bb2-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88bb2-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88bb2-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88bb2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88bb2-121">CommonParameters</span></span>
<span data-ttu-id="88bb2-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88bb2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88bb2-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88bb2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88bb2-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="88bb2-124">INPUTS</span></span>

### <span data-ttu-id="88bb2-125">System.String</span><span class="sxs-lookup"><span data-stu-id="88bb2-125">System.String</span></span>

## <span data-ttu-id="88bb2-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="88bb2-126">OUTPUTS</span></span>

### <span data-ttu-id="88bb2-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span><span class="sxs-lookup"><span data-stu-id="88bb2-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="88bb2-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="88bb2-128">NOTES</span></span>
* <span data-ttu-id="88bb2-129">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="88bb2-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="88bb2-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="88bb2-130">RELATED LINKS</span></span>

[<span data-ttu-id="88bb2-131">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="88bb2-131">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="88bb2-132">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="88bb2-132">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="88bb2-133">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="88bb2-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
