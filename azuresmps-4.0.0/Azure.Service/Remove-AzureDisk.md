---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 75A50C59-28D1-4D29-A420-D24BF479F79E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29e5e7e0bc2fcc0ce93186cf966f18d6c9c3e372
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006363"
---
# <span data-ttu-id="e567f-101">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="e567f-101">Remove-AzureDisk</span></span>

## <span data-ttu-id="e567f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e567f-102">SYNOPSIS</span></span>
<span data-ttu-id="e567f-103">Entfernt einen Datenträger aus dem Azure Disk Repository.</span><span class="sxs-lookup"><span data-stu-id="e567f-103">Removes a disk from the Azure disk repository.</span></span>

## <span data-ttu-id="e567f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e567f-104">SYNTAX</span></span>

```
Remove-AzureDisk [-DiskName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e567f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e567f-105">DESCRIPTION</span></span>
<span data-ttu-id="e567f-106">Das Cmdlet **Remove-AzureDisk** entfernt einen Datenträger aus dem Azure Disk Repository im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e567f-106">The **Remove-AzureDisk** cmdlet removes a disk from the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="e567f-107">Standardmäßig wird mit diesem Cmdlet keine VHD-Datei (Virtual Hard Disk) aus dem BLOB-Speicher gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e567f-107">By default, this cmdlet does not delete the virtual hard disk (VHD) file from blob storage.</span></span>
<span data-ttu-id="e567f-108">Um die VHD zu löschen, geben Sie den Parameter *DeleteVHD* an.</span><span class="sxs-lookup"><span data-stu-id="e567f-108">To delete the VHD, specify the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="e567f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e567f-109">EXAMPLES</span></span>

### <span data-ttu-id="e567f-110">Beispiel 1: Entfernen eines Datenträgers</span><span class="sxs-lookup"><span data-stu-id="e567f-110">Example 1: Remove a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="e567f-111">Dieser Befehl entfernt den Datenträger mit dem Namen ContosoDataDisk Disk aus dem Datenträger-Repository.</span><span class="sxs-lookup"><span data-stu-id="e567f-111">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="e567f-112">Der Befehl löscht die VHD nicht.</span><span class="sxs-lookup"><span data-stu-id="e567f-112">The command does not delete the VHD.</span></span>

### <span data-ttu-id="e567f-113">Beispiel 2: entfernen und Löschen eines Datenträgers</span><span class="sxs-lookup"><span data-stu-id="e567f-113">Example 2: Remove and delete a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk" -DeleteVHD
```

<span data-ttu-id="e567f-114">Dieser Befehl entfernt den Datenträger mit dem Namen ContosoDataDisk Disk aus dem Datenträger-Repository.</span><span class="sxs-lookup"><span data-stu-id="e567f-114">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="e567f-115">Mit diesem Befehl wird der DeleteVHD-Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="e567f-115">This command specifies the DeleteVHD parameter.</span></span>
<span data-ttu-id="e567f-116">Daher löscht der Befehl die VHD aus dem Azure-Speicher.</span><span class="sxs-lookup"><span data-stu-id="e567f-116">Therefore, the command deletes the VHD from Azure Storage.</span></span>

## <span data-ttu-id="e567f-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="e567f-117">PARAMETERS</span></span>

### <span data-ttu-id="e567f-118">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="e567f-118">-DeleteVHD</span></span>
<span data-ttu-id="e567f-119">Gibt an, dass dieses Cmdlet die VHD aus dem BLOB-Speicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="e567f-119">Indicates that this cmdlet removes the VHD from blob storage.</span></span>

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

### <span data-ttu-id="e567f-120">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="e567f-120">-DiskName</span></span>
<span data-ttu-id="e567f-121">Gibt den Namen des Daten Datenträgers im Datenträger-Repository an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="e567f-121">Specifies the name of the data disk in the disk repository that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e567f-122">-Information</span><span class="sxs-lookup"><span data-stu-id="e567f-122">-InformationAction</span></span>
<span data-ttu-id="e567f-123">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="e567f-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e567f-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e567f-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e567f-125">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="e567f-125">Continue</span></span>
- <span data-ttu-id="e567f-126">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="e567f-126">Ignore</span></span>
- <span data-ttu-id="e567f-127">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="e567f-127">Inquire</span></span>
- <span data-ttu-id="e567f-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e567f-128">SilentlyContinue</span></span>
- <span data-ttu-id="e567f-129">Beenden</span><span class="sxs-lookup"><span data-stu-id="e567f-129">Stop</span></span>
- <span data-ttu-id="e567f-130">Anhalten</span><span class="sxs-lookup"><span data-stu-id="e567f-130">Suspend</span></span>

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

### <span data-ttu-id="e567f-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e567f-131">-InformationVariable</span></span>
<span data-ttu-id="e567f-132">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="e567f-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e567f-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="e567f-133">-Profile</span></span>
<span data-ttu-id="e567f-134">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="e567f-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e567f-135">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="e567f-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e567f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e567f-136">CommonParameters</span></span>
<span data-ttu-id="e567f-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e567f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e567f-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e567f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e567f-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e567f-139">INPUTS</span></span>

## <span data-ttu-id="e567f-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e567f-140">OUTPUTS</span></span>

## <span data-ttu-id="e567f-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="e567f-141">NOTES</span></span>

## <span data-ttu-id="e567f-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e567f-142">RELATED LINKS</span></span>

[<span data-ttu-id="e567f-143">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="e567f-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="e567f-144">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="e567f-144">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="e567f-145">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="e567f-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


