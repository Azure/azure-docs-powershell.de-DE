---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d9ff0746de44d2e5c3c67ea95b66dd3bd3902ca
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93828035"
---
# <span data-ttu-id="2932f-101">Get-AzsBlobService</span><span class="sxs-lookup"><span data-stu-id="2932f-101">Get-AzsBlobService</span></span>

## <span data-ttu-id="2932f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2932f-102">SYNOPSIS</span></span>
<span data-ttu-id="2932f-103">Gibt den BLOB-Dienst zurück.</span><span class="sxs-lookup"><span data-stu-id="2932f-103">Returns the blob service.</span></span>

## <span data-ttu-id="2932f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2932f-104">SYNTAX</span></span>

```
Get-AzsBlobService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="2932f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2932f-105">DESCRIPTION</span></span>
<span data-ttu-id="2932f-106">Gibt den BLOB-Dienst zurück.</span><span class="sxs-lookup"><span data-stu-id="2932f-106">Returns the blob service.</span></span>

## <span data-ttu-id="2932f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2932f-107">EXAMPLES</span></span>

### <span data-ttu-id="2932f-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2932f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBlobService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="2932f-109">Rufen Sie den BLOB-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="2932f-109">Get the blob service.</span></span>

## <span data-ttu-id="2932f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2932f-110">PARAMETERS</span></span>

### <span data-ttu-id="2932f-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="2932f-111">-FarmName</span></span>
<span data-ttu-id="2932f-112">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="2932f-112">Farm Id.</span></span>

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

### <span data-ttu-id="2932f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2932f-113">-ResourceGroupName</span></span>
<span data-ttu-id="2932f-114">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2932f-114">Resource group name.</span></span>

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

### <span data-ttu-id="2932f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2932f-115">CommonParameters</span></span>
<span data-ttu-id="2932f-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2932f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2932f-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2932f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2932f-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2932f-118">INPUTS</span></span>

## <span data-ttu-id="2932f-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2932f-119">OUTPUTS</span></span>

### <span data-ttu-id="2932f-120">Microsoft. AzureStack. Management. Storage. admin. Models. BlobService</span><span class="sxs-lookup"><span data-stu-id="2932f-120">Microsoft.AzureStack.Management.Storage.Admin.Models.BlobService</span></span>

## <span data-ttu-id="2932f-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="2932f-121">NOTES</span></span>

## <span data-ttu-id="2932f-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2932f-122">RELATED LINKS</span></span>

