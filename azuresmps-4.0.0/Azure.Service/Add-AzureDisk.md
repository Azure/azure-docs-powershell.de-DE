---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 16A34F31-1C61-4911-8C1F-9F82683524A1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 775d2deff8a83e758d48fb9328bf4156b142d20c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006599"
---
# <span data-ttu-id="381a1-101">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="381a1-101">Add-AzureDisk</span></span>

## <span data-ttu-id="381a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="381a1-102">SYNOPSIS</span></span>
<span data-ttu-id="381a1-103">Fügt dem Azure Disk Repository einen Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="381a1-103">Adds a disk to the Azure disk repository.</span></span>

## <span data-ttu-id="381a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="381a1-104">SYNTAX</span></span>

```
Add-AzureDisk [-DiskName] <String> [-MediaLocation] <String> [-Label <String>] [-OS <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="381a1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="381a1-105">DESCRIPTION</span></span>
<span data-ttu-id="381a1-106">Das Cmdlet **Add-AzureDisk** fügt dem Azure Disk Repository im aktuellen Abonnement einen Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="381a1-106">The **Add-AzureDisk** cmdlet adds a disk to the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="381a1-107">Mit diesem Cmdlet kann ein Systemdatenträger oder ein Daten Datenträger hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="381a1-107">This cmdlet can add a system disk or a data disk.</span></span>
<span data-ttu-id="381a1-108">Geben Sie zum Hinzufügen eines Systemdatenträgers einen Betriebssystemtyp mithilfe des Parameters " *OS* " an.</span><span class="sxs-lookup"><span data-stu-id="381a1-108">To add a system disk, specify an operating system type by using the *OS* parameter.</span></span>

## <span data-ttu-id="381a1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="381a1-109">EXAMPLES</span></span>

### <span data-ttu-id="381a1-110">Beispiel 1: Hinzufügen einer Startdiskette, die das Windows-Betriebssystem verwendet</span><span class="sxs-lookup"><span data-stu-id="381a1-110">Example 1: Add a startup disk that uses the Windows operating system</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyWinDisk" -MediaLocation "http://contosostorage.blob.core.azure.com/vhds/winserver-system.vhd" -Label "StartupDisk" -OS "Windows"
```

<span data-ttu-id="381a1-111">Mit diesem Befehl wird dem Datenträger-Repository ein Systemdatenträger hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="381a1-111">This command adds a system disk to your disk repository.</span></span>
<span data-ttu-id="381a1-112">Auf dem Systemdatenträger wird das Windows-Betriebssystem verwendet.</span><span class="sxs-lookup"><span data-stu-id="381a1-112">The system disk uses the Windows operating system.</span></span>

### <span data-ttu-id="381a1-113">Beispiel 2: Hinzufügen eines Daten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="381a1-113">Example 2: Add a data disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyDataDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/winserver-data.vhd" -Label "DataDisk"
```

<span data-ttu-id="381a1-114">Mit diesem Befehl wird ein Daten Datenträger hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="381a1-114">This command adds a data disk.</span></span>

### <span data-ttu-id="381a1-115">Beispiel 3: Hinzufügen eines Linux-Systemdatenträgers</span><span class="sxs-lookup"><span data-stu-id="381a1-115">Example 3: Add a Linux system disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyLinuxDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/linuxsys.vhd" -OS "Linux"
```

<span data-ttu-id="381a1-116">Mit diesem Befehl wird ein Linux-Systemdatenträger hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="381a1-116">This command adds a Linux system disk.</span></span>

## <span data-ttu-id="381a1-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="381a1-117">PARAMETERS</span></span>

### <span data-ttu-id="381a1-118">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="381a1-118">-DiskName</span></span>
<span data-ttu-id="381a1-119">Gibt den Namen des Datenträgers an, der vom Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="381a1-119">Specifies the name of the disk that this cmdlet adds.</span></span>

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

