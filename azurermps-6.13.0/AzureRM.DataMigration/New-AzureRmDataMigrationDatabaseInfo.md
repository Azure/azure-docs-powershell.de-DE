---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: c04a79a54e42c64fe897a419565e4816964879b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665174"
---
# <span data-ttu-id="539ee-101">New-AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="539ee-101">New-AzureRmDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="539ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="539ee-102">SYNOPSIS</span></span>
<span data-ttu-id="539ee-103">Erstellt das DatabaseInfo-Objekt für den Azure-Daten Bank Migrationsdienst, der die Datenbankquelle für die Migration angibt.</span><span class="sxs-lookup"><span data-stu-id="539ee-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="539ee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="539ee-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="539ee-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="539ee-105">DESCRIPTION</span></span>
<span data-ttu-id="539ee-106">Das New-AzureRmDataMigrationDatabaseInfo-Cmdlet erstellt das DatabaseInfo-Objekt, das die zu migrierende Quelldaten Bank Instanz angibt.</span><span class="sxs-lookup"><span data-stu-id="539ee-106">The New-AzureRmDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="539ee-107">Der Datenbankname wird als Eingabeparameter übernommen.</span><span class="sxs-lookup"><span data-stu-id="539ee-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="539ee-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="539ee-108">EXAMPLES</span></span>

### <span data-ttu-id="539ee-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="539ee-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="539ee-110">Im vorangehenden Beispiel wird ein neues DatabaseInfo-Objekt für die Quelldatenbank- **AdventureWorks2016** erstellt.</span><span class="sxs-lookup"><span data-stu-id="539ee-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="539ee-111">Bei diesem Skript wird davon ausgegangen, dass Sie bereits bei Ihrem Azure-Konto angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="539ee-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="539ee-112">Sie können Ihren Anmeldestatus mithilfe des Get-AzureSubscription-Cmdlets bestätigen.</span><span class="sxs-lookup"><span data-stu-id="539ee-112">You can confirm your login status by using the Get-AzureSubscription cmdlet.</span></span>

## <span data-ttu-id="539ee-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="539ee-113">PARAMETERS</span></span>

### <span data-ttu-id="539ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="539ee-114">-DefaultProfile</span></span>
<span data-ttu-id="539ee-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="539ee-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="539ee-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="539ee-116">-SourceDatabaseName</span></span>
<span data-ttu-id="539ee-117">Name der Quelldatenbank.</span><span class="sxs-lookup"><span data-stu-id="539ee-117">Source Database Name.</span></span>

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

### <span data-ttu-id="539ee-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="539ee-118">CommonParameters</span></span>
<span data-ttu-id="539ee-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="539ee-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="539ee-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="539ee-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="539ee-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="539ee-121">INPUTS</span></span>

### <span data-ttu-id="539ee-122">Keine</span><span class="sxs-lookup"><span data-stu-id="539ee-122">None</span></span>

## <span data-ttu-id="539ee-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="539ee-123">OUTPUTS</span></span>

### <span data-ttu-id="539ee-124">Microsoft. Azure. Management. datamigration. Models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="539ee-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="539ee-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="539ee-125">NOTES</span></span>

## <span data-ttu-id="539ee-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="539ee-126">RELATED LINKS</span></span>
