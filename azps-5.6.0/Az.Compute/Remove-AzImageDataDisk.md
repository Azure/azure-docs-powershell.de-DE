---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 77f01dc2161188660ecdc46086e6c53a29e520f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934264"
---
# <span data-ttu-id="357f4-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="357f4-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="357f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="357f4-102">SYNOPSIS</span></span>
<span data-ttu-id="357f4-103">Entfernt einen Datenträger aus einem Bildobjekt.</span><span class="sxs-lookup"><span data-stu-id="357f4-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="357f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="357f4-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="357f4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="357f4-105">DESCRIPTION</span></span>
<span data-ttu-id="357f4-106">Das **Cmdlet Remove-AzImageDataDisk** entfernt einen Datenträger aus einem Bildobjekt.</span><span class="sxs-lookup"><span data-stu-id="357f4-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="357f4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="357f4-107">EXAMPLES</span></span>

### <span data-ttu-id="357f4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="357f4-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="357f4-109">Mit diesem Befehl wird der Datenträger der logischen Einheit 1 aus dem vorhandenen Bild "Image01" in der Ressourcengruppe "ResourceGroup01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="357f4-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="357f4-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="357f4-110">PARAMETERS</span></span>

### <span data-ttu-id="357f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="357f4-111">-DefaultProfile</span></span>
<span data-ttu-id="357f4-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="357f4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="357f4-113">-Image</span><span class="sxs-lookup"><span data-stu-id="357f4-113">-Image</span></span>
<span data-ttu-id="357f4-114">Gibt ein lokales Bildobjekt an.</span><span class="sxs-lookup"><span data-stu-id="357f4-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="357f4-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="357f4-115">-Lun</span></span>
<span data-ttu-id="357f4-116">Gibt die Logische Einheitennummer (LUN) an.</span><span class="sxs-lookup"><span data-stu-id="357f4-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="357f4-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="357f4-117">-Confirm</span></span>
<span data-ttu-id="357f4-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="357f4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="357f4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="357f4-119">-WhatIf</span></span>
<span data-ttu-id="357f4-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="357f4-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="357f4-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="357f4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="357f4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="357f4-122">CommonParameters</span></span>
<span data-ttu-id="357f4-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="357f4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="357f4-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="357f4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="357f4-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="357f4-125">INPUTS</span></span>

### <span data-ttu-id="357f4-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="357f4-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="357f4-127">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="357f4-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="357f4-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="357f4-128">OUTPUTS</span></span>

### <span data-ttu-id="357f4-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="357f4-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="357f4-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="357f4-130">NOTES</span></span>

## <span data-ttu-id="357f4-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="357f4-131">RELATED LINKS</span></span>
