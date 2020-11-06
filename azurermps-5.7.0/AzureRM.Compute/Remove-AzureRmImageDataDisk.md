---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
ms.openlocfilehash: 4115cabbeeb2a7c458ce52e80eb251cb972491f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478582"
---
# <span data-ttu-id="4180b-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="4180b-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="4180b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4180b-102">SYNOPSIS</span></span>
<span data-ttu-id="4180b-103">Entfernt einen Datenträger aus einem Image-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4180b-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4180b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4180b-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <Image> [-Lun] <Int32> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4180b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4180b-105">DESCRIPTION</span></span>
<span data-ttu-id="4180b-106">Das Cmdlet **Remove-AzureRmImageDataDisk** entfernt einen Datenträger aus einem Image-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4180b-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="4180b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4180b-107">EXAMPLES</span></span>

### <span data-ttu-id="4180b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4180b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="4180b-109">Mit diesem Befehl wird der Datenträger der logischen Einheit 1 aus dem vorhandenen Bild ' Image01 ' in der Ressourcengruppe ' ResourceGroup01 ' entfernt.</span><span class="sxs-lookup"><span data-stu-id="4180b-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4180b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4180b-110">PARAMETERS</span></span>

### <span data-ttu-id="4180b-111">-Bild</span><span class="sxs-lookup"><span data-stu-id="4180b-111">-Image</span></span>
<span data-ttu-id="4180b-112">Gibt ein lokales Image-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4180b-112">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4180b-113">-LUN</span><span class="sxs-lookup"><span data-stu-id="4180b-113">-Lun</span></span>
<span data-ttu-id="4180b-114">Gibt die logische Einheitsnummer an (LUN).</span><span class="sxs-lookup"><span data-stu-id="4180b-114">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4180b-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4180b-115">-Confirm</span></span>
<span data-ttu-id="4180b-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4180b-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4180b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4180b-117">-WhatIf</span></span>
<span data-ttu-id="4180b-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4180b-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4180b-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4180b-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4180b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4180b-120">CommonParameters</span></span>
<span data-ttu-id="4180b-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4180b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4180b-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4180b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4180b-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4180b-123">INPUTS</span></span>

### <span data-ttu-id="4180b-124">Microsoft. Azure. Management. Compute. Models. Image</span><span class="sxs-lookup"><span data-stu-id="4180b-124">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="4180b-125">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4180b-125">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4180b-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4180b-126">OUTPUTS</span></span>

### <span data-ttu-id="4180b-127">Microsoft. Azure. Management. Compute. Models. Image</span><span class="sxs-lookup"><span data-stu-id="4180b-127">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="4180b-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="4180b-128">NOTES</span></span>

## <span data-ttu-id="4180b-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4180b-129">RELATED LINKS</span></span>

