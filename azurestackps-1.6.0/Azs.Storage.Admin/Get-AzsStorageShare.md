---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cc6e2adff73e4b7c81a401bb98e9ab625005ae3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661943"
---
# <span data-ttu-id="e3de9-101">Get-AzsStorageShare</span><span class="sxs-lookup"><span data-stu-id="e3de9-101">Get-AzsStorageShare</span></span>

## <span data-ttu-id="e3de9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3de9-102">SYNOPSIS</span></span>
<span data-ttu-id="e3de9-103">Gibt eine Liste von Speicherfreigaben zurück.</span><span class="sxs-lookup"><span data-stu-id="e3de9-103">Returns a list of storage shares.</span></span>

## <span data-ttu-id="e3de9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3de9-104">SYNTAX</span></span>

### <span data-ttu-id="e3de9-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="e3de9-105">List (Default)</span></span>
```
Get-AzsStorageShare -FarmName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e3de9-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="e3de9-106">Get</span></span>
```
Get-AzsStorageShare -FarmName <String> -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e3de9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3de9-107">ResourceId</span></span>
```
Get-AzsStorageShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e3de9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3de9-108">DESCRIPTION</span></span>
<span data-ttu-id="e3de9-109">Gibt eine Liste von Speicherfreigaben zurück.</span><span class="sxs-lookup"><span data-stu-id="e3de9-109">Returns a list of storage shares.</span></span>

## <span data-ttu-id="e3de9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3de9-110">EXAMPLES</span></span>

### <span data-ttu-id="e3de9-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e3de9-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="e3de9-112">Rufen Sie die Liste der Speicherfreigaben ab.</span><span class="sxs-lookup"><span data-stu-id="e3de9-112">Get the list of storage shares.</span></span>

## <span data-ttu-id="e3de9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3de9-113">PARAMETERS</span></span>

### <span data-ttu-id="e3de9-114">-Farmname</span><span class="sxs-lookup"><span data-stu-id="e3de9-114">-FarmName</span></span>
<span data-ttu-id="e3de9-115">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="e3de9-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3de9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e3de9-116">-Name</span></span>
<span data-ttu-id="e3de9-117">Freigabename.</span><span class="sxs-lookup"><span data-stu-id="e3de9-117">Share name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3de9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3de9-118">-ResourceGroupName</span></span>
<span data-ttu-id="e3de9-119">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e3de9-119">Resource group name.</span></span>

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

### <span data-ttu-id="e3de9-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e3de9-120">-ResourceId</span></span>
<span data-ttu-id="e3de9-121">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e3de9-121">The resource id.</span></span>

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

### <span data-ttu-id="e3de9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3de9-122">CommonParameters</span></span>
<span data-ttu-id="e3de9-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3de9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3de9-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3de9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3de9-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3de9-125">INPUTS</span></span>

## <span data-ttu-id="e3de9-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3de9-126">OUTPUTS</span></span>

### <span data-ttu-id="e3de9-127">Microsoft. AzureStack. Management. Storage. admin. Models. share</span><span class="sxs-lookup"><span data-stu-id="e3de9-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Share</span></span>

## <span data-ttu-id="e3de9-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3de9-128">NOTES</span></span>

## <span data-ttu-id="e3de9-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3de9-129">RELATED LINKS</span></span>

