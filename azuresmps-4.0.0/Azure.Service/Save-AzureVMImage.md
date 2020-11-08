---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A1CE31E-0158-441E-BC2D-B5D21C9D9421
online version: ''
schema: 2.0.0
ms.openlocfilehash: a956aa7eaf383b0cf5cdb20b39d2f6b54e292f92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005657"
---
# <span data-ttu-id="067c4-101">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="067c4-101">Save-AzureVMImage</span></span>

## <span data-ttu-id="067c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="067c4-102">SYNOPSIS</span></span>
<span data-ttu-id="067c4-103">Erfasst und speichert das Bild eines gestoppten Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="067c4-103">Captures and saves the image of a stopped Azure virtual machine.</span></span>

## <span data-ttu-id="067c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="067c4-104">SYNTAX</span></span>

```
Save-AzureVMImage [-ServiceName] <String> [-Name] <String> [-ImageName] <String> [[-ImageLabel] <String>]
 [[-OSState] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="067c4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="067c4-105">DESCRIPTION</span></span>
<span data-ttu-id="067c4-106">Das Cmdlet **Save-AzureVMImage** erfasst und speichert das Bild eines gestoppten Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="067c4-106">The **Save-AzureVMImage** cmdlet captures and saves the image of a stopped Azure virtual machine.</span></span>
<span data-ttu-id="067c4-107">Führen Sie bei Windows-virtuellen Computern das Sysprep-Tool aus, um das Bild vorzubereiten, bevor es erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="067c4-107">For Windows virtual machines, run the Sysprep tool to prepare the image before it is captured.</span></span>
<span data-ttu-id="067c4-108">Nachdem das Bild aufgenommen wurde, wird der virtuelle Computer gelöscht.</span><span class="sxs-lookup"><span data-stu-id="067c4-108">After the image is captured, the virtual machine is deleted.</span></span>

## <span data-ttu-id="067c4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="067c4-109">EXAMPLES</span></span>

### <span data-ttu-id="067c4-110">Beispiel 1: Speichern einer vorhandenen virtuellen Maschine und anschließendes Löschen aus einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="067c4-110">Example 1: Save an existing virtual machine and then delete it from a deployment</span></span>
```
PS C:\> Save-AzureVMImage -ServiceName "MyService" -Name "MyVM" -NewImageName "MyBaseImage" -NewImageLabel "MyBaseVM"
```

<span data-ttu-id="067c4-111">Dieser Befehl zeichnet einen vorhandenen virtuellen Computer auf und löscht ihn aus der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="067c4-111">This command captures an existing virtual machine and deletes it from the deployment.</span></span>

## <span data-ttu-id="067c4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="067c4-112">PARAMETERS</span></span>

### <span data-ttu-id="067c4-113">-ImageLabel</span><span class="sxs-lookup"><span data-stu-id="067c4-113">-ImageLabel</span></span>
<span data-ttu-id="067c4-114">Gibt die Beschriftung des virtuellen Computer Bilds an.</span><span class="sxs-lookup"><span data-stu-id="067c4-114">Specifies the label of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageLabel

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="067c4-115">-Bildname</span><span class="sxs-lookup"><span data-stu-id="067c4-115">-ImageName</span></span>
<span data-ttu-id="067c4-116">Gibt den Namen des virtuellen Computer Bilds an.</span><span class="sxs-lookup"><span data-stu-id="067c4-116">Specifies the name of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="067c4-117">-Information</span><span class="sxs-lookup"><span data-stu-id="067c4-117">-InformationAction</span></span>
<span data-ttu-id="067c4-118">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="067c4-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="067c4-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="067c4-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="067c4-120">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="067c4-120">Continue</span></span>
- <span data-ttu-id="067c4-121">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="067c4-121">Ignore</span></span>
- <span data-ttu-id="067c4-122">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="067c4-122">Inquire</span></span>
- <span data-ttu-id="067c4-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="067c4-123">SilentlyContinue</span></span>
- <span data-ttu-id="067c4-124">Beenden</span><span class="sxs-lookup"><span data-stu-id="067c4-124">Stop</span></span>
- <span data-ttu-id="067c4-125">Anhalten</span><span class="sxs-lookup"><span data-stu-id="067c4-125">Suspend</span></span>

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

### <span data-ttu-id="067c4-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="067c4-126">-InformationVariable</span></span>
<span data-ttu-id="067c4-127">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="067c4-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="067c4-128">-Name</span><span class="sxs-lookup"><span data-stu-id="067c4-128">-Name</span></span>
<span data-ttu-id="067c4-129">Gibt den Namen der virtuellen Quellmaschine an.</span><span class="sxs-lookup"><span data-stu-id="067c4-129">Specifies the name of the source virtual machine.</span></span>

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

### <span data-ttu-id="067c4-130">-OSState</span><span class="sxs-lookup"><span data-stu-id="067c4-130">-OSState</span></span>
<span data-ttu-id="067c4-131">Gibt den Zustand des Betriebssystems für das Bild des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="067c4-131">Specifies the operation system state for the virtual machine image.</span></span>
<span data-ttu-id="067c4-132">Verwenden Sie diesen Parameter, wenn Sie beabsichtigen, ein Bild eines virtuellen Computers in Azure zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="067c4-132">Use this parameter if you intend to capture a virtual machine image to Azure.</span></span>

<span data-ttu-id="067c4-133">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="067c4-133">Valid values are:</span></span>

- <span data-ttu-id="067c4-134">Generalisierten</span><span class="sxs-lookup"><span data-stu-id="067c4-134">Generalized</span></span>
- <span data-ttu-id="067c4-135">Spezielle</span><span class="sxs-lookup"><span data-stu-id="067c4-135">Specialized</span></span>

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

### <span data-ttu-id="067c4-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="067c4-136">-Profile</span></span>
<span data-ttu-id="067c4-137">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="067c4-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="067c4-138">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="067c4-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="067c4-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="067c4-139">-ServiceName</span></span>
<span data-ttu-id="067c4-140">Gibt den Namen des Azure-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="067c4-140">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="067c4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="067c4-141">CommonParameters</span></span>
<span data-ttu-id="067c4-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="067c4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="067c4-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="067c4-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="067c4-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="067c4-144">INPUTS</span></span>

## <span data-ttu-id="067c4-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="067c4-145">OUTPUTS</span></span>

## <span data-ttu-id="067c4-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="067c4-146">NOTES</span></span>

## <span data-ttu-id="067c4-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="067c4-147">RELATED LINKS</span></span>

[<span data-ttu-id="067c4-148">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="067c4-148">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="067c4-149">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="067c4-149">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="067c4-150">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="067c4-150">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="067c4-151">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="067c4-151">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


