---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DECCEE-86C8-4662-9ED0-D1BDB4E687C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68efd1c750646abffa90eb8318d0df189a4c9eb9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005921"
---
# <span data-ttu-id="8c1a1-101">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="8c1a1-101">Add-AzureVMImage</span></span>

## <span data-ttu-id="8c1a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8c1a1-102">SYNOPSIS</span></span>
<span data-ttu-id="8c1a1-103">Fügt ein neues Betriebssystemabbild oder ein neues Abbild eines virtuellen Computers zum Bild-Repository hinzu.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-103">Adds a new operating system image or a new virtual machine image to the image repository.</span></span>

## <span data-ttu-id="8c1a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c1a1-104">SYNTAX</span></span>

### <span data-ttu-id="8c1a1-105">OSImage (Standard)</span><span class="sxs-lookup"><span data-stu-id="8c1a1-105">OSImage (Default)</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-MediaLocation] <String> [-OS] <String> [[-Label] <String>]
 [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>]
 [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>] [[-SmallIconName] <String>]
 [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8c1a1-106">VMImage</span><span class="sxs-lookup"><span data-stu-id="8c1a1-106">VMImage</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-OS] <String>]
 [[-Label] <String>] [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>]
 [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8c1a1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c1a1-107">DESCRIPTION</span></span>
<span data-ttu-id="8c1a1-108">Das Cmdlet **Add-AzureVMImage** fügt ein neues Betriebssystemabbild oder ein neues Bild des virtuellen Computers zum Bild-Repository hinzu.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-108">The **Add-AzureVMImage** cmdlet adds a new operating system image or a new virtual machine image to the image repository.</span></span>
<span data-ttu-id="8c1a1-109">Bei dem Bild handelt es sich um ein generalisiertes Betriebssystemabbild, bei dem entweder Sysprep für Windows oder, für Linux, das entsprechende Tool für die Verteilung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-109">The image is a generalized operating system image, using either Sysprep for Windows or, for Linux, using the appropriate tool for the distribution.</span></span>

## <span data-ttu-id="8c1a1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c1a1-110">EXAMPLES</span></span>

### <span data-ttu-id="8c1a1-111">Beispiel 1: Hinzufügen eines Betriebssystemabbilds zum Repository</span><span class="sxs-lookup"><span data-stu-id="8c1a1-111">Example 1: Add an operating system image to the repository</span></span>
```
PS C:\> $S = New-AzureVMImageDiskConfigSet
PS C:\> Set-AzureVMImageOSDiskConfig -DiskConfig $S -HostCaching ReadWrite -OSState "Generalized" -OS "Windows" -MediaLink $Link
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test1" -HostCaching ReadWrite -Lun 0 -MediaLink $Link1
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4" -HostCaching ReadWrite -Lun 0 -MediaLink $Link
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4"
PS C:\> $IMGName = "TestCREATEvmimage2";
PS C:\> Add-AzureVMImage -ImageName $IMGName -Label "Test1" -Description "Test1" -DiskConfig $S -Eula "http://www.contoso.com" -ImageFamily Windows -PublishedDate (Get-Date) -PrivacyUri "http://www.test.com" -RecommendedVMSize Small -IconName "Icon01" -SmallIconName "SmallIcon01" -ShowInGui
```

<span data-ttu-id="8c1a1-112">In diesem Beispiel wird dem Repository ein Betriebssystembild hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-112">This example adds an operating system image to the repository.</span></span>

## <span data-ttu-id="8c1a1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c1a1-113">PARAMETERS</span></span>

### <span data-ttu-id="8c1a1-114">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c1a1-114">-Description</span></span>
<span data-ttu-id="8c1a1-115">Gibt die Beschreibung des Betriebssystemabbilds an.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-115">Specifies the description of the operating system image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1a1-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="8c1a1-116">-DiskConfig</span></span>
<span data-ttu-id="8c1a1-117">Gibt die Festplattenkonfiguration des Betriebssystems für das Bild des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-117">Specifies the operating system disk configuration for the virtual machine image.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: VMImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1a1-118">-EULA</span><span class="sxs-lookup"><span data-stu-id="8c1a1-118">-Eula</span></span>
<span data-ttu-id="8c1a1-119">Gibt den Endbenutzer-Lizenzvertrag an.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-119">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="8c1a1-120">Es wird empfohlen, dass Sie eine URL für diesen Wert verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-120">It is recommended that you use an URL for this value.</span></span>

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

### <span data-ttu-id="8c1a1-121">-IconName</span><span class="sxs-lookup"><span data-stu-id="8c1a1-121">-IconName</span></span>
<span data-ttu-id="8c1a1-122">Gibt den Namen des Symbols an, das verwendet wird, wenn das Bild zum Repository hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-122">Specifies the name of the icon that is used when the image is added to the repository.</span></span>

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

### <span data-ttu-id="8c1a1-123">-Imagefamily</span><span class="sxs-lookup"><span data-stu-id="8c1a1-123">-ImageFamily</span></span>
<span data-ttu-id="8c1a1-124">Gibt einen Wert an, der zum Gruppieren von Betriebssystemabbildern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-124">Specifies a value that is used to group operating system images.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1a1-125">-Bildname</span><span class="sxs-lookup"><span data-stu-id="8c1a1-125">-ImageName</span></span>
<span data-ttu-id="8c1a1-126">Gibt den Namen des Bilds an, das dem Bild-Repository hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-126">Specifies the name of the image being added to the image repository.</span></span>

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

### <span data-ttu-id="8c1a1-127">-Information</span><span class="sxs-lookup"><span data-stu-id="8c1a1-127">-InformationAction</span></span>
<span data-ttu-id="8c1a1-128">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8c1a1-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8c1a1-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c1a1-130">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="8c1a1-130">Continue</span></span>
- <span data-ttu-id="8c1a1-131">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="8c1a1-131">Ignore</span></span>
- <span data-ttu-id="8c1a1-132">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="8c1a1-132">Inquire</span></span>
- <span data-ttu-id="8c1a1-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8c1a1-133">SilentlyContinue</span></span>
- <span data-ttu-id="8c1a1-134">Beenden</span><span class="sxs-lookup"><span data-stu-id="8c1a1-134">Stop</span></span>
- <span data-ttu-id="8c1a1-135">Anhalten</span><span class="sxs-lookup"><span data-stu-id="8c1a1-135">Suspend</span></span>

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

### <span data-ttu-id="8c1a1-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8c1a1-136">-InformationVariable</span></span>
<span data-ttu-id="8c1a1-137">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8c1a1-138">-Label</span><span class="sxs-lookup"><span data-stu-id="8c1a1-138">-Label</span></span>
<span data-ttu-id="8c1a1-139">Gibt eine Beschriftung an, um das Bild zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-139">Specifies a label to give the image.</span></span>

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

### <span data-ttu-id="8c1a1-140">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="8c1a1-140">-MediaLocation</span></span>
<span data-ttu-id="8c1a1-141">Gibt den Speicherort der physikalischen BLOB-Seite an, auf der sich das Bild befindet.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-141">Specifies the location of the physical blob page where the image resides.</span></span>
<span data-ttu-id="8c1a1-142">Hierbei handelt es sich um einen Link zu einer BLOB-Seite im Speicher des aktuellen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-142">This is a link to a blob page in the current subscription's storage.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1a1-143">-OS</span><span class="sxs-lookup"><span data-stu-id="8c1a1-143">-OS</span></span>
<span data-ttu-id="8c1a1-144">Gibt die Version des Betriebssystems für das Bild an.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-144">Specifies the operating system version of the image.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: VMImage
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1a1-145">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="8c1a1-145">-PrivacyUri</span></span>
<span data-ttu-id="8c1a1-146">Gibt die URL an, die auf ein Dokument verweist, das die Datenschutzrichtlinie enthält, die sich auf das Betriebssystemabbild bezieht.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-146">Specifies the URL that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1a1-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="8c1a1-147">-Profile</span></span>
<span data-ttu-id="8c1a1-148">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8c1a1-149">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8c1a1-150">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="8c1a1-150">-PublishedDate</span></span>
<span data-ttu-id="8c1a1-151">Gibt das Datum an, an dem das Betriebssystemabbild dem Image-Repository hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-151">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1a1-152">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="8c1a1-152">-RecommendedVMSize</span></span>
<span data-ttu-id="8c1a1-153">Gibt die Größe an, die für den virtuellen Computer verwendet werden soll, der aus dem Betriebssystemabbild erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-153">Specifies the size to use for the virtual machine that is created from the operating system image.</span></span>

<span data-ttu-id="8c1a1-154">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8c1a1-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c1a1-155">Mittel</span><span class="sxs-lookup"><span data-stu-id="8c1a1-155">Medium</span></span>
- <span data-ttu-id="8c1a1-156">Große</span><span class="sxs-lookup"><span data-stu-id="8c1a1-156">Large</span></span>
- <span data-ttu-id="8c1a1-157">Extra Large</span><span class="sxs-lookup"><span data-stu-id="8c1a1-157">ExtraLarge</span></span>
- <span data-ttu-id="8c1a1-158">A5</span><span class="sxs-lookup"><span data-stu-id="8c1a1-158">A5</span></span>
- <span data-ttu-id="8c1a1-159">A6</span><span class="sxs-lookup"><span data-stu-id="8c1a1-159">A6</span></span>
- <span data-ttu-id="8c1a1-160">A7</span><span class="sxs-lookup"><span data-stu-id="8c1a1-160">A7</span></span>

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

### <span data-ttu-id="8c1a1-161">-ShowInGui</span><span class="sxs-lookup"><span data-stu-id="8c1a1-161">-ShowInGui</span></span>
<span data-ttu-id="8c1a1-162">Gibt an, dass dieses Cmdlet das Bild in der GUI anzeigt.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-162">Indicates that this cmdlet shows the image in the GUI.</span></span>

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

### <span data-ttu-id="8c1a1-163">-SmallIconName</span><span class="sxs-lookup"><span data-stu-id="8c1a1-163">-SmallIconName</span></span>
<span data-ttu-id="8c1a1-164">Gibt den Namen des kleinen Symbols an, das verwendet wird, wenn das Bild zum Repository hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-164">Specifies the name of the small icon that is used when the image is added to the repository.</span></span>

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

### <span data-ttu-id="8c1a1-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c1a1-165">CommonParameters</span></span>
<span data-ttu-id="8c1a1-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c1a1-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c1a1-167">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c1a1-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c1a1-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8c1a1-168">INPUTS</span></span>

## <span data-ttu-id="8c1a1-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8c1a1-169">OUTPUTS</span></span>

### <span data-ttu-id="8c1a1-170">OSImageContext</span><span class="sxs-lookup"><span data-stu-id="8c1a1-170">OSImageContext</span></span>

## <span data-ttu-id="8c1a1-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="8c1a1-171">NOTES</span></span>

## <span data-ttu-id="8c1a1-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8c1a1-172">RELATED LINKS</span></span>

[<span data-ttu-id="8c1a1-173">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="8c1a1-173">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="8c1a1-174">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="8c1a1-174">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="8c1a1-175">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="8c1a1-175">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="8c1a1-176">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="8c1a1-176">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


