---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
ms.openlocfilehash: 1d37af16fcb84db8247ac5db495abb1f41319c6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504190"
---
# <span data-ttu-id="d556e-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="d556e-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="d556e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d556e-102">SYNOPSIS</span></span>
<span data-ttu-id="d556e-103">Entfernt einen Datenträger aus einem Image-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d556e-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d556e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d556e-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d556e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d556e-105">DESCRIPTION</span></span>
<span data-ttu-id="d556e-106">Das Cmdlet **Remove-AzureRmImageDataDisk** entfernt einen Datenträger aus einem Image-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d556e-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="d556e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d556e-107">EXAMPLES</span></span>

### <span data-ttu-id="d556e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d556e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="d556e-109">Mit diesem Befehl wird der Datenträger der logischen Einheit 1 aus dem vorhandenen Bild ' Image01 ' in der Ressourcengruppe ' ResourceGroup01 ' entfernt.</span><span class="sxs-lookup"><span data-stu-id="d556e-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d556e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d556e-110">PARAMETERS</span></span>

### <span data-ttu-id="d556e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d556e-111">-DefaultProfile</span></span>
<span data-ttu-id="d556e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d556e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d556e-113">-Bild</span><span class="sxs-lookup"><span data-stu-id="d556e-113">-Image</span></span>
<span data-ttu-id="d556e-114">Gibt ein lokales Image-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d556e-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d556e-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="d556e-115">-Lun</span></span>
<span data-ttu-id="d556e-116">Gibt die logische Einheitsnummer an (LUN).</span><span class="sxs-lookup"><span data-stu-id="d556e-116">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d556e-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d556e-117">-Confirm</span></span>
<span data-ttu-id="d556e-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d556e-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d556e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d556e-119">-WhatIf</span></span>
<span data-ttu-id="d556e-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d556e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d556e-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d556e-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d556e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d556e-122">CommonParameters</span></span>
<span data-ttu-id="d556e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d556e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d556e-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d556e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d556e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d556e-125">INPUTS</span></span>

### <span data-ttu-id="d556e-126">Microsoft. Azure. Management. Compute. Models. Image</span><span class="sxs-lookup"><span data-stu-id="d556e-126">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="d556e-127">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d556e-127">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d556e-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d556e-128">OUTPUTS</span></span>

### <span data-ttu-id="d556e-129">Microsoft. Azure. Management. Compute. Models. Image</span><span class="sxs-lookup"><span data-stu-id="d556e-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="d556e-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="d556e-130">NOTES</span></span>

## <span data-ttu-id="d556e-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d556e-131">RELATED LINKS</span></span>

