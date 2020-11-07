---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: ccca83cdbebcf73df9059807dc5b030e4ab21736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663330"
---
# <span data-ttu-id="6f27f-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="6f27f-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="6f27f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6f27f-102">SYNOPSIS</span></span>
<span data-ttu-id="6f27f-103">Aktualisiert ein Bild.</span><span class="sxs-lookup"><span data-stu-id="6f27f-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f27f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f27f-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f27f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f27f-105">DESCRIPTION</span></span>
<span data-ttu-id="6f27f-106">Das Cmdlet **Update-AzureRmImage** aktualisiert ein Bild.</span><span class="sxs-lookup"><span data-stu-id="6f27f-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="6f27f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f27f-107">EXAMPLES</span></span>

### <span data-ttu-id="6f27f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6f27f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="6f27f-109">Mit diesem Befehl wird der Datenträger der logischen Einheit 1 aus dem vorhandenen Bild ' Image01 ' in der Ressourcengruppe ' ResourceGroup01 ' entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f27f-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6f27f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f27f-110">PARAMETERS</span></span>

### <span data-ttu-id="6f27f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f27f-111">-DefaultProfile</span></span>
<span data-ttu-id="6f27f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6f27f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f27f-113">-Bild</span><span class="sxs-lookup"><span data-stu-id="6f27f-113">-Image</span></span>
<span data-ttu-id="6f27f-114">Gibt ein lokales Image-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="6f27f-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f27f-115">-Bildname</span><span class="sxs-lookup"><span data-stu-id="6f27f-115">-ImageName</span></span>
<span data-ttu-id="6f27f-116">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="6f27f-116">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f27f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f27f-117">-ResourceGroupName</span></span>
<span data-ttu-id="6f27f-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6f27f-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f27f-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6f27f-119">-Confirm</span></span>
<span data-ttu-id="6f27f-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f27f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f27f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f27f-121">-WhatIf</span></span>
<span data-ttu-id="6f27f-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6f27f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f27f-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f27f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f27f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f27f-124">CommonParameters</span></span>
<span data-ttu-id="6f27f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f27f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f27f-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f27f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f27f-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6f27f-127">INPUTS</span></span>

### <span data-ttu-id="6f27f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6f27f-128">System.String</span></span>
<span data-ttu-id="6f27f-129">Microsoft. Azure. Management. Compute. Models. Image</span><span class="sxs-lookup"><span data-stu-id="6f27f-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="6f27f-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6f27f-130">OUTPUTS</span></span>

### <span data-ttu-id="6f27f-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="6f27f-131">System.Object</span></span>

## <span data-ttu-id="6f27f-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="6f27f-132">NOTES</span></span>

## <span data-ttu-id="6f27f-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6f27f-133">RELATED LINKS</span></span>

