---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: ACBE32E5-AA8C-43CA-9FF4-4B59906C6B85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 45d18179fba41d39456a11575fc2041ad4be8557
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006736"
---
# <span data-ttu-id="50ca0-101">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="50ca0-101">Get-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="50ca0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="50ca0-102">SYNOPSIS</span></span>
<span data-ttu-id="50ca0-103">Ruft ein Festplatten-Konfigurationssatz Objekt aus dem Kontext des Eingabebilds ab.</span><span class="sxs-lookup"><span data-stu-id="50ca0-103">Gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="50ca0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="50ca0-104">SYNTAX</span></span>

```
Get-AzureVMImageDiskConfigSet [[-ImageContext] <OSImageContext>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="50ca0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50ca0-105">DESCRIPTION</span></span>
<span data-ttu-id="50ca0-106">Das Cmdlet " **Get-AzureVMImageDiskConfigSet** " Ruft ein Festplatten-Konfigurationssatz Objekt aus dem Kontext des Eingabebilds ab.</span><span class="sxs-lookup"><span data-stu-id="50ca0-106">The **Get-AzureVMImageDiskConfigSet** cmdlet gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="50ca0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50ca0-107">EXAMPLES</span></span>

### <span data-ttu-id="50ca0-108">Beispiel 1: Abrufen eines Festplatten-Konfigurationssatz Objekts von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="50ca0-108">Example 1: Get a disk configuration set object from a virtual machine</span></span>
```
PS C:\> Get-AzureVMImage -ImageName $Img | Get-AzureVMImageDiskConfigSet
```

<span data-ttu-id="50ca0-109">Dieser Befehl ruft ein Festplatten-Konfigurationssatz Objekt von einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="50ca0-109">This command gets a disk configuration set object from a virtual machine.</span></span>

## <span data-ttu-id="50ca0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="50ca0-110">PARAMETERS</span></span>

### <span data-ttu-id="50ca0-111">-Imagecontext</span><span class="sxs-lookup"><span data-stu-id="50ca0-111">-ImageContext</span></span>
<span data-ttu-id="50ca0-112">Gibt den Bildkontext des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="50ca0-112">Specifies the virtual machine image context.</span></span>

```yaml
Type: OSImageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50ca0-113">-Information</span><span class="sxs-lookup"><span data-stu-id="50ca0-113">-InformationAction</span></span>
<span data-ttu-id="50ca0-114">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="50ca0-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="50ca0-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="50ca0-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="50ca0-116">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="50ca0-116">Continue</span></span>
- <span data-ttu-id="50ca0-117">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="50ca0-117">Ignore</span></span>
- <span data-ttu-id="50ca0-118">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="50ca0-118">Inquire</span></span>
- <span data-ttu-id="50ca0-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="50ca0-119">SilentlyContinue</span></span>
- <span data-ttu-id="50ca0-120">Beenden</span><span class="sxs-lookup"><span data-stu-id="50ca0-120">Stop</span></span>
- <span data-ttu-id="50ca0-121">Anhalten</span><span class="sxs-lookup"><span data-stu-id="50ca0-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50ca0-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="50ca0-122">-InformationVariable</span></span>
<span data-ttu-id="50ca0-123">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="50ca0-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50ca0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50ca0-124">CommonParameters</span></span>
<span data-ttu-id="50ca0-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50ca0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50ca0-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50ca0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50ca0-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="50ca0-127">INPUTS</span></span>

## <span data-ttu-id="50ca0-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="50ca0-128">OUTPUTS</span></span>

### <span data-ttu-id="50ca0-129">Microsoft. WindowsAzure. Commands. Servicemanagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="50ca0-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="50ca0-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="50ca0-130">NOTES</span></span>

## <span data-ttu-id="50ca0-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="50ca0-131">RELATED LINKS</span></span>

[<span data-ttu-id="50ca0-132">Neu – AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="50ca0-132">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="50ca0-133">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="50ca0-133">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)


