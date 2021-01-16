---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: fe07416cd4c7ec9287937a405d8cfaf2a6111b23
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291718"
---
# <span data-ttu-id="8d7fd-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="8d7fd-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="8d7fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d7fd-102">SYNOPSIS</span></span>
<span data-ttu-id="8d7fd-103">Erstellt das DatabaseInfo-Objekt für den Azure-Datenbankmigrationsdienst, der die Datenbankquelle für die Migration angibt.</span><span class="sxs-lookup"><span data-stu-id="8d7fd-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="8d7fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d7fd-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d7fd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d7fd-105">DESCRIPTION</span></span>
<span data-ttu-id="8d7fd-106">Das New-AzDataMigrationDatabaseInfo erstellt das DatabaseInfo-Objekt, das die zu migrierende Quelldatenbankinstanz angibt.</span><span class="sxs-lookup"><span data-stu-id="8d7fd-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="8d7fd-107">Der Datenbankname wird als Eingabeparameter übernommen.</span><span class="sxs-lookup"><span data-stu-id="8d7fd-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="8d7fd-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8d7fd-108">EXAMPLES</span></span>

### <span data-ttu-id="8d7fd-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8d7fd-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="8d7fd-110">Im vorherigen Beispiel wird ein neues DatabaseInfo-Objekt für die Quelldatenbank **"AdventureWorks2016" erstellt.**</span><span class="sxs-lookup"><span data-stu-id="8d7fd-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="8d7fd-111">Bei diesem Skript wird davon ausgegangen, dass Sie bereits bei Ihrem Azure-Konto angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="8d7fd-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="8d7fd-112">Sie können Ihren Anmeldestatus mithilfe des cmdlets Get-AzSubscription bestätigen.</span><span class="sxs-lookup"><span data-stu-id="8d7fd-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="8d7fd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d7fd-113">PARAMETERS</span></span>

### <span data-ttu-id="8d7fd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d7fd-114">-DefaultProfile</span></span>
<span data-ttu-id="8d7fd-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d7fd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d7fd-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8d7fd-116">-SourceDatabaseName</span></span>
<span data-ttu-id="8d7fd-117">Quelldatenbankname.</span><span class="sxs-lookup"><span data-stu-id="8d7fd-117">Source Database Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d7fd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d7fd-118">CommonParameters</span></span>
<span data-ttu-id="8d7fd-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d7fd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d7fd-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d7fd-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d7fd-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8d7fd-121">INPUTS</span></span>

### <span data-ttu-id="8d7fd-122">Keine</span><span class="sxs-lookup"><span data-stu-id="8d7fd-122">None</span></span>

## <span data-ttu-id="8d7fd-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8d7fd-123">OUTPUTS</span></span>

### <span data-ttu-id="8d7fd-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="8d7fd-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="8d7fd-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8d7fd-125">NOTES</span></span>

## <span data-ttu-id="8d7fd-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8d7fd-126">RELATED LINKS</span></span>
