---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdfb3714bbabcacd2805dc4198e2cfffde3f0e8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826155"
---
# <span data-ttu-id="a6bf9-101">New-AzsDataDiskObject</span><span class="sxs-lookup"><span data-stu-id="a6bf9-101">New-AzsDataDiskObject</span></span>

## <span data-ttu-id="a6bf9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a6bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="a6bf9-103">Erstellt einen Daten Datenträger, der zum Erstellen eines neuen Platt Form Bilds für eine virtuelle Maschine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a6bf9-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="a6bf9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6bf9-104">SYNTAX</span></span>

```
New-AzsDataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="a6bf9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6bf9-105">DESCRIPTION</span></span>
<span data-ttu-id="a6bf9-106">Erstellt ein Objekt, das Informationen zu einem Datenträger aufhält.</span><span class="sxs-lookup"><span data-stu-id="a6bf9-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="a6bf9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6bf9-107">EXAMPLES</span></span>

### <span data-ttu-id="a6bf9-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a6bf9-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="a6bf9-109">Erstellen Sie ein neues Datenträgerobjekt.</span><span class="sxs-lookup"><span data-stu-id="a6bf9-109">Create a new data disk object.</span></span>

## <span data-ttu-id="a6bf9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6bf9-110">PARAMETERS</span></span>

### <span data-ttu-id="a6bf9-111">-LUN</span><span class="sxs-lookup"><span data-stu-id="a6bf9-111">-Lun</span></span>
<span data-ttu-id="a6bf9-112">Logische Einheitsnummer.</span><span class="sxs-lookup"><span data-stu-id="a6bf9-112">Logical unit number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6bf9-113">-URI</span><span class="sxs-lookup"><span data-stu-id="a6bf9-113">-Uri</span></span>
<span data-ttu-id="a6bf9-114">Speicherort der Datenträger Vorlage</span><span class="sxs-lookup"><span data-stu-id="a6bf9-114">Location of the disk template.</span></span>

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

### <span data-ttu-id="a6bf9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6bf9-115">CommonParameters</span></span>
<span data-ttu-id="a6bf9-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6bf9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6bf9-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6bf9-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6bf9-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a6bf9-118">INPUTS</span></span>

## <span data-ttu-id="a6bf9-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a6bf9-119">OUTPUTS</span></span>

## <span data-ttu-id="a6bf9-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="a6bf9-120">NOTES</span></span>

## <span data-ttu-id="a6bf9-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a6bf9-121">RELATED LINKS</span></span>

