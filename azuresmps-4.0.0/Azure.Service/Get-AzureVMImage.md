---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006738"
---
# <span data-ttu-id="70d04-101">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="70d04-101">Get-AzureVMImage</span></span>

## <span data-ttu-id="70d04-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70d04-102">SYNOPSIS</span></span>
<span data-ttu-id="70d04-103">Ruft die Eigenschaften für eine oder eine Liste von Betriebssystemen oder ein Bild eines virtuellen Computers im Bild-Repository ab.</span><span class="sxs-lookup"><span data-stu-id="70d04-103">Gets the properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>

## <span data-ttu-id="70d04-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70d04-104">SYNTAX</span></span>

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="70d04-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70d04-105">DESCRIPTION</span></span>
<span data-ttu-id="70d04-106">Das Cmdlet " **Get-AzureVMImage** " Ruft Eigenschaften für eine oder eine Liste von Betriebssystemen oder ein Bild eines virtuellen Computers im Bild-Repository ab.</span><span class="sxs-lookup"><span data-stu-id="70d04-106">The **Get-AzureVMImage** cmdlet gets properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>
<span data-ttu-id="70d04-107">Das Cmdlet gibt Informationen zu allen Bildern im Repository oder zu einem bestimmten Bild zurück, wenn sein Bildname angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="70d04-107">The cmdlet returns information for all images in the repository, or about a specific image if its image name is provided.</span></span>

## <span data-ttu-id="70d04-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70d04-108">EXAMPLES</span></span>

### <span data-ttu-id="70d04-109">Beispiel 1: Abrufen eines bestimmten Image-Objekts aus dem aktuellen Bild-Repository.</span><span class="sxs-lookup"><span data-stu-id="70d04-109">Example 1: Get a specific image object from the current image repository.</span></span>
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

<span data-ttu-id="70d04-110">Dieser Befehl ruft das Image-Objekt mit dem Namen Image001 aus dem aktuellen Bild-Repository ab.</span><span class="sxs-lookup"><span data-stu-id="70d04-110">This command gets the image object named Image001 from the current image repository.</span></span>

### <span data-ttu-id="70d04-111">Beispiel 2: Abrufen aller Bilder aus dem aktuellen Bild-Repository</span><span class="sxs-lookup"><span data-stu-id="70d04-111">Example 2: Get all images from the current image repository</span></span>
```
PS C:\> Get-AzureVMImage
```

<span data-ttu-id="70d04-112">Dieser Befehl ruft alle Bilder aus dem aktuellen Bild-Repository ab.</span><span class="sxs-lookup"><span data-stu-id="70d04-112">This command retrieves all the images from the current image repository.</span></span>

### <span data-ttu-id="70d04-113">Beispiel 3: Einrichten des Abonnement Kontexts und Abrufen aller Bilder</span><span class="sxs-lookup"><span data-stu-id="70d04-113">Example 3: Set the subscription context and then get all the images</span></span>
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

<span data-ttu-id="70d04-114">Mit diesem Befehl wird der Abonnement Kontext festgelegt und dann alle Bilder aus dem Bild-Repository abgerufen.</span><span class="sxs-lookup"><span data-stu-id="70d04-114">This command sets the subscription context and then retrieves all the images from the image repository.</span></span>

## <span data-ttu-id="70d04-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="70d04-115">PARAMETERS</span></span>

### <span data-ttu-id="70d04-116">-Bildname</span><span class="sxs-lookup"><span data-stu-id="70d04-116">-ImageName</span></span>
<span data-ttu-id="70d04-117">Gibt den Namen des Betriebssystem-oder virtuellen Computer Bilds im Bild-Repository an.</span><span class="sxs-lookup"><span data-stu-id="70d04-117">Specifies the name of the operating system or virtual machine image in the image repository.</span></span>
<span data-ttu-id="70d04-118">Wenn Sie diesen Parameter nicht angeben, werden alle Bilder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="70d04-118">If you do not specify this parameter, all the images are returned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70d04-119">-Information</span><span class="sxs-lookup"><span data-stu-id="70d04-119">-InformationAction</span></span>
<span data-ttu-id="70d04-120">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="70d04-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="70d04-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="70d04-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="70d04-122">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="70d04-122">Continue</span></span>
- <span data-ttu-id="70d04-123">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="70d04-123">Ignore</span></span>
- <span data-ttu-id="70d04-124">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="70d04-124">Inquire</span></span>
- <span data-ttu-id="70d04-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="70d04-125">SilentlyContinue</span></span>
- <span data-ttu-id="70d04-126">Beenden</span><span class="sxs-lookup"><span data-stu-id="70d04-126">Stop</span></span>
- <span data-ttu-id="70d04-127">Anhalten</span><span class="sxs-lookup"><span data-stu-id="70d04-127">Suspend</span></span>

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

### <span data-ttu-id="70d04-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="70d04-128">-InformationVariable</span></span>
<span data-ttu-id="70d04-129">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="70d04-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="70d04-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="70d04-130">-Profile</span></span>
<span data-ttu-id="70d04-131">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="70d04-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="70d04-132">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="70d04-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="70d04-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70d04-133">CommonParameters</span></span>
<span data-ttu-id="70d04-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70d04-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70d04-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70d04-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70d04-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70d04-136">INPUTS</span></span>

## <span data-ttu-id="70d04-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70d04-137">OUTPUTS</span></span>

## <span data-ttu-id="70d04-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="70d04-138">NOTES</span></span>

## <span data-ttu-id="70d04-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70d04-139">RELATED LINKS</span></span>

[<span data-ttu-id="70d04-140">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="70d04-140">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="70d04-141">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="70d04-141">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="70d04-142">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="70d04-142">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="70d04-143">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="70d04-143">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


