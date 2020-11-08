---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a53b5af4cf77ec961e65f8c0c0d84b05b4adfa1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007098"
---
# <span data-ttu-id="39d6a-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="39d6a-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="39d6a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="39d6a-103">Gibt eine Liste der BLOB-Akquisitionen zurück.</span><span class="sxs-lookup"><span data-stu-id="39d6a-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="39d6a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39d6a-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="39d6a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39d6a-105">DESCRIPTION</span></span>
<span data-ttu-id="39d6a-106">Gibt eine Liste der BLOB-Akquisitionen zurück.</span><span class="sxs-lookup"><span data-stu-id="39d6a-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="39d6a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39d6a-107">EXAMPLES</span></span>

### <span data-ttu-id="39d6a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="39d6a-108">EXAMPLE 1</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="39d6a-109">Rufen Sie die Liste der BLOB-Akquisitionen.</span><span class="sxs-lookup"><span data-stu-id="39d6a-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="39d6a-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="39d6a-110">EXAMPLE 2</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="39d6a-111">Rufen Sie die Liste der BLOB-Akquisitionen.</span><span class="sxs-lookup"><span data-stu-id="39d6a-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="39d6a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="39d6a-112">PARAMETERS</span></span>

### <span data-ttu-id="39d6a-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="39d6a-113">-FarmName</span></span>
<span data-ttu-id="39d6a-114">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="39d6a-114">Farm Id.</span></span>

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

### <span data-ttu-id="39d6a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39d6a-115">-ResourceGroupName</span></span>
<span data-ttu-id="39d6a-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="39d6a-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39d6a-117">-Filter</span><span class="sxs-lookup"><span data-stu-id="39d6a-117">-Filter</span></span>
<span data-ttu-id="39d6a-118">Filter Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="39d6a-118">Filter string</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39d6a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d6a-119">CommonParameters</span></span>
<span data-ttu-id="39d6a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39d6a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d6a-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39d6a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d6a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39d6a-122">INPUTS</span></span>

## <span data-ttu-id="39d6a-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39d6a-123">OUTPUTS</span></span>

## <span data-ttu-id="39d6a-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="39d6a-124">NOTES</span></span>

## <span data-ttu-id="39d6a-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39d6a-125">RELATED LINKS</span></span>
