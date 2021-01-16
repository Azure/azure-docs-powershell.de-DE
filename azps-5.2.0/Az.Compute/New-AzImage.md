---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
ms.openlocfilehash: ff291afae70636863dff8ce34b5610cd77ce1251
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289745"
---
# <span data-ttu-id="1e4b9-101">New-AzImage</span><span class="sxs-lookup"><span data-stu-id="1e4b9-101">New-AzImage</span></span>

## <span data-ttu-id="1e4b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e4b9-102">SYNOPSIS</span></span>
<span data-ttu-id="1e4b9-103">Erstellt ein Bild.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-103">Creates an image.</span></span>

## <span data-ttu-id="1e4b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e4b9-104">SYNTAX</span></span>

```
New-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e4b9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e4b9-105">DESCRIPTION</span></span>
<span data-ttu-id="1e4b9-106">Das **Cmdlet "New-AzImage"** erstellt ein Bild.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-106">The **New-AzImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="1e4b9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1e4b9-107">EXAMPLES</span></span>

### <span data-ttu-id="1e4b9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1e4b9-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="1e4b9-109">Der erste Befehl erstellt ein Bildobjekt und speichert es dann in der $imageConfig Variable.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="1e4b9-110">Mit den nächsten drei Befehlen werden den Variablen $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 Pfade des Betriebssystemdatenträgers zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="1e4b9-111">Dieser Ansatz ist nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="1e4b9-112">Mit den nächsten drei Befehlen werden dem in der Datei gespeicherten Bild jeweils ein Betriebssystemdatenträger und zwei Datenträger $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="1e4b9-113">Der URI der einzelnen Datenträger wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="1e4b9-114">Der letzte Befehl erstellt ein Bild mit dem Namen 'ImageName01' in der Ressourcengruppe 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="1e4b9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e4b9-115">PARAMETERS</span></span>

### <span data-ttu-id="1e4b9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e4b9-116">-AsJob</span></span>
<span data-ttu-id="1e4b9-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1e4b9-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4b9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e4b9-118">-DefaultProfile</span></span>
<span data-ttu-id="1e4b9-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e4b9-120">-Image</span><span class="sxs-lookup"><span data-stu-id="1e4b9-120">-Image</span></span>
<span data-ttu-id="1e4b9-121">Gibt ein lokales Bildobjekt an.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-121">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e4b9-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="1e4b9-122">-ImageName</span></span>
<span data-ttu-id="1e4b9-123">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-123">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e4b9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e4b9-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e4b9-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e4b9-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e4b9-126">-Confirm</span></span>
<span data-ttu-id="1e4b9-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e4b9-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1e4b9-128">-WhatIf</span></span>
<span data-ttu-id="1e4b9-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e4b9-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e4b9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e4b9-131">CommonParameters</span></span>
<span data-ttu-id="1e4b9-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e4b9-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e4b9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e4b9-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1e4b9-134">INPUTS</span></span>

### <span data-ttu-id="1e4b9-135">System.String</span><span class="sxs-lookup"><span data-stu-id="1e4b9-135">System.String</span></span>

### <span data-ttu-id="1e4b9-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="1e4b9-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="1e4b9-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1e4b9-137">OUTPUTS</span></span>

### <span data-ttu-id="1e4b9-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="1e4b9-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="1e4b9-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1e4b9-139">NOTES</span></span>

## <span data-ttu-id="1e4b9-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1e4b9-140">RELATED LINKS</span></span>
