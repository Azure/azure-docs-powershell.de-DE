---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d38e4bd949a6118f55ce0096a8ca56d08137bb2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827411"
---
# <span data-ttu-id="083e7-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="083e7-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="083e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="083e7-102">SYNOPSIS</span></span>
<span data-ttu-id="083e7-103">Abbrechen eines verwalteten Datenträger Migrationsauftrags</span><span class="sxs-lookup"><span data-stu-id="083e7-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="083e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="083e7-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="083e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="083e7-105">DESCRIPTION</span></span>
<span data-ttu-id="083e7-106">Abbrechen eines Datenträger Migrationsauftrags</span><span class="sxs-lookup"><span data-stu-id="083e7-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="083e7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="083e7-107">EXAMPLES</span></span>

### <span data-ttu-id="083e7-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="083e7-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="083e7-109">Abbrechen eines verwalteten Datenträger Migrationsauftrags</span><span class="sxs-lookup"><span data-stu-id="083e7-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="083e7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="083e7-110">PARAMETERS</span></span>

### <span data-ttu-id="083e7-111">-Standort</span><span class="sxs-lookup"><span data-stu-id="083e7-111">-Location</span></span>
<span data-ttu-id="083e7-112">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="083e7-112">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083e7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="083e7-113">-Name</span></span>
<span data-ttu-id="083e7-114">Der GUID-Name des Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="083e7-114">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083e7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="083e7-115">CommonParameters</span></span>
<span data-ttu-id="083e7-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="083e7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="083e7-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="083e7-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="083e7-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="083e7-118">INPUTS</span></span>

## <span data-ttu-id="083e7-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="083e7-119">OUTPUTS</span></span>

### <span data-ttu-id="083e7-120">Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="083e7-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="083e7-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="083e7-121">NOTES</span></span>

## <span data-ttu-id="083e7-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="083e7-122">RELATED LINKS</span></span>

