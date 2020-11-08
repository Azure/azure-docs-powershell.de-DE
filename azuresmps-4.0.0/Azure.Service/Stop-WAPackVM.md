---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4FB7096E-DDA1-474C-BF0C-D910681BE58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e4ef4660761ab29e738050c0445534602accda6
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007602"
---
# <span data-ttu-id="2f9fa-101">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="2f9fa-101">Stop-WAPackVM</span></span>

## <span data-ttu-id="2f9fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f9fa-102">SYNOPSIS</span></span>
<span data-ttu-id="2f9fa-103">Beendet einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="2f9fa-103">Stops a virtual machine.</span></span>

## <span data-ttu-id="2f9fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f9fa-104">SYNTAX</span></span>

```
Stop-WAPackVM [-Shutdown] -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2f9fa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f9fa-105">DESCRIPTION</span></span>
<span data-ttu-id="2f9fa-106">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="2f9fa-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="2f9fa-107">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2f9fa-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2f9fa-108">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2f9fa-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2f9fa-109">Das Cmdlet **Stop-WAPackVM** beendet einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="2f9fa-109">The **Stop-WAPackVM** cmdlet stops a virtual machine.</span></span>

## <span data-ttu-id="2f9fa-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f9fa-110">EXAMPLES</span></span>

### <span data-ttu-id="2f9fa-111">Beispiel 1: Beenden eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="2f9fa-111">Example 1: Stop a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Stop-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="2f9fa-112">Der erste Befehl ruft den virtuellen Computer mit dem Namen ContosoV126 mit dem Cmdlet **Get-WAPackVM** ab und speichert dieses Objekt dann in der $VirtualMachine Variablen.</span><span class="sxs-lookup"><span data-stu-id="2f9fa-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="2f9fa-113">Der zweite Befehl beendet den virtuellen Computer, der in $VirtualMachine gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="2f9fa-113">The second command stops the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="2f9fa-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f9fa-114">PARAMETERS</span></span>

### <span data-ttu-id="2f9fa-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f9fa-115">-PassThru</span></span>
<span data-ttu-id="2f9fa-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2f9fa-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2f9fa-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="2f9fa-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2f9fa-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="2f9fa-118">-Profile</span></span>
<span data-ttu-id="2f9fa-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="2f9fa-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2f9fa-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="2f9fa-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2f9fa-121">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="2f9fa-121">-Shutdown</span></span>
<span data-ttu-id="2f9fa-122">Gibt an, dass das Cmdlet das Betriebssystem des virtuellen Computers herunterfährt.</span><span class="sxs-lookup"><span data-stu-id="2f9fa-122">Indicates that the cmdlet shuts down the operating system of the virtual machine.</span></span>

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

### <span data-ttu-id="2f9fa-123">-VM</span><span class="sxs-lookup"><span data-stu-id="2f9fa-123">-VM</span></span>
<span data-ttu-id="2f9fa-124">Gibt einen virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="2f9fa-124">Specifies a virtual machine.</span></span>
<span data-ttu-id="2f9fa-125">Verwenden Sie zum Abrufen eines virtuellen Computers das Cmdlet **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="2f9fa-125">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="2f9fa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f9fa-126">CommonParameters</span></span>
<span data-ttu-id="2f9fa-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f9fa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f9fa-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f9fa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f9fa-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f9fa-129">INPUTS</span></span>

## <span data-ttu-id="2f9fa-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f9fa-130">OUTPUTS</span></span>

## <span data-ttu-id="2f9fa-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f9fa-131">NOTES</span></span>

## <span data-ttu-id="2f9fa-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f9fa-132">RELATED LINKS</span></span>

[<span data-ttu-id="2f9fa-133">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="2f9fa-133">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="2f9fa-134">Neu – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="2f9fa-134">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="2f9fa-135">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="2f9fa-135">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="2f9fa-136">Neustart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="2f9fa-136">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="2f9fa-137">Lebenslauf-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="2f9fa-137">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="2f9fa-138">Satz-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="2f9fa-138">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="2f9fa-139">Anfang-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="2f9fa-139">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="2f9fa-140">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="2f9fa-140">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


