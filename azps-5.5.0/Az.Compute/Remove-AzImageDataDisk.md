---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 20399a1b62062afa5585e78a9fdb229ad3781d33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144849"
---
# <span data-ttu-id="447ac-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="447ac-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="447ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="447ac-102">SYNOPSIS</span></span>
<span data-ttu-id="447ac-103">Entfernt einen Datenträger aus einem Bildobjekt.</span><span class="sxs-lookup"><span data-stu-id="447ac-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="447ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="447ac-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="447ac-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="447ac-105">DESCRIPTION</span></span>
<span data-ttu-id="447ac-106">Das **Cmdlet "Remove-AzImageDataDisk"** entfernt einen Datenträger aus einem Bildobjekt.</span><span class="sxs-lookup"><span data-stu-id="447ac-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="447ac-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="447ac-107">EXAMPLES</span></span>

### <span data-ttu-id="447ac-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="447ac-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="447ac-109">Mit diesem Befehl wird der Datenträger der logischen Einheit 1 aus dem vorhandenen Bild "Image01" in der Ressourcengruppe "ResourceGroup01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="447ac-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="447ac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="447ac-110">PARAMETERS</span></span>

### <span data-ttu-id="447ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="447ac-111">-DefaultProfile</span></span>
<span data-ttu-id="447ac-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="447ac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="447ac-113">-Image</span><span class="sxs-lookup"><span data-stu-id="447ac-113">-Image</span></span>
<span data-ttu-id="447ac-114">Gibt ein lokales Bildobjekt an.</span><span class="sxs-lookup"><span data-stu-id="447ac-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="447ac-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="447ac-115">-Lun</span></span>
<span data-ttu-id="447ac-116">Gibt die Wahrheitsnummer der Einheit (LUN) an.</span><span class="sxs-lookup"><span data-stu-id="447ac-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="447ac-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="447ac-117">-Confirm</span></span>
<span data-ttu-id="447ac-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="447ac-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="447ac-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="447ac-119">-WhatIf</span></span>
<span data-ttu-id="447ac-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="447ac-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="447ac-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="447ac-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="447ac-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="447ac-122">CommonParameters</span></span>
<span data-ttu-id="447ac-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="447ac-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="447ac-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="447ac-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="447ac-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="447ac-125">INPUTS</span></span>

### <span data-ttu-id="447ac-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="447ac-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="447ac-127">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="447ac-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="447ac-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="447ac-128">OUTPUTS</span></span>

### <span data-ttu-id="447ac-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="447ac-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="447ac-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="447ac-130">NOTES</span></span>

## <span data-ttu-id="447ac-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="447ac-131">RELATED LINKS</span></span>
