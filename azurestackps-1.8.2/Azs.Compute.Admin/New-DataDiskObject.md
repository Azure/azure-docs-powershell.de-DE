---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37d41ae2ec772cc755436bc01c3c4009c9c30f5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006993"
---
# <span data-ttu-id="c345e-101">New-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="c345e-101">New-DataDiskObject</span></span>

## <span data-ttu-id="c345e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c345e-102">SYNOPSIS</span></span>
<span data-ttu-id="c345e-103">Erstellt einen Daten Datenträger, der zum Erstellen eines neuen Platt Form Bilds für eine virtuelle Maschine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c345e-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="c345e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c345e-104">SYNTAX</span></span>

```
New-DataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="c345e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c345e-105">DESCRIPTION</span></span>
<span data-ttu-id="c345e-106">Erstellt ein Objekt, das Informationen zu einem Datenträger aufhält.</span><span class="sxs-lookup"><span data-stu-id="c345e-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="c345e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c345e-107">EXAMPLES</span></span>

### <span data-ttu-id="c345e-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c345e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-DataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="c345e-109">Erstellen Sie ein neues Datenträgerobjekt.</span><span class="sxs-lookup"><span data-stu-id="c345e-109">Create a new data disk object.</span></span>

## <span data-ttu-id="c345e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c345e-110">PARAMETERS</span></span>

### <span data-ttu-id="c345e-111">-LUN</span><span class="sxs-lookup"><span data-stu-id="c345e-111">-Lun</span></span>
<span data-ttu-id="c345e-112">Logische Einheitsnummer.</span><span class="sxs-lookup"><span data-stu-id="c345e-112">Logical unit number.</span></span>

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

### <span data-ttu-id="c345e-113">-URI</span><span class="sxs-lookup"><span data-stu-id="c345e-113">-Uri</span></span>
<span data-ttu-id="c345e-114">Speicherort der Datenträger Vorlage</span><span class="sxs-lookup"><span data-stu-id="c345e-114">Location of the disk template.</span></span>

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

### <span data-ttu-id="c345e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c345e-115">CommonParameters</span></span>
<span data-ttu-id="c345e-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c345e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c345e-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c345e-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c345e-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c345e-118">INPUTS</span></span>

## <span data-ttu-id="c345e-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c345e-119">OUTPUTS</span></span>

## <span data-ttu-id="c345e-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="c345e-120">NOTES</span></span>

## <span data-ttu-id="c345e-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c345e-121">RELATED LINKS</span></span>

