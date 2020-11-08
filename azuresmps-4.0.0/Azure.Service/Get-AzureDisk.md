---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006560"
---
# <span data-ttu-id="0512b-101">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="0512b-101">Get-AzureDisk</span></span>

## <span data-ttu-id="0512b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0512b-102">SYNOPSIS</span></span>
<span data-ttu-id="0512b-103">Ruft Informationen zu Datenträgern im Azure Disk Repository ab.</span><span class="sxs-lookup"><span data-stu-id="0512b-103">Gets information about disks in the Azure disk repository.</span></span>

## <span data-ttu-id="0512b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0512b-104">SYNTAX</span></span>

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0512b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0512b-105">DESCRIPTION</span></span>
<span data-ttu-id="0512b-106">Das Cmdlet " **Get-AzureDisk** " Ruft Informationen zu den Datenträgern ab, die im Azure Disk Repository für das aktuelle Abonnement gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="0512b-106">The **Get-AzureDisk** cmdlet gets information about the disks that are stored in the Azure disk repository for the current subscription.</span></span>
<span data-ttu-id="0512b-107">Dieses Cmdlet gibt eine Liste der Informationen für alle Datenträger im Repository zurück.</span><span class="sxs-lookup"><span data-stu-id="0512b-107">This cmdlet returns a list of information for all disks in the repository.</span></span>
<span data-ttu-id="0512b-108">Wenn Sie Informationen zu einem bestimmten Datenträger anzeigen möchten, geben Sie den Namen des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="0512b-108">To view information for a specific disk, specify the name of the disk.</span></span>

## <span data-ttu-id="0512b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0512b-109">EXAMPLES</span></span>

### <span data-ttu-id="0512b-110">Beispiel 1: Abrufen von Informationen zu einem Datenträger</span><span class="sxs-lookup"><span data-stu-id="0512b-110">Example 1: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="0512b-111">Dieser Befehl ruft Informationsdaten über den Datenträger mit dem Namen ContosoDataDisk aus dem Datenträger-Repository ab.</span><span class="sxs-lookup"><span data-stu-id="0512b-111">This command gets information data about the disk named ContosoDataDisk from the disk repository.</span></span>

### <span data-ttu-id="0512b-112">Beispiel 2: Abrufen von Informationen zu allen Datenträgern</span><span class="sxs-lookup"><span data-stu-id="0512b-112">Example 2: Get information about all disks</span></span>
```
PS C:\> Get-AzureDisk
```

<span data-ttu-id="0512b-113">Dieser Befehl ruft Informationen zu allen Datenträgern im Datenträger-Repository ab.</span><span class="sxs-lookup"><span data-stu-id="0512b-113">This command gets information about all the disks in the disk repository.</span></span>

### <span data-ttu-id="0512b-114">Beispiel 3: Abrufen von Informationen zu einem Datenträger</span><span class="sxs-lookup"><span data-stu-id="0512b-114">Example 3: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

<span data-ttu-id="0512b-115">Dieser Befehl ruft Daten für alle Datenträger im Datenträger-Repository ab, die derzeit nicht an einen virtuellen Computer angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="0512b-115">This command gets data for all of the disks in the disk repository that are not currently attached to a virtual machine.</span></span>
<span data-ttu-id="0512b-116">Der Befehl ruft Informationen zu allen Datenträgern ab und übergibt die einzelnen Objekte an das Cmdlet **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="0512b-116">The command gets information about all of the disks, and passes each object to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="0512b-117">Dieses Cmdlet löscht alle Datenträger, die keinen Wert von $NULL für die **in** -Eigenschaft aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0512b-117">That cmdlet drops any disk that does not have a value of $Null for the **AttachedTo** property.</span></span>
<span data-ttu-id="0512b-118">Der Befehl formatiert die Liste mit dem Cmdlet **Format-Table** als Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0512b-118">The command formats the list as a table by using the **Format-Table** cmdlet.</span></span>

## <span data-ttu-id="0512b-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="0512b-119">PARAMETERS</span></span>

### <span data-ttu-id="0512b-120">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="0512b-120">-DiskName</span></span>
<span data-ttu-id="0512b-121">Gibt den Namen des Datenträgers im Datenträger-Repository an, über den dieses Cmdlet Informationen erhält.</span><span class="sxs-lookup"><span data-stu-id="0512b-121">Specifies the name of the disk in the disk repository about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="0512b-122">-Information</span><span class="sxs-lookup"><span data-stu-id="0512b-122">-InformationAction</span></span>
<span data-ttu-id="0512b-123">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="0512b-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0512b-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0512b-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0512b-125">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="0512b-125">Continue</span></span>
- <span data-ttu-id="0512b-126">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="0512b-126">Ignore</span></span>
- <span data-ttu-id="0512b-127">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="0512b-127">Inquire</span></span>
- <span data-ttu-id="0512b-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0512b-128">SilentlyContinue</span></span>
- <span data-ttu-id="0512b-129">Beenden</span><span class="sxs-lookup"><span data-stu-id="0512b-129">Stop</span></span>
- <span data-ttu-id="0512b-130">Anhalten</span><span class="sxs-lookup"><span data-stu-id="0512b-130">Suspend</span></span>

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

### <span data-ttu-id="0512b-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0512b-131">-InformationVariable</span></span>
<span data-ttu-id="0512b-132">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="0512b-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0512b-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="0512b-133">-Profile</span></span>
<span data-ttu-id="0512b-134">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0512b-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0512b-135">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0512b-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0512b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0512b-136">CommonParameters</span></span>
<span data-ttu-id="0512b-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0512b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0512b-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0512b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0512b-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0512b-139">INPUTS</span></span>

## <span data-ttu-id="0512b-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0512b-140">OUTPUTS</span></span>

## <span data-ttu-id="0512b-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="0512b-141">NOTES</span></span>

## <span data-ttu-id="0512b-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0512b-142">RELATED LINKS</span></span>

[<span data-ttu-id="0512b-143">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="0512b-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="0512b-144">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="0512b-144">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="0512b-145">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="0512b-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


