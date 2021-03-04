---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 0075b057cecb91b618d06ad36788801a672268aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922091"
---
# <span data-ttu-id="5564b-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="5564b-101">Get-AzVMImage</span></span>

## <span data-ttu-id="5564b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5564b-102">SYNOPSIS</span></span>
<span data-ttu-id="5564b-103">Ruft alle Versionen eines VMImage ab.</span><span class="sxs-lookup"><span data-stu-id="5564b-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="5564b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5564b-104">SYNTAX</span></span>

### <span data-ttu-id="5564b-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="5564b-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> [-Top <Int32>]
 [-OrderBy <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5564b-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="5564b-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5564b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5564b-107">DESCRIPTION</span></span>
<span data-ttu-id="5564b-108">Das **Get-AzVMImage-Cmdlet** ruft alle Versionen eines VMImage ab.</span><span class="sxs-lookup"><span data-stu-id="5564b-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="5564b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5564b-109">EXAMPLES</span></span>

### <span data-ttu-id="5564b-110">Beispiel 1: Herunterladen von VMImage-Objekten</span><span class="sxs-lookup"><span data-stu-id="5564b-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"

Version        Skus               Offer         PublisherName          Location  Id
-------        ----               -----         -------------          --------  --
4.127.20180315 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190104 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190115 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190204 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190218 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="5564b-111">Dieser Befehl ruft alle Versionen von VMImage ab, die den angegebenen Werten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5564b-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="5564b-112">Beispiel 2: VmImage-Objekt herunterladen</span><span class="sxs-lookup"><span data-stu-id="5564b-112">Example 2: Get VMImage object</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.20180315

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/centralus/
                   Publishers/MicrosoftWindowsServer/ArtifactTypes/VMImage/Offers/windowsserver/Skus/2012-R2-Datacenter
                   /Versions/4.127.20180315
Location         : centralus
PublisherName    : MicrosoftWindowsServer
Offer            : windowsserver
Skus             : 2012-R2-Datacenter
Version          : 4.127.20180315
Name             : 4.127.20180315
OSDiskImage      : {
                     "operatingSystem": "Windows"
                   }
PurchasePlan     : null
DataDiskImages   : []
```

<span data-ttu-id="5564b-113">Dieser Befehl ruft eine bestimmte Version von VMImage ab, die den angegebenen Werten entspricht.</span><span class="sxs-lookup"><span data-stu-id="5564b-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="5564b-114">Beispiel 3: Herunterladen von VMImage-Objekten</span><span class="sxs-lookup"><span data-stu-id="5564b-114">Example 3: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.2018*

Version        Skus               Offer         PublisherName          Location  Id
-------        ----               -----         -------------          --------  --
4.127.20180315 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="5564b-115">Dieser Befehl ruft alle Versionen von VMImage ab, die den angegebenen Werten entsprechen, und filtert über die Version.</span><span class="sxs-lookup"><span data-stu-id="5564b-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="5564b-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5564b-116">PARAMETERS</span></span>

### <span data-ttu-id="5564b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5564b-117">-DefaultProfile</span></span>
<span data-ttu-id="5564b-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5564b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5564b-119">-Location</span><span class="sxs-lookup"><span data-stu-id="5564b-119">-Location</span></span>
<span data-ttu-id="5564b-120">Gibt den Speicherort eines VMImages an.</span><span class="sxs-lookup"><span data-stu-id="5564b-120">Specifies the location of a VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5564b-121">-Angebot</span><span class="sxs-lookup"><span data-stu-id="5564b-121">-Offer</span></span>
<span data-ttu-id="5564b-122">Gibt den Typ des VMImage-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="5564b-122">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="5564b-123">Verwenden Sie das cmdlet Get-AzVMImageOffer, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5564b-123">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5564b-124">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="5564b-124">-OrderBy</span></span>
<span data-ttu-id="5564b-125">Gibt die Reihenfolge der zurückgegebenen Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="5564b-125">Specifies the order of the results returned.</span></span> <span data-ttu-id="5564b-126">Als OData-Abfrage formatiert.</span><span class="sxs-lookup"><span data-stu-id="5564b-126">Formatted as an OData query.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5564b-127">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="5564b-127">-PublisherName</span></span>
<span data-ttu-id="5564b-128">Gibt den Herausgeber eines VMImages an.</span><span class="sxs-lookup"><span data-stu-id="5564b-128">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="5564b-129">Verwenden Sie das cmdlet Get-AzVMImagePublisher, um einen Bildherausgeber zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5564b-129">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5564b-130">-Skus</span><span class="sxs-lookup"><span data-stu-id="5564b-130">-Skus</span></span>
<span data-ttu-id="5564b-131">Gibt eine VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="5564b-131">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="5564b-132">Verwenden Sie zum Abrufen einer SKU das Get-AzVMImageSku Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5564b-132">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5564b-133">-Top</span><span class="sxs-lookup"><span data-stu-id="5564b-133">-Top</span></span>
<span data-ttu-id="5564b-134">Gibt die maximale Anzahl der zurückgegebenen Virtuellen Computerbilder an.</span><span class="sxs-lookup"><span data-stu-id="5564b-134">Specifies the maximum number of virtual machine images returned.</span></span> 

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5564b-135">-Version</span><span class="sxs-lookup"><span data-stu-id="5564b-135">-Version</span></span>
<span data-ttu-id="5564b-136">Gibt die Version des VMImage an.</span><span class="sxs-lookup"><span data-stu-id="5564b-136">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5564b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5564b-137">CommonParameters</span></span>
<span data-ttu-id="5564b-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5564b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5564b-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5564b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5564b-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5564b-140">INPUTS</span></span>

### <span data-ttu-id="5564b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="5564b-141">System.String</span></span>

## <span data-ttu-id="5564b-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5564b-142">OUTPUTS</span></span>

### <span data-ttu-id="5564b-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="5564b-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="5564b-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="5564b-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="5564b-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5564b-145">NOTES</span></span>

## <span data-ttu-id="5564b-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5564b-146">RELATED LINKS</span></span>

[<span data-ttu-id="5564b-147">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="5564b-147">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="5564b-148">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="5564b-148">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="5564b-149">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="5564b-149">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="5564b-150">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="5564b-150">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


