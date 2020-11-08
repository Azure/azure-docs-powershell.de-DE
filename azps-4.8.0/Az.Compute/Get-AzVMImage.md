---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 350e03d6e238eb0cf1aa6b27da6b9a321603a664
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008339"
---
# <span data-ttu-id="755d8-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="755d8-101">Get-AzVMImage</span></span>

## <span data-ttu-id="755d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="755d8-102">SYNOPSIS</span></span>
<span data-ttu-id="755d8-103">Ruft alle Versionen eines VMImage ab.</span><span class="sxs-lookup"><span data-stu-id="755d8-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="755d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="755d8-104">SYNTAX</span></span>

### <span data-ttu-id="755d8-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="755d8-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> [-Top <Int32>]
 [-OrderBy <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="755d8-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="755d8-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="755d8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="755d8-107">DESCRIPTION</span></span>
<span data-ttu-id="755d8-108">Das Cmdlet " **Get-AzVMImage** " ruft alle Versionen eines VMImage ab.</span><span class="sxs-lookup"><span data-stu-id="755d8-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="755d8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="755d8-109">EXAMPLES</span></span>

### <span data-ttu-id="755d8-110">Beispiel 1: Abrufen von VMImage-Objekten</span><span class="sxs-lookup"><span data-stu-id="755d8-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190104                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190115                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190204                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190218                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="755d8-111">Dieser Befehl ruft alle Versionen von VMImage ab, die den angegebenen Werten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="755d8-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="755d8-112">Beispiel 2: Abrufen des VMImage-Objekts</span><span class="sxs-lookup"><span data-stu-id="755d8-112">Example 2: Get VMImage object</span></span>
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
FilterExpression :
Name             : 4.127.20180315
OSDiskImage      : {
                     "operatingSystem": "Windows"
                   }
PurchasePlan     : null
DataDiskImages   : []
```

<span data-ttu-id="755d8-113">Dieser Befehl ruft eine bestimmte Version von VMImage ab, die den angegebenen Werten entspricht.</span><span class="sxs-lookup"><span data-stu-id="755d8-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="755d8-114">Beispiel 3: Abrufen von VMImage-Objekten</span><span class="sxs-lookup"><span data-stu-id="755d8-114">Example 3: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.2018*

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="755d8-115">Dieser Befehl ruft alle Versionen von VMImage ab, die den angegebenen Werten entsprechen, und filtert über Version.</span><span class="sxs-lookup"><span data-stu-id="755d8-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="755d8-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="755d8-116">PARAMETERS</span></span>

### <span data-ttu-id="755d8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="755d8-117">-DefaultProfile</span></span>
<span data-ttu-id="755d8-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="755d8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="755d8-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="755d8-119">-Location</span></span>
<span data-ttu-id="755d8-120">Gibt die Position eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="755d8-120">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="755d8-121">-Angebot</span><span class="sxs-lookup"><span data-stu-id="755d8-121">-Offer</span></span>
<span data-ttu-id="755d8-122">Gibt den Typ des VMImage-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="755d8-122">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="755d8-123">Verwenden Sie das Get-AzVMImageOffer-Cmdlet, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="755d8-123">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="755d8-124">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="755d8-124">-OrderBy</span></span>
<span data-ttu-id="755d8-125">Gibt die Reihenfolge der zurückgegebenen Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="755d8-125">Specifies the order of the results returned.</span></span> <span data-ttu-id="755d8-126">Als OData-Abfrage formatiert.</span><span class="sxs-lookup"><span data-stu-id="755d8-126">Formatted as an OData query.</span></span>

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

### <span data-ttu-id="755d8-127">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="755d8-127">-PublisherName</span></span>
<span data-ttu-id="755d8-128">Gibt den Herausgeber eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="755d8-128">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="755d8-129">Verwenden Sie das Get-AzVMImagePublisher-Cmdlet, um einen Bildherausgeber zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="755d8-129">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="755d8-130">-SKUs</span><span class="sxs-lookup"><span data-stu-id="755d8-130">-Skus</span></span>
<span data-ttu-id="755d8-131">Gibt eine VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="755d8-131">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="755d8-132">Verwenden Sie das Get-AzVMImageSku-Cmdlet, um eine SKU zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="755d8-132">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="755d8-133">-Top</span><span class="sxs-lookup"><span data-stu-id="755d8-133">-Top</span></span>
<span data-ttu-id="755d8-134">Gibt die maximale Anzahl der zurückgegebenen virtuellen Computer Bilder an.</span><span class="sxs-lookup"><span data-stu-id="755d8-134">Specifies the maximum number of virtual machine images returned.</span></span> 

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

### <span data-ttu-id="755d8-135">-Version</span><span class="sxs-lookup"><span data-stu-id="755d8-135">-Version</span></span>
<span data-ttu-id="755d8-136">Gibt die Version von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="755d8-136">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="755d8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755d8-137">CommonParameters</span></span>
<span data-ttu-id="755d8-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="755d8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755d8-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="755d8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755d8-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="755d8-140">INPUTS</span></span>

### <span data-ttu-id="755d8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="755d8-141">System.String</span></span>

## <span data-ttu-id="755d8-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="755d8-142">OUTPUTS</span></span>

### <span data-ttu-id="755d8-143">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="755d8-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="755d8-144">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="755d8-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="755d8-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="755d8-145">NOTES</span></span>

## <span data-ttu-id="755d8-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="755d8-146">RELATED LINKS</span></span>

[<span data-ttu-id="755d8-147">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="755d8-147">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="755d8-148">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="755d8-148">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="755d8-149">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="755d8-149">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="755d8-150">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="755d8-150">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


