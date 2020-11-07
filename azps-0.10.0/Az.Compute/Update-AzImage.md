---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: 1a04ca9df307b8d6251c6a8378df86827a76d001
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842444"
---
# <span data-ttu-id="eabb1-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="eabb1-101">Update-AzImage</span></span>

## <span data-ttu-id="eabb1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eabb1-102">SYNOPSIS</span></span>
<span data-ttu-id="eabb1-103">Aktualisiert ein Bild.</span><span class="sxs-lookup"><span data-stu-id="eabb1-103">Updates an image.</span></span>

## <span data-ttu-id="eabb1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eabb1-104">SYNTAX</span></span>

```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eabb1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eabb1-105">DESCRIPTION</span></span>
<span data-ttu-id="eabb1-106">Das Cmdlet **Update-AzImage** aktualisiert ein Bild.</span><span class="sxs-lookup"><span data-stu-id="eabb1-106">The **Update-AzImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="eabb1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eabb1-107">EXAMPLES</span></span>

### <span data-ttu-id="eabb1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eabb1-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="eabb1-109">Mit diesem Befehl wird der Datenträger der logischen Einheit 1 aus dem vorhandenen Bild ' Image01 ' in der Ressourcengruppe ' ResourceGroup01 ' entfernt.</span><span class="sxs-lookup"><span data-stu-id="eabb1-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="eabb1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="eabb1-110">PARAMETERS</span></span>

### <span data-ttu-id="eabb1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eabb1-111">-AsJob</span></span>
<span data-ttu-id="eabb1-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="eabb1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eabb1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eabb1-113">-DefaultProfile</span></span>
<span data-ttu-id="eabb1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eabb1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eabb1-115">-Bild</span><span class="sxs-lookup"><span data-stu-id="eabb1-115">-Image</span></span>
<span data-ttu-id="eabb1-116">Gibt ein lokales Image-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="eabb1-116">Specifies a local image object.</span></span>

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

### <span data-ttu-id="eabb1-117">-Bildname</span><span class="sxs-lookup"><span data-stu-id="eabb1-117">-ImageName</span></span>
<span data-ttu-id="eabb1-118">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="eabb1-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="eabb1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eabb1-119">-ResourceGroupName</span></span>
<span data-ttu-id="eabb1-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="eabb1-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="eabb1-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eabb1-121">-Confirm</span></span>
<span data-ttu-id="eabb1-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eabb1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eabb1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eabb1-123">-WhatIf</span></span>
<span data-ttu-id="eabb1-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eabb1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eabb1-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eabb1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eabb1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eabb1-126">CommonParameters</span></span>
<span data-ttu-id="eabb1-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eabb1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eabb1-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eabb1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eabb1-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eabb1-129">INPUTS</span></span>

### <span data-ttu-id="eabb1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="eabb1-130">System.String</span></span>
<span data-ttu-id="eabb1-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="eabb1-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="eabb1-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eabb1-132">OUTPUTS</span></span>

### <span data-ttu-id="eabb1-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="eabb1-133">System.Object</span></span>

## <span data-ttu-id="eabb1-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="eabb1-134">NOTES</span></span>

## <span data-ttu-id="eabb1-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eabb1-135">RELATED LINKS</span></span>

