---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9234cb73b1f9c3652827293ae2813f78d7ce336
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661990"
---
# <span data-ttu-id="78600-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="78600-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="78600-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78600-102">SYNOPSIS</span></span>
<span data-ttu-id="78600-103">Rufen Sie die Liste der Update Speicherorte ab.</span><span class="sxs-lookup"><span data-stu-id="78600-103">Get the list of update locations.</span></span>

## <span data-ttu-id="78600-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78600-104">SYNTAX</span></span>

### <span data-ttu-id="78600-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="78600-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="78600-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="78600-106">Get</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="78600-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="78600-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="78600-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78600-108">DESCRIPTION</span></span>
<span data-ttu-id="78600-109">Rufen Sie die Liste der Update Speicherorte ab.</span><span class="sxs-lookup"><span data-stu-id="78600-109">Get the list of update locations.</span></span> <span data-ttu-id="78600-110">Die zurückgegebenen Speicherorte können verwendet werden, um verfügbare Updates an einem bestimmten Speicherort mithilfe von Get-AzsUpdate abzurufen.</span><span class="sxs-lookup"><span data-stu-id="78600-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="78600-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78600-111">EXAMPLES</span></span>

### <span data-ttu-id="78600-112">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="78600-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="78600-113">Rufen Sie die Liste der Update Speicherorte ab.</span><span class="sxs-lookup"><span data-stu-id="78600-113">Get the list of update locations.</span></span>

## <span data-ttu-id="78600-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="78600-114">PARAMETERS</span></span>

### <span data-ttu-id="78600-115">-Name</span><span class="sxs-lookup"><span data-stu-id="78600-115">-Name</span></span>
<span data-ttu-id="78600-116">Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="78600-116">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78600-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78600-117">-ResourceGroupName</span></span>
<span data-ttu-id="78600-118">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="78600-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="78600-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="78600-119">-ResourceId</span></span>
<span data-ttu-id="78600-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="78600-120">The resource id.</span></span>

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

### <span data-ttu-id="78600-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78600-121">CommonParameters</span></span>
<span data-ttu-id="78600-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78600-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78600-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78600-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78600-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78600-124">INPUTS</span></span>

## <span data-ttu-id="78600-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78600-125">OUTPUTS</span></span>

### <span data-ttu-id="78600-126">Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation angegeben ist</span><span class="sxs-lookup"><span data-stu-id="78600-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="78600-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="78600-127">NOTES</span></span>

## <span data-ttu-id="78600-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78600-128">RELATED LINKS</span></span>

