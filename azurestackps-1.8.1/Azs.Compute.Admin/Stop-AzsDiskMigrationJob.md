---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee1a9ae5a4d5ef7545ee9a3e071fcc06475034f4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828299"
---
# <span data-ttu-id="25780-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="25780-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="25780-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25780-102">SYNOPSIS</span></span>
<span data-ttu-id="25780-103">Abbrechen eines verwalteten Datenträger Migrationsauftrags</span><span class="sxs-lookup"><span data-stu-id="25780-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="25780-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25780-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="25780-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25780-105">DESCRIPTION</span></span>
<span data-ttu-id="25780-106">Abbrechen eines Datenträger Migrationsauftrags</span><span class="sxs-lookup"><span data-stu-id="25780-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="25780-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25780-107">EXAMPLES</span></span>

### <span data-ttu-id="25780-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="25780-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="25780-109">Abbrechen eines verwalteten Datenträger Migrationsauftrags</span><span class="sxs-lookup"><span data-stu-id="25780-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="25780-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="25780-110">PARAMETERS</span></span>

### <span data-ttu-id="25780-111">-Standort</span><span class="sxs-lookup"><span data-stu-id="25780-111">-Location</span></span>
<span data-ttu-id="25780-112">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="25780-112">Location of the resource.</span></span>

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

### <span data-ttu-id="25780-113">-Name</span><span class="sxs-lookup"><span data-stu-id="25780-113">-Name</span></span>
<span data-ttu-id="25780-114">Der GUID-Name des Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="25780-114">The migration job guid name.</span></span>

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

### <span data-ttu-id="25780-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25780-115">CommonParameters</span></span>
<span data-ttu-id="25780-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25780-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25780-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25780-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25780-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25780-118">INPUTS</span></span>

## <span data-ttu-id="25780-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25780-119">OUTPUTS</span></span>

### <span data-ttu-id="25780-120">Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="25780-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="25780-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="25780-121">NOTES</span></span>

## <span data-ttu-id="25780-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25780-122">RELATED LINKS</span></span>

