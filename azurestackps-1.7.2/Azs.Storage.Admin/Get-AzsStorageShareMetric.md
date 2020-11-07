---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1e5679c04e31fecf837154e0cc41b484d1ab4843
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826664"
---
# <span data-ttu-id="53a58-101">Get-AzsStorageShareMetric</span><span class="sxs-lookup"><span data-stu-id="53a58-101">Get-AzsStorageShareMetric</span></span>

## <span data-ttu-id="53a58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53a58-102">SYNOPSIS</span></span>
<span data-ttu-id="53a58-103">Gibt eine Liste von Metriken für eine Speicherfreigabe zurück.</span><span class="sxs-lookup"><span data-stu-id="53a58-103">Returns a list of metrics for a storage share.</span></span>

## <span data-ttu-id="53a58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53a58-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetric [-FarmName] <String> [-Name] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="53a58-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53a58-105">DESCRIPTION</span></span>
<span data-ttu-id="53a58-106">Gibt eine Liste von Metriken für eine Speicherfreigabe zurück.</span><span class="sxs-lookup"><span data-stu-id="53a58-106">Returns a list of metrics for a storage share.</span></span>

## <span data-ttu-id="53a58-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53a58-107">EXAMPLES</span></span>

### <span data-ttu-id="53a58-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="53a58-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageShareMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Name "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="53a58-109">Rufen Sie die Liste der Metriken für eine Speicherfreigabe ab.</span><span class="sxs-lookup"><span data-stu-id="53a58-109">Get the list of metrics for a storage share.</span></span>

## <span data-ttu-id="53a58-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="53a58-110">PARAMETERS</span></span>

### <span data-ttu-id="53a58-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="53a58-111">-FarmName</span></span>
<span data-ttu-id="53a58-112">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="53a58-112">Farm Id.</span></span>

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

### <span data-ttu-id="53a58-113">-Name</span><span class="sxs-lookup"><span data-stu-id="53a58-113">-Name</span></span>
<span data-ttu-id="53a58-114">Freigabename.</span><span class="sxs-lookup"><span data-stu-id="53a58-114">Share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a58-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53a58-115">-ResourceGroupName</span></span>
<span data-ttu-id="53a58-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="53a58-116">Resource group name.</span></span>

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

### <span data-ttu-id="53a58-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="53a58-117">-Skip</span></span>
<span data-ttu-id="53a58-118">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="53a58-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a58-119">-Top</span><span class="sxs-lookup"><span data-stu-id="53a58-119">-Top</span></span>
<span data-ttu-id="53a58-120">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="53a58-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="53a58-121">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="53a58-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a58-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a58-122">CommonParameters</span></span>
<span data-ttu-id="53a58-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53a58-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a58-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53a58-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a58-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53a58-125">INPUTS</span></span>

## <span data-ttu-id="53a58-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53a58-126">OUTPUTS</span></span>

### <span data-ttu-id="53a58-127">Microsoft. AzureStack. Management. Storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="53a58-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="53a58-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="53a58-128">NOTES</span></span>

## <span data-ttu-id="53a58-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53a58-129">RELATED LINKS</span></span>

