---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: f1feead56c25b76890edd0fe183e65211294cf87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651480"
---
# <span data-ttu-id="e1ba5-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="e1ba5-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="e1ba5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1ba5-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ba5-103">Erstellt das DatabaseInfo-Objekt für den Azure-Daten Bank Migrationsdienst, der die Datenbankquelle für die Migration angibt.</span><span class="sxs-lookup"><span data-stu-id="e1ba5-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="e1ba5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1ba5-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1ba5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1ba5-105">DESCRIPTION</span></span>
<span data-ttu-id="e1ba5-106">Das New-AzDataMigrationDatabaseInfo-Cmdlet erstellt das DatabaseInfo-Objekt, das die zu migrierende Quelldaten Bank Instanz angibt.</span><span class="sxs-lookup"><span data-stu-id="e1ba5-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="e1ba5-107">Der Datenbankname wird als Eingabeparameter übernommen.</span><span class="sxs-lookup"><span data-stu-id="e1ba5-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="e1ba5-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1ba5-108">EXAMPLES</span></span>

### <span data-ttu-id="e1ba5-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e1ba5-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="e1ba5-110">Im vorangehenden Beispiel wird ein neues DatabaseInfo-Objekt für die Quelldatenbank- **AdventureWorks2016** erstellt.</span><span class="sxs-lookup"><span data-stu-id="e1ba5-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="e1ba5-111">Bei diesem Skript wird davon ausgegangen, dass Sie bereits bei Ihrem Azure-Konto angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="e1ba5-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="e1ba5-112">Sie können Ihren Anmeldestatus mithilfe des Get-AzSubscription-Cmdlets bestätigen.</span><span class="sxs-lookup"><span data-stu-id="e1ba5-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="e1ba5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1ba5-113">PARAMETERS</span></span>

### <span data-ttu-id="e1ba5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ba5-114">-DefaultProfile</span></span>
<span data-ttu-id="e1ba5-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1ba5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1ba5-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e1ba5-116">-SourceDatabaseName</span></span>
<span data-ttu-id="e1ba5-117">Name der Quelldatenbank.</span><span class="sxs-lookup"><span data-stu-id="e1ba5-117">Source Database Name.</span></span>

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

### <span data-ttu-id="e1ba5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ba5-118">CommonParameters</span></span>
<span data-ttu-id="e1ba5-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ba5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ba5-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ba5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ba5-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1ba5-121">INPUTS</span></span>

### <span data-ttu-id="e1ba5-122">Keine</span><span class="sxs-lookup"><span data-stu-id="e1ba5-122">None</span></span>

## <span data-ttu-id="e1ba5-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1ba5-123">OUTPUTS</span></span>

### <span data-ttu-id="e1ba5-124">Microsoft. Azure. Management. datamigration. Models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="e1ba5-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="e1ba5-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1ba5-125">NOTES</span></span>

## <span data-ttu-id="e1ba5-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1ba5-126">RELATED LINKS</span></span>
