---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dd280133b3a0bc536c57f839fcc0faab81669c03
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840656"
---
# <span data-ttu-id="cac17-101">Get-AzsStorageFarm</span><span class="sxs-lookup"><span data-stu-id="cac17-101">Get-AzsStorageFarm</span></span>

## <span data-ttu-id="cac17-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cac17-102">SYNOPSIS</span></span>
<span data-ttu-id="cac17-103">Gibt eine Liste aller Speicher Farmen zurück.</span><span class="sxs-lookup"><span data-stu-id="cac17-103">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="cac17-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cac17-104">SYNTAX</span></span>

### <span data-ttu-id="cac17-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="cac17-105">List (Default)</span></span>
```
Get-AzsStorageFarm [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="cac17-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="cac17-106">Get</span></span>
```
Get-AzsStorageFarm [-Name] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="cac17-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cac17-107">ResourceId</span></span>
```
Get-AzsStorageFarm -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="cac17-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cac17-108">DESCRIPTION</span></span>
<span data-ttu-id="cac17-109">Gibt eine Liste aller Speicher Farmen zurück.</span><span class="sxs-lookup"><span data-stu-id="cac17-109">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="cac17-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cac17-110">EXAMPLES</span></span>

### <span data-ttu-id="cac17-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cac17-111">EXAMPLE 1</span></span>
```
Get-AzsStorageFarm
```

<span data-ttu-id="cac17-112">Abrufen der Liste aller Speicher Farmen</span><span class="sxs-lookup"><span data-stu-id="cac17-112">Get the list of all storage farms.</span></span>

## <span data-ttu-id="cac17-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="cac17-113">PARAMETERS</span></span>

### <span data-ttu-id="cac17-114">-Name</span><span class="sxs-lookup"><span data-stu-id="cac17-114">-Name</span></span>
<span data-ttu-id="cac17-115">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="cac17-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cac17-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cac17-116">-ResourceGroupName</span></span>
<span data-ttu-id="cac17-117">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cac17-117">Resource group name.</span></span>

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

### <span data-ttu-id="cac17-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cac17-118">-ResourceId</span></span>
<span data-ttu-id="cac17-119">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="cac17-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cac17-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="cac17-120">-Skip</span></span>
<span data-ttu-id="cac17-121">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="cac17-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cac17-122">-Top</span><span class="sxs-lookup"><span data-stu-id="cac17-122">-Top</span></span>
<span data-ttu-id="cac17-123">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="cac17-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="cac17-124">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="cac17-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cac17-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cac17-125">CommonParameters</span></span>
<span data-ttu-id="cac17-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cac17-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cac17-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cac17-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cac17-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cac17-128">INPUTS</span></span>

## <span data-ttu-id="cac17-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cac17-129">OUTPUTS</span></span>

### <span data-ttu-id="cac17-130">Microsoft. AzureStack. Management. Storage. admin. Models. Farm</span><span class="sxs-lookup"><span data-stu-id="cac17-130">Microsoft.AzureStack.Management.Storage.Admin.Models.Farm</span></span>

## <span data-ttu-id="cac17-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="cac17-131">NOTES</span></span>

## <span data-ttu-id="cac17-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cac17-132">RELATED LINKS</span></span>
