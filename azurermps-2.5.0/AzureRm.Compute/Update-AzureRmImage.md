---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermimage
schema: 2.0.0
ms.openlocfilehash: f1309453384f028c51bea20703d6ec75cc8a3a36
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850864"
---
# <span data-ttu-id="f402c-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="f402c-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="f402c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f402c-102">SYNOPSIS</span></span>
<span data-ttu-id="f402c-103">Aktualisiert ein Bild.</span><span class="sxs-lookup"><span data-stu-id="f402c-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f402c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f402c-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f402c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f402c-105">DESCRIPTION</span></span>
<span data-ttu-id="f402c-106">Das Cmdlet **Update-AzureRmImage** aktualisiert ein Bild.</span><span class="sxs-lookup"><span data-stu-id="f402c-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="f402c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f402c-107">EXAMPLES</span></span>

### <span data-ttu-id="f402c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f402c-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="f402c-109">Mit diesem Befehl wird der Datenträger der logischen Einheit 1 aus dem vorhandenen Bild ' Image01 ' in der Ressourcengruppe ' ResourceGroup01 ' entfernt.</span><span class="sxs-lookup"><span data-stu-id="f402c-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f402c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f402c-110">PARAMETERS</span></span>

### <span data-ttu-id="f402c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f402c-111">-AsJob</span></span>
<span data-ttu-id="f402c-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f402c-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f402c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f402c-113">-DefaultProfile</span></span>
<span data-ttu-id="f402c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f402c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f402c-115">-Bild</span><span class="sxs-lookup"><span data-stu-id="f402c-115">-Image</span></span>
<span data-ttu-id="f402c-116">Gibt ein lokales Image-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f402c-116">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f402c-117">-Bildname</span><span class="sxs-lookup"><span data-stu-id="f402c-117">-ImageName</span></span>
<span data-ttu-id="f402c-118">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="f402c-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="f402c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f402c-119">-ResourceGroupName</span></span>
<span data-ttu-id="f402c-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f402c-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f402c-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f402c-121">-Confirm</span></span>
<span data-ttu-id="f402c-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f402c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f402c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f402c-123">-WhatIf</span></span>
<span data-ttu-id="f402c-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f402c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f402c-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f402c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f402c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f402c-126">CommonParameters</span></span>
<span data-ttu-id="f402c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f402c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f402c-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f402c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f402c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f402c-129">INPUTS</span></span>

### <span data-ttu-id="f402c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f402c-130">System.String</span></span>
<span data-ttu-id="f402c-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="f402c-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="f402c-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f402c-132">OUTPUTS</span></span>

### <span data-ttu-id="f402c-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="f402c-133">System.Object</span></span>

## <span data-ttu-id="f402c-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="f402c-134">NOTES</span></span>

## <span data-ttu-id="f402c-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f402c-135">RELATED LINKS</span></span>

