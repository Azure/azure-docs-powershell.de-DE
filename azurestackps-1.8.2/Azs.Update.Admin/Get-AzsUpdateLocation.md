---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007141"
---
# <span data-ttu-id="1ae6a-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="1ae6a-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="1ae6a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1ae6a-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae6a-103">Rufen Sie die Liste der Update Speicherorte ab.</span><span class="sxs-lookup"><span data-stu-id="1ae6a-103">Get the list of update locations.</span></span>

## <span data-ttu-id="1ae6a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ae6a-104">SYNTAX</span></span>

### <span data-ttu-id="1ae6a-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="1ae6a-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1ae6a-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="1ae6a-106">Get</span></span>
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1ae6a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ae6a-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1ae6a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ae6a-108">DESCRIPTION</span></span>
<span data-ttu-id="1ae6a-109">Rufen Sie die Liste der Update Speicherorte ab.</span><span class="sxs-lookup"><span data-stu-id="1ae6a-109">Get the list of update locations.</span></span> <span data-ttu-id="1ae6a-110">Die zurückgegebenen Speicherorte können verwendet werden, um verfügbare Updates an einem bestimmten Speicherort mithilfe von Get-AzsUpdate abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1ae6a-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="1ae6a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ae6a-111">EXAMPLES</span></span>

### <span data-ttu-id="1ae6a-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1ae6a-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="1ae6a-113">Rufen Sie die Liste der Update Speicherorte ab.</span><span class="sxs-lookup"><span data-stu-id="1ae6a-113">Get the list of update locations.</span></span>

## <span data-ttu-id="1ae6a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ae6a-114">PARAMETERS</span></span>

### <span data-ttu-id="1ae6a-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="1ae6a-115">-Location</span></span>
<span data-ttu-id="1ae6a-116">Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="1ae6a-116">Name of the Location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae6a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae6a-117">-ResourceGroupName</span></span>
<span data-ttu-id="1ae6a-118">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="1ae6a-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae6a-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1ae6a-119">-ResourceId</span></span>
<span data-ttu-id="1ae6a-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="1ae6a-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae6a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae6a-121">CommonParameters</span></span>
<span data-ttu-id="1ae6a-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae6a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae6a-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae6a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae6a-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ae6a-124">INPUTS</span></span>

## <span data-ttu-id="1ae6a-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1ae6a-125">OUTPUTS</span></span>

### <span data-ttu-id="1ae6a-126">Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation angegeben ist</span><span class="sxs-lookup"><span data-stu-id="1ae6a-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="1ae6a-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ae6a-127">NOTES</span></span>

## <span data-ttu-id="1ae6a-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1ae6a-128">RELATED LINKS</span></span>
