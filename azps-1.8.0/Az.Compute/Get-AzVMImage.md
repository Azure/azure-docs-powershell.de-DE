---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 13871100efbe2fe62de769adcc40ee434e86eb21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820728"
---
# <span data-ttu-id="0ca2e-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="0ca2e-101">Get-AzVMImage</span></span>

## <span data-ttu-id="0ca2e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ca2e-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca2e-103">Ruft alle Versionen eines VMImage ab.</span><span class="sxs-lookup"><span data-stu-id="0ca2e-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="0ca2e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ca2e-104">SYNTAX</span></span>

### <span data-ttu-id="0ca2e-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="0ca2e-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ca2e-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="0ca2e-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ca2e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ca2e-107">DESCRIPTION</span></span>
<span data-ttu-id="0ca2e-108">Das Cmdlet " **Get-AzVMImage** " ruft alle Versionen eines VMImage ab.</span><span class="sxs-lookup"><span data-stu-id="0ca2e-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="0ca2e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ca2e-109">EXAMPLES</span></span>

### <span data-ttu-id="0ca2e-110">Beispiel 1: Abrufen von VMImage-Objekten</span><span class="sxs-lookup"><span data-stu-id="0ca2e-110">Example 1: Get VMImage objects</span></span>
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

<span data-ttu-id="0ca2e-111">Dieser Befehl ruft alle Versionen von VMImage ab, die den angegebenen Werten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0ca2e-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="0ca2e-112">Beispiel 2: Abrufen des VMImage-Objekts</span><span class="sxs-lookup"><span data-stu-id="0ca2e-112">Example 2: Get VMImage object</span></span>
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

<span data-ttu-id="0ca2e-113">Dieser Befehl ruft eine bestimmte Version von VMImage ab, die den angegebenen Werten entspricht.</span><span class="sxs-lookup"><span data-stu-id="0ca2e-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="0ca2e-114">Beispiel 3: Abrufen von VMImage-Objekten</span><span class="sxs-lookup"><span data-stu-id="0ca2e-114">Example 3: Get VMImage objects</span></span>
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

<span data-ttu-id="0ca2e-115">Dieser Befehl ruft alle Versionen von VMImage ab, die den angegebenen Werten entsprechen, und filtert über Version.</span><span class="sxs-lookup"><span data-stu-id="0ca2e-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="0ca2e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ca2e-116">PARAMETERS</span></span>

### <span data-ttu-id="0ca2e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ca2e-117">-DefaultProfile</span></span>
<span data-ttu-id="0ca2e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ca2e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ca2e-119">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="0ca2e-119">-FilterExpression</span></span>
<span data-ttu-id="0ca2e-120">Gibt einen Filterausdruck an.</span><span class="sxs-lookup"><span data-stu-id="0ca2e-120">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca2e-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="0ca2e-121">-Location</span></span>
<span data-ttu-id="0ca2e-122">Gibt die Position eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="0ca2e-122">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="0ca2e-123">-Angebot</span><span class="sxs-lookup"><span data-stu-id="0ca2e-123">-Offer</span></span>
<span data-ttu-id="0ca2e-124">Gibt den Typ des VMImage-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="0ca2e-124">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="0ca2e-125">Verwenden Sie das Get-AzVMImageOffer-Cmdlet, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ca2e-125">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="0ca2e-126">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="0ca2e-126">-PublisherName</span></span>
<span data-ttu-id="0ca2e-127">Gibt den Herausgeber eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="0ca2e-127">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="0ca2e-128">Verwenden Sie das Get-AzVMImagePublisher-Cmdlet, um einen Bildherausgeber zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ca2e-128">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="0ca2e-129">-SKUs</span><span class="sxs-lookup"><span data-stu-id="0ca2e-129">-Skus</span></span>
<span data-ttu-id="0ca2e-130">Gibt eine VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="0ca2e-130">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="0ca2e-131">Verwenden Sie das Get-AzVMImageSku-Cmdlet, um eine SKU zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ca2e-131">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="0ca2e-132">-Version</span><span class="sxs-lookup"><span data-stu-id="0ca2e-132">-Version</span></span>
<span data-ttu-id="0ca2e-133">Gibt die Version von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="0ca2e-133">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0ca2e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ca2e-134">CommonParameters</span></span>
<span data-ttu-id="0ca2e-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ca2e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ca2e-136">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ca2e-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ca2e-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ca2e-137">INPUTS</span></span>

### <span data-ttu-id="0ca2e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0ca2e-138">System.String</span></span>

## <span data-ttu-id="0ca2e-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ca2e-139">OUTPUTS</span></span>

### <span data-ttu-id="0ca2e-140">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="0ca2e-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="0ca2e-141">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="0ca2e-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="0ca2e-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ca2e-142">NOTES</span></span>

## <span data-ttu-id="0ca2e-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ca2e-143">RELATED LINKS</span></span>

[<span data-ttu-id="0ca2e-144">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="0ca2e-144">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="0ca2e-145">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="0ca2e-145">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="0ca2e-146">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="0ca2e-146">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="0ca2e-147">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="0ca2e-147">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


