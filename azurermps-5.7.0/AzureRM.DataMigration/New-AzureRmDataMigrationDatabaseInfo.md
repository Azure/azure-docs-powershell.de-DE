---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationdatabaseinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: 3b0729b07667e634f060293bd8593ed237606460
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664665"
---
# <span data-ttu-id="362c3-101">New-AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="362c3-101">New-AzureRmDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="362c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="362c3-102">SYNOPSIS</span></span>
<span data-ttu-id="362c3-103">Erstellt das DatabaseInfo-Objekt für den Azure-Daten Bank Migrationsdienst, der die Datenbankquelle für die Migration angibt.</span><span class="sxs-lookup"><span data-stu-id="362c3-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="362c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="362c3-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="362c3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="362c3-105">DESCRIPTION</span></span>
<span data-ttu-id="362c3-106">Das New-AzureRmDataMigrationDatabaseInfo-Cmdlet erstellt das DatabaseInfo-Objekt, das die zu migrierende Quelldaten Bank Instanz angibt.</span><span class="sxs-lookup"><span data-stu-id="362c3-106">The New-AzureRmDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="362c3-107">Der Datenbankname wird als Eingabeparameter übernommen.</span><span class="sxs-lookup"><span data-stu-id="362c3-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="362c3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="362c3-108">EXAMPLES</span></span>

### <span data-ttu-id="362c3-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="362c3-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="362c3-110">Im vorangehenden Beispiel wird ein neues DatabaseInfo-Objekt für die Quelldatenbank- **AdventureWorks2016** erstellt.</span><span class="sxs-lookup"><span data-stu-id="362c3-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>

<span data-ttu-id="362c3-111">Bei diesem Skript wird davon ausgegangen, dass Sie bereits bei Ihrem Azure-Konto angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="362c3-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="362c3-112">Sie können Ihren Anmeldestatus mithilfe des Get-AzureSubscription-Cmdlets bestätigen.</span><span class="sxs-lookup"><span data-stu-id="362c3-112">You can confirm your login status by using the Get-AzureSubscription cmdlet.</span></span>

## <span data-ttu-id="362c3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="362c3-113">PARAMETERS</span></span>

### <span data-ttu-id="362c3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="362c3-114">-DefaultProfile</span></span>
<span data-ttu-id="362c3-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="362c3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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
### <span data-ttu-id="362c3-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="362c3-116">-Confirm</span></span>
<span data-ttu-id="362c3-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="362c3-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="362c3-118">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="362c3-118">-SourceDatabaseName</span></span>
<span data-ttu-id="362c3-119">Name der Quelldatenbank.</span><span class="sxs-lookup"><span data-stu-id="362c3-119">Source Database Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="362c3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="362c3-120">-WhatIf</span></span>
<span data-ttu-id="362c3-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="362c3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="362c3-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="362c3-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="362c3-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="362c3-123">INPUTS</span></span>

### <span data-ttu-id="362c3-124">Keine</span><span class="sxs-lookup"><span data-stu-id="362c3-124">None</span></span>


## <span data-ttu-id="362c3-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="362c3-125">OUTPUTS</span></span>

### <span data-ttu-id="362c3-126">Microsoft. Azure. Management. datamigration. Models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="362c3-126">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>


## <span data-ttu-id="362c3-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="362c3-127">NOTES</span></span>

## <span data-ttu-id="362c3-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="362c3-128">RELATED LINKS</span></span>


