---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2A8BE3EB-4929-4B40-82EA-5434C09A5251
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1974de3f5c4bf39aa32100e67bb04642ebcfe3da
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005857"
---
# <span data-ttu-id="31d14-101">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="31d14-101">Get-AzureDataDisk</span></span>

## <span data-ttu-id="31d14-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31d14-102">SYNOPSIS</span></span>
<span data-ttu-id="31d14-103">Ruft Azure-Daten Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="31d14-103">Gets Azure data disks.</span></span>

## <span data-ttu-id="31d14-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31d14-104">SYNTAX</span></span>

```
Get-AzureDataDisk [[-Lun] <Int32>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="31d14-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31d14-105">DESCRIPTION</span></span>
<span data-ttu-id="31d14-106">Das Cmdlet " **Get-AzureDataDisk** " Ruft ein Objekt ab, das die Datenlaufwerke auf einem Azure Virtual Machine darstellt.</span><span class="sxs-lookup"><span data-stu-id="31d14-106">The **Get-AzureDataDisk** cmdlet gets an object that represents the data disks on an Azure virtual machine.</span></span>
<span data-ttu-id="31d14-107">Wenn Sie ein bestimmtes Daten Datenträgerobjekt abrufen möchten, geben Sie die logische Einheitsnummer (LUN) des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="31d14-107">To get a specific data disk object, specify the logical unit number (LUN) of the disk.</span></span>

## <span data-ttu-id="31d14-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31d14-108">EXAMPLES</span></span>

### <span data-ttu-id="31d14-109">Beispiel 1: Abrufen aller Datenlaufwerke für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="31d14-109">Example 1: Get all data disks for a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk
```

<span data-ttu-id="31d14-110">Dieser Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 im Dienst ContosoService mit dem Cmdlet **Get-AzureVM** ab.</span><span class="sxs-lookup"><span data-stu-id="31d14-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="31d14-111">Der Befehl übergibt den virtuellen Computer mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31d14-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="31d14-112">Das aktuelle Cmdlet ruft alle Datenlaufwerke für diesen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="31d14-112">The current cmdlet gets all the data disks for this virtual machine.</span></span>

### <span data-ttu-id="31d14-113">Beispiel 2: Abrufen einer bestimmten Datendiskette für ein vituralvirtual-machinevirtual</span><span class="sxs-lookup"><span data-stu-id="31d14-113">Example 2: Get a specific data disk for a vituralvirtual machinevirtual</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk -LUN 2
```

<span data-ttu-id="31d14-114">Dieser Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 im Dienst mit dem Namen ContosoService.</span><span class="sxs-lookup"><span data-stu-id="31d14-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="31d14-115">Der Befehl übergibt den virtuellen Computer an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31d14-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="31d14-116">Das aktuelle Cmdlet ruft den Datenträger mit der LUN 2 ab.</span><span class="sxs-lookup"><span data-stu-id="31d14-116">The current cmdlet gets the data disk that has the LUN 2.</span></span>

## <span data-ttu-id="31d14-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="31d14-117">PARAMETERS</span></span>

### <span data-ttu-id="31d14-118">-Information</span><span class="sxs-lookup"><span data-stu-id="31d14-118">-InformationAction</span></span>
<span data-ttu-id="31d14-119">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="31d14-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="31d14-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="31d14-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="31d14-121">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="31d14-121">Continue</span></span>
- <span data-ttu-id="31d14-122">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="31d14-122">Ignore</span></span>
- <span data-ttu-id="31d14-123">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="31d14-123">Inquire</span></span>
- <span data-ttu-id="31d14-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="31d14-124">SilentlyContinue</span></span>
- <span data-ttu-id="31d14-125">Beenden</span><span class="sxs-lookup"><span data-stu-id="31d14-125">Stop</span></span>
- <span data-ttu-id="31d14-126">Anhalten</span><span class="sxs-lookup"><span data-stu-id="31d14-126">Suspend</span></span>

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

### <span data-ttu-id="31d14-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="31d14-127">-InformationVariable</span></span>
<span data-ttu-id="31d14-128">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="31d14-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="31d14-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="31d14-129">-Lun</span></span>
<span data-ttu-id="31d14-130">Gibt die LUN für das Datenlaufwerk auf dem virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="31d14-130">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="31d14-131">Gültige Werte sind: 0 bis 15.</span><span class="sxs-lookup"><span data-stu-id="31d14-131">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31d14-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="31d14-132">-Profile</span></span>
<span data-ttu-id="31d14-133">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="31d14-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="31d14-134">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="31d14-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="31d14-135">-VM</span><span class="sxs-lookup"><span data-stu-id="31d14-135">-VM</span></span>
<span data-ttu-id="31d14-136">Gibt das Objekt des virtuellen Computers an, für das dieses Cmdlet Datenlaufwerke erhält.</span><span class="sxs-lookup"><span data-stu-id="31d14-136">Specifies the virtual machine object for which this cmdlet gets data disks.</span></span>
<span data-ttu-id="31d14-137">Verwenden Sie das Cmdlet **Get-AzureVM** , um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="31d14-137">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31d14-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31d14-138">CommonParameters</span></span>
<span data-ttu-id="31d14-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31d14-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31d14-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31d14-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31d14-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31d14-141">INPUTS</span></span>

## <span data-ttu-id="31d14-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31d14-142">OUTPUTS</span></span>

## <span data-ttu-id="31d14-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="31d14-143">NOTES</span></span>

## <span data-ttu-id="31d14-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31d14-144">RELATED LINKS</span></span>

[<span data-ttu-id="31d14-145">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="31d14-145">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="31d14-146">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="31d14-146">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="31d14-147">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="31d14-147">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="31d14-148">Satz-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="31d14-148">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)


