---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C9470E5-21D2-4AF5-9F11-F66F94B133C0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23f4511f8e0439c1581cc388843a37266092f4d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006660"
---
# <span data-ttu-id="940d9-101">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="940d9-101">Remove-AzureVMImage</span></span>

## <span data-ttu-id="940d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="940d9-102">SYNOPSIS</span></span>
<span data-ttu-id="940d9-103">Entfernt ein Betriebssystemabbild aus dem Image-Repository.</span><span class="sxs-lookup"><span data-stu-id="940d9-103">Removes an operating system image from the image repository.</span></span>

## <span data-ttu-id="940d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="940d9-104">SYNTAX</span></span>

```
Remove-AzureVMImage [-ImageName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="940d9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="940d9-105">DESCRIPTION</span></span>
<span data-ttu-id="940d9-106">Das Cmdlet **Remove-AzureVMImage** entfernt ein Betriebssystemabbild aus dem Image-Repository.</span><span class="sxs-lookup"><span data-stu-id="940d9-106">The **Remove-AzureVMImage** cmdlet removes an operating system image from the image repository.</span></span>
<span data-ttu-id="940d9-107">Standardmäßig wird mit diesem Cmdlet nicht das zugeordnete physische Abbild-BLOB aus dem Speicherkonto gelöscht.</span><span class="sxs-lookup"><span data-stu-id="940d9-107">By default, this cmdlet does not delete the associated physical image blob from the storage account.</span></span>
<span data-ttu-id="940d9-108">Verwenden Sie den **DeleteVHD** -Parameter, um die zugeordnete virtuelle Festplatte (VHD) zu löschen.</span><span class="sxs-lookup"><span data-stu-id="940d9-108">To delete the associated virtual hard drive (VHD), use the **DeleteVHD** parameter.</span></span>

## <span data-ttu-id="940d9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="940d9-109">EXAMPLES</span></span>

### <span data-ttu-id="940d9-110">Beispiel 1: Entfernen eines Bilds aus dem Bild-Repository</span><span class="sxs-lookup"><span data-stu-id="940d9-110">Example 1: Remove an image from the image repository</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName "Image001"
```

<span data-ttu-id="940d9-111">Dieser Befehl entfernt das Bild mit dem Namen Image001 aus dem Bild-Repository.</span><span class="sxs-lookup"><span data-stu-id="940d9-111">This command removes the image named Image001 from the image repository.</span></span>

### <span data-ttu-id="940d9-112">Beispiel 2: Entfernen eines Bilds aus dem Bild-Repository und auch der VHD</span><span class="sxs-lookup"><span data-stu-id="940d9-112">Example 2: Remove an image from the image repository and also the VHD</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName " Image001" -DeleteVHD
```

<span data-ttu-id="940d9-113">Mit diesem Befehl wird das Bild mit dem Namen Image001 aus dem Bild-Repository entfernt und auch das physische VHD-Abbild aus dem Speicherkonto gelöscht.</span><span class="sxs-lookup"><span data-stu-id="940d9-113">This command removes the image named Image001 from the image repository and also deletes the physical VHD image from the storage account.</span></span>

### <span data-ttu-id="940d9-114">Beispiel 3: Einrichten eines Abonnement Kontexts und Entfernen aller Bilder</span><span class="sxs-lookup"><span data-stu-id="940d9-114">Example 3: Set a subscription context and then remove all the images</span></span>
```
PS C:\> $SubsId = &amp;lt;MySubscriptionID&amp;gt;
PS C:\> $Cert = Get-AzureCertificate cert:\LocalMachine\MY\&amp;lt;CertificateThumbprint&amp;gt;
PS C:\> Get-AzureVMImage `
| Where-Object {$_.Label -match "Beta" }`
| Foreach-Object {Remove-AzureVMImage -ImageName $_.name }
```

<span data-ttu-id="940d9-115">Mit diesem Befehl wird der Abonnement Kontext festgelegt und dann alle Bilder aus dem Image-Repository entfernt, dessen Beschriftung den Namen Beta enthält.</span><span class="sxs-lookup"><span data-stu-id="940d9-115">This command sets the subscription context and then removes all the images from the image repository whose Label includes the name Beta.</span></span>

## <span data-ttu-id="940d9-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="940d9-116">PARAMETERS</span></span>

### <span data-ttu-id="940d9-117">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="940d9-117">-DeleteVHD</span></span>
<span data-ttu-id="940d9-118">Gibt an, dass dieses Cmdlet den physikalischen VHD-Abbild-BLOB aus dem Speicherkonto löscht.</span><span class="sxs-lookup"><span data-stu-id="940d9-118">Indicates that this cmdlet deletes the physical VHD image blob from the storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940d9-119">-Bildname</span><span class="sxs-lookup"><span data-stu-id="940d9-119">-ImageName</span></span>
<span data-ttu-id="940d9-120">Gibt das Bild des Betriebssystems oder des virtuellen Computers an, das aus dem Image-Repository entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="940d9-120">Specifies the operating system or virtual machine image to remove from the image repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="940d9-121">-Information</span><span class="sxs-lookup"><span data-stu-id="940d9-121">-InformationAction</span></span>
<span data-ttu-id="940d9-122">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="940d9-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="940d9-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="940d9-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="940d9-124">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="940d9-124">Continue</span></span>
- <span data-ttu-id="940d9-125">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="940d9-125">Ignore</span></span>
- <span data-ttu-id="940d9-126">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="940d9-126">Inquire</span></span>
- <span data-ttu-id="940d9-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="940d9-127">SilentlyContinue</span></span>
- <span data-ttu-id="940d9-128">Beenden</span><span class="sxs-lookup"><span data-stu-id="940d9-128">Stop</span></span>
- <span data-ttu-id="940d9-129">Anhalten</span><span class="sxs-lookup"><span data-stu-id="940d9-129">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940d9-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="940d9-130">-InformationVariable</span></span>
<span data-ttu-id="940d9-131">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="940d9-131">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940d9-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="940d9-132">-Profile</span></span>
<span data-ttu-id="940d9-133">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="940d9-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="940d9-134">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="940d9-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940d9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="940d9-135">CommonParameters</span></span>
<span data-ttu-id="940d9-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="940d9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="940d9-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="940d9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="940d9-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="940d9-138">INPUTS</span></span>

## <span data-ttu-id="940d9-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="940d9-139">OUTPUTS</span></span>

## <span data-ttu-id="940d9-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="940d9-140">NOTES</span></span>

## <span data-ttu-id="940d9-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="940d9-141">RELATED LINKS</span></span>

[<span data-ttu-id="940d9-142">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="940d9-142">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="940d9-143">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="940d9-143">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="940d9-144">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="940d9-144">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="940d9-145">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="940d9-145">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


