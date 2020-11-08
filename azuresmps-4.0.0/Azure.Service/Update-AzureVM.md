---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8DC10708-09CE-449C-BE20-1E9E49CCE08A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55d9879d6e6768bf3ad409c84a4fc1052d58d8b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006219"
---
# <span data-ttu-id="fcfd1-101">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fcfd1-101">Update-AzureVM</span></span>

## <span data-ttu-id="fcfd1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fcfd1-102">SYNOPSIS</span></span>
<span data-ttu-id="fcfd1-103">Ändert die Konfiguration eines Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="fcfd1-103">Modifies the configuration of an Azure virtual machine.</span></span>

## <span data-ttu-id="fcfd1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcfd1-104">SYNTAX</span></span>

```
Update-AzureVM [-Name] <String> -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fcfd1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fcfd1-105">DESCRIPTION</span></span>
<span data-ttu-id="fcfd1-106">Das Cmdlet **Update-AzureVM** akzeptiert Update Informationen für den angegebenen virtuellen Computer und initiiert das Update.</span><span class="sxs-lookup"><span data-stu-id="fcfd1-106">The **Update-AzureVM** cmdlet accepts update information for the specified virtual machine and initiates the update.</span></span>
<span data-ttu-id="fcfd1-107">Sie können Datenlaufwerke hinzufügen oder entfernen, den Cachemodus von Daten-oder Betriebssystemdatenträgern ändern, die Netzwerkendpunkte ändern oder die Größe des virtuellen Computers ändern.</span><span class="sxs-lookup"><span data-stu-id="fcfd1-107">You can add or remove data disks, modify the cache mode of data or operating system disks, change the network endpoints, or change the size of the virtual machine.</span></span>

## <span data-ttu-id="fcfd1-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fcfd1-108">EXAMPLES</span></span>

### <span data-ttu-id="fcfd1-109">Beispiel 1: Aktualisieren der Größe eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="fcfd1-109">Example 1: Update the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" | Set-AzureVMSize -InstanceSize "Medium" | Update-AzureVM
```

<span data-ttu-id="fcfd1-110">Mit diesem Befehl wird die Größe des virtuellen Computers mit dem Namen VirtualMachine04 geändert, der im Dienst mit dem Namen ContosoService03 auf Mittel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fcfd1-110">This command changes the size of the virtual machine named VirtualMachine04, running in the service named ContosoService03, to Medium.</span></span>

### <span data-ttu-id="fcfd1-111">Beispiel 2: Hinzufügen eines Datenlaufwerks zu einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="fcfd1-111">Example 2: Add a data disk to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine05" | Add-AzureDataDisk -CreateNew -MediaLocation "https://ContosoStore1.blob.core.azure.com/vhds/Disk22.vhd" -DiskSizeInGB 128 -DiskLabel "Data-128" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="fcfd1-112">Dieser Befehl fügt dem virtuellen Computer mit dem Namen VirtualMachine05 einen neuen Daten Datenträger hinzu, der im Dienst mit dem Namen ContosoService03 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fcfd1-112">This command adds a new data disk to the virtual machine named VirtualMachine05, running in the service named ContosoService03.</span></span>

## <span data-ttu-id="fcfd1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcfd1-113">PARAMETERS</span></span>

### <span data-ttu-id="fcfd1-114">-Information</span><span class="sxs-lookup"><span data-stu-id="fcfd1-114">-InformationAction</span></span>
<span data-ttu-id="fcfd1-115">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="fcfd1-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fcfd1-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fcfd1-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fcfd1-117">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="fcfd1-117">Continue</span></span>
- <span data-ttu-id="fcfd1-118">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="fcfd1-118">Ignore</span></span>
- <span data-ttu-id="fcfd1-119">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="fcfd1-119">Inquire</span></span>
- <span data-ttu-id="fcfd1-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fcfd1-120">SilentlyContinue</span></span>
- <span data-ttu-id="fcfd1-121">Beenden</span><span class="sxs-lookup"><span data-stu-id="fcfd1-121">Stop</span></span>
- <span data-ttu-id="fcfd1-122">Anhalten</span><span class="sxs-lookup"><span data-stu-id="fcfd1-122">Suspend</span></span>

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

### <span data-ttu-id="fcfd1-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fcfd1-123">-InformationVariable</span></span>
<span data-ttu-id="fcfd1-124">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="fcfd1-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fcfd1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fcfd1-125">-Name</span></span>
<span data-ttu-id="fcfd1-126">Gibt den Namen der zu aktualisierende virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="fcfd1-126">Specifies the name of the virtual machine to update.</span></span>

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

### <span data-ttu-id="fcfd1-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="fcfd1-127">-Profile</span></span>
<span data-ttu-id="fcfd1-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="fcfd1-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fcfd1-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="fcfd1-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fcfd1-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fcfd1-130">-ServiceName</span></span>
<span data-ttu-id="fcfd1-131">Gibt den Namen des Azure-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="fcfd1-131">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="fcfd1-132">-VM</span><span class="sxs-lookup"><span data-stu-id="fcfd1-132">-VM</span></span>
<span data-ttu-id="fcfd1-133">Gibt das Objekt des virtuellen Computers an, das aktualisierte Einstellungen enthält.</span><span class="sxs-lookup"><span data-stu-id="fcfd1-133">Specifies the virtual machine object that includes updated settings.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcfd1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcfd1-134">CommonParameters</span></span>
<span data-ttu-id="fcfd1-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcfd1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcfd1-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcfd1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcfd1-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fcfd1-137">INPUTS</span></span>

## <span data-ttu-id="fcfd1-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fcfd1-138">OUTPUTS</span></span>

## <span data-ttu-id="fcfd1-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="fcfd1-139">NOTES</span></span>

## <span data-ttu-id="fcfd1-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fcfd1-140">RELATED LINKS</span></span>

[<span data-ttu-id="fcfd1-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fcfd1-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="fcfd1-142">Neu – AzureVM</span><span class="sxs-lookup"><span data-stu-id="fcfd1-142">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="fcfd1-143">Neu – AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="fcfd1-143">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="fcfd1-144">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fcfd1-144">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="fcfd1-145">Neustart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fcfd1-145">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="fcfd1-146">Satz-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="fcfd1-146">Set-AzureVMSize</span></span>](./Set-AzureVMSize.md)

[<span data-ttu-id="fcfd1-147">Anfang-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fcfd1-147">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="fcfd1-148">Stopp-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fcfd1-148">Stop-AzureVM</span></span>](./Stop-AzureVM.md)


