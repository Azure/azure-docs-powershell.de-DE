---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
ms.openlocfilehash: 054462398a0f7b3e8710928000f9c10fb42f04db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662752"
---
# <span data-ttu-id="1ced2-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="1ced2-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="1ced2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1ced2-102">SYNOPSIS</span></span>
<span data-ttu-id="1ced2-103">Entfernt ein Bild.</span><span class="sxs-lookup"><span data-stu-id="1ced2-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ced2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ced2-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ced2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ced2-105">DESCRIPTION</span></span>
<span data-ttu-id="1ced2-106">Mit dem Cmdlet **Remove-AzureRmImage** wird ein Bild entfernt.</span><span class="sxs-lookup"><span data-stu-id="1ced2-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="1ced2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ced2-107">EXAMPLES</span></span>

### <span data-ttu-id="1ced2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1ced2-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="1ced2-109">Dieser Befehl entfernt das Bild mit dem Namen "Image01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1ced2-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="1ced2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ced2-110">PARAMETERS</span></span>

### <span data-ttu-id="1ced2-111">-Force</span><span class="sxs-lookup"><span data-stu-id="1ced2-111">-Force</span></span>
<span data-ttu-id="1ced2-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="1ced2-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ced2-113">-Bildname</span><span class="sxs-lookup"><span data-stu-id="1ced2-113">-ImageName</span></span>
<span data-ttu-id="1ced2-114">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="1ced2-114">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ced2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ced2-115">-ResourceGroupName</span></span>
<span data-ttu-id="1ced2-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1ced2-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ced2-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ced2-117">-Confirm</span></span>
<span data-ttu-id="1ced2-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ced2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ced2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ced2-119">-WhatIf</span></span>
<span data-ttu-id="1ced2-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ced2-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ced2-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ced2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ced2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ced2-122">CommonParameters</span></span>
<span data-ttu-id="1ced2-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ced2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ced2-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ced2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ced2-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ced2-125">INPUTS</span></span>

### <span data-ttu-id="1ced2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1ced2-126">System.String</span></span>

## <span data-ttu-id="1ced2-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1ced2-127">OUTPUTS</span></span>

### <span data-ttu-id="1ced2-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="1ced2-128">System.Object</span></span>

## <span data-ttu-id="1ced2-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ced2-129">NOTES</span></span>

## <span data-ttu-id="1ced2-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1ced2-130">RELATED LINKS</span></span>

