---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 849714BC-8B19-453E-B790-A9C38F9D48CB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ef8bd3b1fef6a3af01193a104f6917c4131064f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005631"
---
# <span data-ttu-id="1e56b-101">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="1e56b-101">Update-AzureDisk</span></span>

## <span data-ttu-id="1e56b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e56b-102">SYNOPSIS</span></span>
<span data-ttu-id="1e56b-103">Ändert die Beschriftung eines Datenträgers im Azure Disk Repository.</span><span class="sxs-lookup"><span data-stu-id="1e56b-103">Changes the label of a disk in the Azure disk repository.</span></span>

## <span data-ttu-id="1e56b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e56b-104">SYNTAX</span></span>

### <span data-ttu-id="1e56b-105">Größe</span><span class="sxs-lookup"><span data-stu-id="1e56b-105">Resize</span></span>
```
Update-AzureDisk [-DiskName] <String> [[-Label] <String>] [-ResizedSizeInGB] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e56b-106">NORESIZE</span><span class="sxs-lookup"><span data-stu-id="1e56b-106">NoResize</span></span>
```
Update-AzureDisk [-DiskName] <String> [-Label] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1e56b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e56b-107">DESCRIPTION</span></span>
<span data-ttu-id="1e56b-108">Das Cmdlet **Update-AzureDisk** ändert die Beschriftung, die einem Datenträger im Datenträger-Repository des aktuellen Azure-Abonnements zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1e56b-108">The **Update-AzureDisk** cmdlet changes the label that is associated with a disk in the disk repository of the current Azure subscription.</span></span>

## <span data-ttu-id="1e56b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e56b-109">EXAMPLES</span></span>

### <span data-ttu-id="1e56b-110">Beispiel 1: Ändern der Bezeichnung eines Datenträgers</span><span class="sxs-lookup"><span data-stu-id="1e56b-110">Example 1: Change the label of a disk</span></span>
```
PS C:\> Update-AzureDisk ?DiskName "ContosoOSDisk" -Label "DoNotUse"
```

<span data-ttu-id="1e56b-111">Dieser Befehl ändert die Beschriftung des Datenträgers mit dem Namen ContosoOSDisk in DoNotUse.</span><span class="sxs-lookup"><span data-stu-id="1e56b-111">This command changes the label of the disk named ContosoOSDisk to DoNotUse.</span></span>

## <span data-ttu-id="1e56b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e56b-112">PARAMETERS</span></span>

### <span data-ttu-id="1e56b-113">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="1e56b-113">-DiskName</span></span>
<span data-ttu-id="1e56b-114">Gibt den Namen des Datenträgers an, der von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="1e56b-114">Specifies the name of the disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1e56b-115">-Information</span><span class="sxs-lookup"><span data-stu-id="1e56b-115">-InformationAction</span></span>
<span data-ttu-id="1e56b-116">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="1e56b-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1e56b-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1e56b-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e56b-118">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="1e56b-118">Continue</span></span>
- <span data-ttu-id="1e56b-119">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="1e56b-119">Ignore</span></span>
- <span data-ttu-id="1e56b-120">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="1e56b-120">Inquire</span></span>
- <span data-ttu-id="1e56b-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1e56b-121">SilentlyContinue</span></span>
- <span data-ttu-id="1e56b-122">Beenden</span><span class="sxs-lookup"><span data-stu-id="1e56b-122">Stop</span></span>
- <span data-ttu-id="1e56b-123">Anhalten</span><span class="sxs-lookup"><span data-stu-id="1e56b-123">Suspend</span></span>

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

### <span data-ttu-id="1e56b-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1e56b-124">-InformationVariable</span></span>
<span data-ttu-id="1e56b-125">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="1e56b-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1e56b-126">-Label</span><span class="sxs-lookup"><span data-stu-id="1e56b-126">-Label</span></span>
<span data-ttu-id="1e56b-127">Gibt die neue Bezeichnung für den Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="1e56b-127">Specifies the new label for the disk.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoResize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e56b-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="1e56b-128">-Profile</span></span>
<span data-ttu-id="1e56b-129">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="1e56b-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1e56b-130">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="1e56b-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1e56b-131">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="1e56b-131">-ResizedSizeInGB</span></span>
<span data-ttu-id="1e56b-132">Gibt die neue Größe in Gigabyte für den Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="1e56b-132">Specifies the new size, in gigabytes, for the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e56b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e56b-133">CommonParameters</span></span>
<span data-ttu-id="1e56b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e56b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e56b-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e56b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e56b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e56b-136">INPUTS</span></span>

## <span data-ttu-id="1e56b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e56b-137">OUTPUTS</span></span>

### <span data-ttu-id="1e56b-138">Daten trägercontext</span><span class="sxs-lookup"><span data-stu-id="1e56b-138">DiskContext</span></span>

## <span data-ttu-id="1e56b-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e56b-139">NOTES</span></span>

## <span data-ttu-id="1e56b-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e56b-140">RELATED LINKS</span></span>

[<span data-ttu-id="1e56b-141">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="1e56b-141">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="1e56b-142">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="1e56b-142">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="1e56b-143">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="1e56b-143">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)


