---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf6664023fbd43601c9b7c41a4f578809a9717c5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840867"
---
# <span data-ttu-id="ef5fc-101">Get-AzsTableService</span><span class="sxs-lookup"><span data-stu-id="ef5fc-101">Get-AzsTableService</span></span>

## <span data-ttu-id="ef5fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef5fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ef5fc-103">Gibt den tabellendienst zurück.</span><span class="sxs-lookup"><span data-stu-id="ef5fc-103">Returns the table service.</span></span>

## <span data-ttu-id="ef5fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef5fc-104">SYNTAX</span></span>

```
Get-AzsTableService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="ef5fc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef5fc-105">DESCRIPTION</span></span>
<span data-ttu-id="ef5fc-106">Gibt den tabellendienst zurück.</span><span class="sxs-lookup"><span data-stu-id="ef5fc-106">Returns the table service.</span></span>

## <span data-ttu-id="ef5fc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef5fc-107">EXAMPLES</span></span>

### <span data-ttu-id="ef5fc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ef5fc-108">EXAMPLE 1</span></span>
```
Get-AzsTableService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="ef5fc-109">Holen Sie sich die Tabelle Servie.</span><span class="sxs-lookup"><span data-stu-id="ef5fc-109">Get the table servie.</span></span>

## <span data-ttu-id="ef5fc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef5fc-110">PARAMETERS</span></span>

### <span data-ttu-id="ef5fc-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="ef5fc-111">-FarmName</span></span>
<span data-ttu-id="ef5fc-112">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="ef5fc-112">Farm Id.</span></span>

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

### <span data-ttu-id="ef5fc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef5fc-113">-ResourceGroupName</span></span>
<span data-ttu-id="ef5fc-114">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ef5fc-114">Resource group name.</span></span>

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

### <span data-ttu-id="ef5fc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef5fc-115">CommonParameters</span></span>
<span data-ttu-id="ef5fc-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef5fc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef5fc-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef5fc-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef5fc-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef5fc-118">INPUTS</span></span>

## <span data-ttu-id="ef5fc-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef5fc-119">OUTPUTS</span></span>

### <span data-ttu-id="ef5fc-120">Microsoft. AzureStack. Management. Storage. admin. Models. Dienst</span><span class="sxs-lookup"><span data-stu-id="ef5fc-120">Microsoft.AzureStack.Management.Storage.Admin.Models.TableService</span></span>

## <span data-ttu-id="ef5fc-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef5fc-121">NOTES</span></span>

## <span data-ttu-id="ef5fc-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef5fc-122">RELATED LINKS</span></span>
