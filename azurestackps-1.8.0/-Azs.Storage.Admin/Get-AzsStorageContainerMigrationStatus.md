---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0207d9d2353954fc1997f5752ac6dad26dbdfa13
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827995"
---
# <span data-ttu-id="2e075-101">Get-AzsStorageContainerMigrationStatus</span><span class="sxs-lookup"><span data-stu-id="2e075-101">Get-AzsStorageContainerMigrationStatus</span></span>

## <span data-ttu-id="2e075-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2e075-102">SYNOPSIS</span></span>
<span data-ttu-id="2e075-103">Gibt den Status eines Container Migrationsauftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="2e075-103">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="2e075-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e075-104">SYNTAX</span></span>

```
Get-AzsStorageContainerMigrationStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e075-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e075-105">DESCRIPTION</span></span>
<span data-ttu-id="2e075-106">Gibt den Status eines Container Migrationsauftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="2e075-106">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="2e075-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e075-107">EXAMPLES</span></span>

### <span data-ttu-id="2e075-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2e075-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageContainerMigrationStatus -FarmName "6ed442a3-ec47-4145-b2f0-9b90377b01d0" -JobId "6478ef3b-b7d5-4827-8d47-551c6afb9dd4"
```

<span data-ttu-id="2e075-109">Abrufen des Status eines Container Migrationsauftrags</span><span class="sxs-lookup"><span data-stu-id="2e075-109">Get the status of a container migration job.</span></span>

## <span data-ttu-id="2e075-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e075-110">PARAMETERS</span></span>

### <span data-ttu-id="2e075-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="2e075-111">-FarmName</span></span>
<span data-ttu-id="2e075-112">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="2e075-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e075-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="2e075-113">-JobId</span></span>
<span data-ttu-id="2e075-114">Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="2e075-114">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e075-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e075-115">-ResourceGroupName</span></span>
<span data-ttu-id="2e075-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2e075-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e075-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e075-117">CommonParameters</span></span>
<span data-ttu-id="2e075-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e075-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e075-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e075-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e075-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e075-120">INPUTS</span></span>

## <span data-ttu-id="2e075-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2e075-121">OUTPUTS</span></span>

### <span data-ttu-id="2e075-122">Microsoft. AzureStack. Management. Storage. admin. Models. MigrationResult</span><span class="sxs-lookup"><span data-stu-id="2e075-122">Microsoft.AzureStack.Management.Storage.Admin.Models.MigrationResult</span></span>

## <span data-ttu-id="2e075-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="2e075-123">NOTES</span></span>

## <span data-ttu-id="2e075-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2e075-124">RELATED LINKS</span></span>

