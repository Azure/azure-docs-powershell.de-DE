---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 20399a1b62062afa5585e78a9fdb229ad3781d33
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009322"
---
# <span data-ttu-id="aaa50-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="aaa50-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="aaa50-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aaa50-102">SYNOPSIS</span></span>
<span data-ttu-id="aaa50-103">Entfernt einen Datenträger aus einem Image-Objekt.</span><span class="sxs-lookup"><span data-stu-id="aaa50-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="aaa50-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aaa50-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaa50-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aaa50-105">DESCRIPTION</span></span>
<span data-ttu-id="aaa50-106">Das Cmdlet **Remove-AzImageDataDisk** entfernt einen Datenträger aus einem Image-Objekt.</span><span class="sxs-lookup"><span data-stu-id="aaa50-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="aaa50-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aaa50-107">EXAMPLES</span></span>

### <span data-ttu-id="aaa50-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aaa50-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="aaa50-109">Mit diesem Befehl wird der Datenträger der logischen Einheit 1 aus dem vorhandenen Bild ' Image01 ' in der Ressourcengruppe ' ResourceGroup01 ' entfernt.</span><span class="sxs-lookup"><span data-stu-id="aaa50-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="aaa50-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="aaa50-110">PARAMETERS</span></span>

### <span data-ttu-id="aaa50-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaa50-111">-DefaultProfile</span></span>
<span data-ttu-id="aaa50-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aaa50-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aaa50-113">-Bild</span><span class="sxs-lookup"><span data-stu-id="aaa50-113">-Image</span></span>
<span data-ttu-id="aaa50-114">Gibt ein lokales Image-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="aaa50-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="aaa50-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="aaa50-115">-Lun</span></span>
<span data-ttu-id="aaa50-116">Gibt die logische Einheitsnummer an (LUN).</span><span class="sxs-lookup"><span data-stu-id="aaa50-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="aaa50-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aaa50-117">-Confirm</span></span>
<span data-ttu-id="aaa50-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aaa50-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaa50-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaa50-119">-WhatIf</span></span>
<span data-ttu-id="aaa50-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aaa50-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aaa50-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aaa50-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaa50-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa50-122">CommonParameters</span></span>
<span data-ttu-id="aaa50-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaa50-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa50-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aaa50-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa50-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aaa50-125">INPUTS</span></span>

### <span data-ttu-id="aaa50-126">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="aaa50-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="aaa50-127">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="aaa50-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="aaa50-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aaa50-128">OUTPUTS</span></span>

### <span data-ttu-id="aaa50-129">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="aaa50-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="aaa50-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="aaa50-130">NOTES</span></span>

## <span data-ttu-id="aaa50-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aaa50-131">RELATED LINKS</span></span>
