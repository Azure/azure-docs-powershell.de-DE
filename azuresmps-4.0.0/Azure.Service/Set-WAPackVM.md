---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 08A7556E-C07F-4B3B-B9D6-B241C72860FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: b01ac318982b62499164cd54c9d9a51356ad9830
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007591"
---
# <span data-ttu-id="ffe7e-101">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ffe7e-101">Set-WAPackVM</span></span>

## <span data-ttu-id="ffe7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ffe7e-102">SYNOPSIS</span></span>
<span data-ttu-id="ffe7e-103">Ändert die Größeneigenschaften einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-103">Changes the size properties of a virtual machine.</span></span>

## <span data-ttu-id="ffe7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffe7e-104">SYNTAX</span></span>

```
Set-WAPackVM -VM <VirtualMachine> -VMSizeProfile <HardwareProfile> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ffe7e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ffe7e-105">DESCRIPTION</span></span>
<span data-ttu-id="ffe7e-106">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="ffe7e-107">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ffe7e-108">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ffe7e-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ffe7e-109">Das Cmdlet " **Satz-WAPackVM** " ändert die Größeneigenschaften einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-109">The **Set-WAPackVM** cmdlet changes the size properties of a virtual machine.</span></span>

## <span data-ttu-id="ffe7e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ffe7e-110">EXAMPLES</span></span>

### <span data-ttu-id="ffe7e-111">Beispiel 1: Angeben der Größe für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="ffe7e-111">Example 1: Specify the size for a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> Set-WAPackVM -VM $VirtualMachine -VMSizeProfile $SizeProfile
```

<span data-ttu-id="ffe7e-112">Der erste Befehl ruft den virtuellen Computer mit dem Namen ContosoV126 mit dem Cmdlet **Get-WAPackVM** ab und speichert dieses Objekt dann in der $VirtualMachine Variablen.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="ffe7e-113">Der zweite Befehl ruft das size-Profil mit dem Namen MediumSizeVM mit dem Cmdlet **Get-WAPackVMSizeProfile** ab und speichert dieses Objekt dann in der $SizeProfile Variablen.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-113">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores that object in the $SizeProfile variable.</span></span>

<span data-ttu-id="ffe7e-114">Der endgültige Befehl weist das in $SizeProfile gespeicherte Größen Profil dem in $VirtualMachine gespeicherten virtuellen Computer zu.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-114">The final command assigns the size profile stored in $SizeProfile to the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="ffe7e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffe7e-115">PARAMETERS</span></span>

### <span data-ttu-id="ffe7e-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ffe7e-116">-PassThru</span></span>
<span data-ttu-id="ffe7e-117">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ffe7e-118">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ffe7e-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="ffe7e-119">-Profile</span></span>
<span data-ttu-id="ffe7e-120">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ffe7e-121">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ffe7e-122">-VM</span><span class="sxs-lookup"><span data-stu-id="ffe7e-122">-VM</span></span>
<span data-ttu-id="ffe7e-123">Gibt einen virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-123">Specifies a virtual machine.</span></span>
<span data-ttu-id="ffe7e-124">Verwenden Sie zum Abrufen eines virtuellen Computers das Cmdlet **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="ffe7e-124">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

```yaml
Type: VirtualMachine
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffe7e-125">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="ffe7e-125">-VMSizeProfile</span></span>
<span data-ttu-id="ffe7e-126">Gibt ein Größen Profil für einen virtuellen Computer als **Hardwareprofile** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-126">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="ffe7e-127">Um ein Größen Profil zu erhalten, verwenden Sie das Cmdlet **Get-WAPackVMSizeProfile** .</span><span class="sxs-lookup"><span data-stu-id="ffe7e-127">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe7e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffe7e-128">CommonParameters</span></span>
<span data-ttu-id="ffe7e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffe7e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffe7e-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffe7e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffe7e-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ffe7e-131">INPUTS</span></span>

## <span data-ttu-id="ffe7e-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ffe7e-132">OUTPUTS</span></span>

## <span data-ttu-id="ffe7e-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="ffe7e-133">NOTES</span></span>

## <span data-ttu-id="ffe7e-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ffe7e-134">RELATED LINKS</span></span>

[<span data-ttu-id="ffe7e-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ffe7e-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="ffe7e-136">Neu – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ffe7e-136">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="ffe7e-137">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ffe7e-137">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="ffe7e-138">Neustart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ffe7e-138">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="ffe7e-139">Lebenslauf-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ffe7e-139">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="ffe7e-140">Anfang-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ffe7e-140">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="ffe7e-141">Stopp-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ffe7e-141">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="ffe7e-142">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ffe7e-142">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="ffe7e-143">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="ffe7e-143">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)


