---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09391f521a2b75663b25731c6cc20ef78a658d5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661892"
---
# <span data-ttu-id="65274-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="65274-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="65274-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65274-102">SYNOPSIS</span></span>
<span data-ttu-id="65274-103">Skalieren einer Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="65274-103">Scale out a scale unit.</span></span>

## <span data-ttu-id="65274-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65274-104">SYNTAX</span></span>

```
Add-AzsScaleUnitNode [-NodeList] <ScaleOutScaleUnitParameters[]> [[-ResourceGroupName] <String>]
 [-ScaleUnit] <String> [[-Location] <String>] [-AwaitStorageConvergence] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="65274-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65274-105">DESCRIPTION</span></span>
<span data-ttu-id="65274-106">Fügen Sie einen neuen Skalierungseinheiten Knoten zu Ihrem Skalierungseinheiten Cluster hinzu.</span><span class="sxs-lookup"><span data-stu-id="65274-106">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="65274-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65274-107">EXAMPLES</span></span>

### <span data-ttu-id="65274-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="65274-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName
```

<span data-ttu-id="65274-109">Fügt der Skalierungseinheit eine Liste von Knoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="65274-109">Adds a list of nodes to the scale unit.</span></span>

## <span data-ttu-id="65274-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="65274-110">PARAMETERS</span></span>

### <span data-ttu-id="65274-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65274-111">-AsJob</span></span>
<span data-ttu-id="65274-112">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="65274-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65274-113">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="65274-113">-AwaitStorageConvergence</span></span>
<span data-ttu-id="65274-114">Warten Sie, bis die Speicherreplikation abgeschlossen ist, bevor Sie erfolgreich zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="65274-114">Wait for storage replication to complete before returning success.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65274-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="65274-115">-Location</span></span>
<span data-ttu-id="65274-116">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="65274-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65274-117">-Nodeliste</span><span class="sxs-lookup"><span data-stu-id="65274-117">-NodeList</span></span>
<span data-ttu-id="65274-118">Eine Liste mit Eingabedaten, die das Hinzufügen einer Gruppe von Skalierungseinheiten Knoten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="65274-118">A list of input data that allows for adding a set of scale unit nodes.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65274-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65274-119">-ResourceGroupName</span></span>
<span data-ttu-id="65274-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="65274-120">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65274-121">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="65274-121">-ScaleUnit</span></span>
<span data-ttu-id="65274-122">Name der Skalierungseinheiten</span><span class="sxs-lookup"><span data-stu-id="65274-122">Name of the scale units.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65274-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65274-123">CommonParameters</span></span>
<span data-ttu-id="65274-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65274-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65274-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65274-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65274-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65274-126">INPUTS</span></span>

## <span data-ttu-id="65274-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65274-127">OUTPUTS</span></span>

## <span data-ttu-id="65274-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="65274-128">NOTES</span></span>

## <span data-ttu-id="65274-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65274-129">RELATED LINKS</span></span>