### <span data-ttu-id="381a1-120">-Information</span><span class="sxs-lookup"><span data-stu-id="381a1-120">-InformationAction</span></span>
<span data-ttu-id="381a1-121">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="381a1-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="381a1-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="381a1-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="381a1-123">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="381a1-123">Continue</span></span>
- <span data-ttu-id="381a1-124">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="381a1-124">Ignore</span></span>
- <span data-ttu-id="381a1-125">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="381a1-125">Inquire</span></span>
- <span data-ttu-id="381a1-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="381a1-126">SilentlyContinue</span></span>
- <span data-ttu-id="381a1-127">Beenden</span><span class="sxs-lookup"><span data-stu-id="381a1-127">Stop</span></span>
- <span data-ttu-id="381a1-128">Anhalten</span><span class="sxs-lookup"><span data-stu-id="381a1-128">Suspend</span></span>

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

### <span data-ttu-id="381a1-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="381a1-129">-InformationVariable</span></span>
<span data-ttu-id="381a1-130">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="381a1-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="381a1-131">-Label</span><span class="sxs-lookup"><span data-stu-id="381a1-131">-Label</span></span>
<span data-ttu-id="381a1-132">Gibt eine Datenträgerbeschriftung für den Datenträger an, den dieses Cmdlet hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="381a1-132">Specifies a disk label for the disk that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381a1-133">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="381a1-133">-MediaLocation</span></span>
<span data-ttu-id="381a1-134">Gibt den physikalischen Speicherort des Datenträgers im Azure-Speicher an.</span><span class="sxs-lookup"><span data-stu-id="381a1-134">Specifies the physical location of the disk in Azure Storage.</span></span>
<span data-ttu-id="381a1-135">Dieser Wert bezieht sich auf eine BLOB-Seite im aktuellen Abonnement-und Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="381a1-135">This value refers to a blob page in the current subscription and storage account.</span></span>

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

### <span data-ttu-id="381a1-136">-OS</span><span class="sxs-lookup"><span data-stu-id="381a1-136">-OS</span></span>
<span data-ttu-id="381a1-137">Gibt den Typ des Betriebssystems für einen Systemdatenträger an.</span><span class="sxs-lookup"><span data-stu-id="381a1-137">Specifies the operating system type for a system disk.</span></span>
<span data-ttu-id="381a1-138">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="381a1-138">Valid values are:</span></span> 

- <span data-ttu-id="381a1-139">Windows</span><span class="sxs-lookup"><span data-stu-id="381a1-139">Windows</span></span> 
- <span data-ttu-id="381a1-140">Linux</span><span class="sxs-lookup"><span data-stu-id="381a1-140">Linux</span></span> 

<span data-ttu-id="381a1-141">Wenn Sie diesen Parameter nicht angeben, fügt das Cmdlet den Datenträger als Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="381a1-141">If you do not specify this parameter, the cmdlet adds the disk as a data disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381a1-142">-Profil</span><span class="sxs-lookup"><span data-stu-id="381a1-142">-Profile</span></span>
<span data-ttu-id="381a1-143">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="381a1-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="381a1-144">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="381a1-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="381a1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="381a1-145">CommonParameters</span></span>
<span data-ttu-id="381a1-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="381a1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="381a1-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="381a1-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="381a1-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="381a1-148">INPUTS</span></span>

## <span data-ttu-id="381a1-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="381a1-149">OUTPUTS</span></span>

### <span data-ttu-id="381a1-150">Daten trägercontext</span><span class="sxs-lookup"><span data-stu-id="381a1-150">DiskContext</span></span>

## <span data-ttu-id="381a1-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="381a1-151">NOTES</span></span>

## <span data-ttu-id="381a1-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="381a1-152">RELATED LINKS</span></span>

[<span data-ttu-id="381a1-153">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="381a1-153">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="381a1-154">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="381a1-154">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="381a1-155">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="381a1-155">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


