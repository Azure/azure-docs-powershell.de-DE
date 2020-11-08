---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96220d7bac0a71f579f81a4d01f4f1dc3cba9dd1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007097"
---
# <span data-ttu-id="37e09-101">Get-AzsStorageContainerMigrationStatus</span><span class="sxs-lookup"><span data-stu-id="37e09-101">Get-AzsStorageContainerMigrationStatus</span></span>

## <span data-ttu-id="37e09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37e09-102">SYNOPSIS</span></span>
<span data-ttu-id="37e09-103">Gibt den Status eines Container Migrationsauftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="37e09-103">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="37e09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37e09-104">SYNTAX</span></span>

```
Get-AzsStorageContainerMigrationStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="37e09-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37e09-105">DESCRIPTION</span></span>
<span data-ttu-id="37e09-106">Gibt den Status eines Container Migrationsauftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="37e09-106">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="37e09-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37e09-107">EXAMPLES</span></span>

### <span data-ttu-id="37e09-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37e09-108">EXAMPLE 1</span></span>
```
Get-AzsStorageContainerMigrationStatus -FarmName "6ed442a3-ec47-4145-b2f0-9b90377b01d0" -JobId "6478ef3b-b7d5-4827-8d47-551c6afb9dd4"
```

<span data-ttu-id="37e09-109">Abrufen des Status eines Container Migrationsauftrags</span><span class="sxs-lookup"><span data-stu-id="37e09-109">Get the status of a container migration job.</span></span>

## <span data-ttu-id="37e09-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="37e09-110">PARAMETERS</span></span>

### <span data-ttu-id="37e09-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="37e09-111">-FarmName</span></span>
<span data-ttu-id="37e09-112">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="37e09-112">Farm Id.</span></span>

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

### <span data-ttu-id="37e09-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="37e09-113">-JobId</span></span>
<span data-ttu-id="37e09-114">Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="37e09-114">Operation Id.</span></span>

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

### <span data-ttu-id="37e09-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37e09-115">-ResourceGroupName</span></span>
<span data-ttu-id="37e09-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="37e09-116">Resource group name.</span></span>

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

### <span data-ttu-id="37e09-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e09-117">CommonParameters</span></span>
<span data-ttu-id="37e09-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37e09-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e09-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37e09-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e09-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37e09-120">INPUTS</span></span>

## <span data-ttu-id="37e09-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37e09-121">OUTPUTS</span></span>

### <span data-ttu-id="37e09-122">Microsoft. AzureStack. Management. Storage. admin. Models. MigrationResult</span><span class="sxs-lookup"><span data-stu-id="37e09-122">Microsoft.AzureStack.Management.Storage.Admin.Models.MigrationResult</span></span>

## <span data-ttu-id="37e09-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="37e09-123">NOTES</span></span>

## <span data-ttu-id="37e09-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37e09-124">RELATED LINKS</span></span>
