---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5544F2E2-27EF-4079-8E13-6B85DF2018A2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a71ad8b25a17c1c2933cdcf305ba0b53f67bf0f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006789"
---
# <span data-ttu-id="ec404-101">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ec404-101">Update-AzureVMImage</span></span>

## <span data-ttu-id="ec404-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec404-102">SYNOPSIS</span></span>
<span data-ttu-id="ec404-103">Aktualisiert die Beschriftung eines Betriebssystemabbilds im Bild-Repository.</span><span class="sxs-lookup"><span data-stu-id="ec404-103">Updates the label of an operating system image in the image repository.</span></span>

## <span data-ttu-id="ec404-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec404-104">SYNTAX</span></span>

```
Update-AzureVMImage [-ImageName] <String> [-Label] <String> [[-Eula] <String>] [[-Description] <String>]
 [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>]
 [[-DiskConfig] <VirtualMachineImageDiskConfigSet>] [[-Language] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-DontShowInGui] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ec404-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec404-105">DESCRIPTION</span></span>
<span data-ttu-id="ec404-106">Das Cmdlet **Update-AzureVMImage** aktualisiert die Beschriftung eines Betriebssystemabbilds im Bild-Repository.</span><span class="sxs-lookup"><span data-stu-id="ec404-106">The **Update-AzureVMImage** cmdlet updates the label on an operating system image in the image repository.</span></span>
<span data-ttu-id="ec404-107">Sie gibt ein Image-Objekt mit Informationen über das aktualisierte Bild zurück.</span><span class="sxs-lookup"><span data-stu-id="ec404-107">It returns an image object with information about the updated image.</span></span>

## <span data-ttu-id="ec404-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec404-108">EXAMPLES</span></span>

### <span data-ttu-id="ec404-109">Beispiel 1: Aktualisieren eines Bilds durch Ändern der Bildbeschriftung</span><span class="sxs-lookup"><span data-stu-id="ec404-109">Example 1: Update an image by changing the image label</span></span>
```
PS C:\> Update-AzureVMImage -ImageName "Windows-Server-2008-SP2" -Label "DoNotUse"
```

<span data-ttu-id="ec404-110">Dieser Befehl aktualisiert das Bild mit dem Namen Windows-Server-2008-SP2 durch Ändern der Bildbeschriftung in DoNotUse.</span><span class="sxs-lookup"><span data-stu-id="ec404-110">This command updates the image named Windows-Server-2008-SP2 by changing the image label to DoNotUse.</span></span>

### <span data-ttu-id="ec404-111">Beispiel 2: Abrufen aller Betriebssysteme nach Beschriftung und Aktualisieren der Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="ec404-111">Example 2: Get all operating systems by label and then update the label</span></span>
```
PS C:\> Get-AzureVMImage | Where-Object {$_.Label -eq "DoNotUse" } | Update-AzureVMImage -Label "Updated"
```

<span data-ttu-id="ec404-112">Dieser Befehl ruft alle Betriebssystem Bilder mit der Bezeichnung "DoNotUse" ab und ändert die Beschriftung in "aktualisiert".</span><span class="sxs-lookup"><span data-stu-id="ec404-112">This command gets all the operating system images labeled DoNotUse and changes the label to Updated.</span></span>

## <span data-ttu-id="ec404-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec404-113">PARAMETERS</span></span>

### <span data-ttu-id="ec404-114">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec404-114">-Description</span></span>
<span data-ttu-id="ec404-115">Gibt die Beschreibung des Betriebssystemabbilds an.</span><span class="sxs-lookup"><span data-stu-id="ec404-115">Specifies the description of the operating system image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec404-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="ec404-116">-DiskConfig</span></span>
<span data-ttu-id="ec404-117">Gibt den Betriebssystemdatenträger und die Datenträgerkonfiguration für das Bild des virtuellen Computers an, das mit den Cmdlets **New-AzureVMImageDiskConfigSet** , **AzureVMImageOSDiskConfig** und **festgelegt** wurde.</span><span class="sxs-lookup"><span data-stu-id="ec404-117">Specifies the operating system disk and data disk configuration for the virtual machine image created by using the **New-AzureVMImageDiskConfigSet** , **Set-AzureVMImageOSDiskConfig** , and **Set-AzureVMImageDataDiskConfig** cmdlets.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec404-118">-DontShowInGui</span><span class="sxs-lookup"><span data-stu-id="ec404-118">-DontShowInGui</span></span>
<span data-ttu-id="ec404-119">Gibt an, dass dieses Cmdlet das Bild nicht in der GUI anzeigt.</span><span class="sxs-lookup"><span data-stu-id="ec404-119">Indicates that this cmdlet does not show the image in the GUI.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec404-120">-EULA</span><span class="sxs-lookup"><span data-stu-id="ec404-120">-Eula</span></span>
<span data-ttu-id="ec404-121">Gibt den Endbenutzer-Lizenzvertrag an.</span><span class="sxs-lookup"><span data-stu-id="ec404-121">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="ec404-122">Wir empfehlen, dass es sich bei dem Wert um eine URL handelt.</span><span class="sxs-lookup"><span data-stu-id="ec404-122">We recommend that the value is a URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec404-123">-IconName</span><span class="sxs-lookup"><span data-stu-id="ec404-123">-IconName</span></span>
<span data-ttu-id="ec404-124">Gibt den Standardsymbolnamen für das Betriebssystem oder das Bild des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="ec404-124">Specifies the standard icon name for the operating system or virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IconUri

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec404-125">-Imagefamily</span><span class="sxs-lookup"><span data-stu-id="ec404-125">-ImageFamily</span></span>
<span data-ttu-id="ec404-126">Gibt einen Wert an, der zum Gruppieren von Bildern des Betriebssystem-oder virtuellen Computers verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ec404-126">Specifies a value that can be used to group operating system or virtual machine images.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec404-127">-Bildname</span><span class="sxs-lookup"><span data-stu-id="ec404-127">-ImageName</span></span>
<span data-ttu-id="ec404-128">Gibt den Namen des Bilds an, das im Bild-Repository aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec404-128">Specifies the name of the image to update in the image repository.</span></span>

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

### <span data-ttu-id="ec404-129">-Information</span><span class="sxs-lookup"><span data-stu-id="ec404-129">-InformationAction</span></span>
<span data-ttu-id="ec404-130">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="ec404-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ec404-131">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ec404-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ec404-132">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="ec404-132">Continue</span></span>
- <span data-ttu-id="ec404-133">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="ec404-133">Ignore</span></span>
- <span data-ttu-id="ec404-134">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="ec404-134">Inquire</span></span>
- <span data-ttu-id="ec404-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ec404-135">SilentlyContinue</span></span>
- <span data-ttu-id="ec404-136">Beenden</span><span class="sxs-lookup"><span data-stu-id="ec404-136">Stop</span></span>
- <span data-ttu-id="ec404-137">Anhalten</span><span class="sxs-lookup"><span data-stu-id="ec404-137">Suspend</span></span>

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

### <span data-ttu-id="ec404-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ec404-138">-InformationVariable</span></span>
<span data-ttu-id="ec404-139">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="ec404-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ec404-140">-Label</span><span class="sxs-lookup"><span data-stu-id="ec404-140">-Label</span></span>
<span data-ttu-id="ec404-141">Gibt die neue Beschriftung des Bilds an.</span><span class="sxs-lookup"><span data-stu-id="ec404-141">Specifies the new label of the image.</span></span>

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

### <span data-ttu-id="ec404-142">– Sprache</span><span class="sxs-lookup"><span data-stu-id="ec404-142">-Language</span></span>
<span data-ttu-id="ec404-143">Gibt die Sprache für das Betriebssystem auf dem virtuellen Computer oder dem Betriebssystemabbild an.</span><span class="sxs-lookup"><span data-stu-id="ec404-143">Specifies the language for the operating system in the virtual machine or operating system image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec404-144">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="ec404-144">-PrivacyUri</span></span>
<span data-ttu-id="ec404-145">Gibt den URI an, der auf ein Dokument verweist, das die Datenschutzrichtlinie enthält, die sich auf das Betriebssystemabbild bezieht.</span><span class="sxs-lookup"><span data-stu-id="ec404-145">Specifies the URI that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec404-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="ec404-146">-Profile</span></span>
<span data-ttu-id="ec404-147">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ec404-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ec404-148">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ec404-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ec404-149">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="ec404-149">-PublishedDate</span></span>
<span data-ttu-id="ec404-150">Gibt das Datum an, an dem das Betriebssystemabbild dem Image-Repository hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="ec404-150">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec404-151">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="ec404-151">-RecommendedVMSize</span></span>
<span data-ttu-id="ec404-152">Gibt die Größe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="ec404-152">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="ec404-153">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ec404-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ec404-154">Mittel</span><span class="sxs-lookup"><span data-stu-id="ec404-154">Medium</span></span>
- <span data-ttu-id="ec404-155">Große</span><span class="sxs-lookup"><span data-stu-id="ec404-155">Large</span></span>
- <span data-ttu-id="ec404-156">Extra Large</span><span class="sxs-lookup"><span data-stu-id="ec404-156">ExtraLarge</span></span>
- <span data-ttu-id="ec404-157">A5</span><span class="sxs-lookup"><span data-stu-id="ec404-157">A5</span></span>
- <span data-ttu-id="ec404-158">A6</span><span class="sxs-lookup"><span data-stu-id="ec404-158">A6</span></span>
- <span data-ttu-id="ec404-159">A7</span><span class="sxs-lookup"><span data-stu-id="ec404-159">A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec404-160">-SmallIconName</span><span class="sxs-lookup"><span data-stu-id="ec404-160">-SmallIconName</span></span>
<span data-ttu-id="ec404-161">Gibt den kleinen Symbolnamen für das Betriebssystem oder das Bild des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="ec404-161">Specifies the small icon name for the operating system or virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SmallIconUri

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec404-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec404-162">CommonParameters</span></span>
<span data-ttu-id="ec404-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec404-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec404-164">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec404-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec404-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec404-165">INPUTS</span></span>

## <span data-ttu-id="ec404-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec404-166">OUTPUTS</span></span>

### <span data-ttu-id="ec404-167">OSImageContext</span><span class="sxs-lookup"><span data-stu-id="ec404-167">OSImageContext</span></span>

## <span data-ttu-id="ec404-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec404-168">NOTES</span></span>

## <span data-ttu-id="ec404-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec404-169">RELATED LINKS</span></span>

[<span data-ttu-id="ec404-170">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ec404-170">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="ec404-171">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ec404-171">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="ec404-172">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ec404-172">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="ec404-173">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ec404-173">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="ec404-174">Neu – AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="ec404-174">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="ec404-175">Satz-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ec404-175">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="ec404-176">Satz-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ec404-176">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


