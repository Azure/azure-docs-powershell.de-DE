---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: ABF5B4EB-0908-4103-B0BF-69A68A21D69C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 296a37d00c97bc3af849886593e09a1a0a9ff863
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007573"
---
# <span data-ttu-id="0b062-101">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="0b062-101">Suspend-WAPackVM</span></span>

## <span data-ttu-id="0b062-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b062-102">SYNOPSIS</span></span>
<span data-ttu-id="0b062-103">Unterbricht einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="0b062-103">Suspends a virtual machine.</span></span>

## <span data-ttu-id="0b062-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b062-104">SYNTAX</span></span>

```
Suspend-WAPackVM -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0b062-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b062-105">DESCRIPTION</span></span>
<span data-ttu-id="0b062-106">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b062-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="0b062-107">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0b062-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0b062-108">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0b062-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0b062-109">Das Cmdlet **Suspend-WAPackVM** unterbricht einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="0b062-109">The **Suspend-WAPackVM** cmdlet suspends a virtual machine.</span></span>

## <span data-ttu-id="0b062-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b062-110">EXAMPLES</span></span>

### <span data-ttu-id="0b062-111">Beispiel 1: Anhalten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="0b062-111">Example 1: Suspend a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Suspend-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="0b062-112">Der erste Befehl ruft den virtuellen Computer mit dem Namen ContosoV126 mit dem Cmdlet **Get-WAPackVM** ab und speichert dieses Objekt dann in der $VirtualMachine Variablen.</span><span class="sxs-lookup"><span data-stu-id="0b062-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="0b062-113">Der zweite Befehl unterbricht den virtuellen Computer, der in $VirtualMachine gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="0b062-113">The second command suspends the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="0b062-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b062-114">PARAMETERS</span></span>

### <span data-ttu-id="0b062-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b062-115">-PassThru</span></span>
<span data-ttu-id="0b062-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="0b062-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0b062-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="0b062-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0b062-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="0b062-118">-Profile</span></span>
<span data-ttu-id="0b062-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0b062-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0b062-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0b062-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0b062-121">-VM</span><span class="sxs-lookup"><span data-stu-id="0b062-121">-VM</span></span>
<span data-ttu-id="0b062-122">Gibt einen virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="0b062-122">Specifies a virtual machine.</span></span>
<span data-ttu-id="0b062-123">Verwenden Sie zum Abrufen eines virtuellen Computers das Cmdlet **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="0b062-123">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="0b062-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b062-124">CommonParameters</span></span>
<span data-ttu-id="0b062-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b062-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b062-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b062-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b062-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b062-127">INPUTS</span></span>

## <span data-ttu-id="0b062-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b062-128">OUTPUTS</span></span>

## <span data-ttu-id="0b062-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b062-129">NOTES</span></span>

## <span data-ttu-id="0b062-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b062-130">RELATED LINKS</span></span>

[<span data-ttu-id="0b062-131">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="0b062-131">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="0b062-132">Neu – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="0b062-132">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="0b062-133">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="0b062-133">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="0b062-134">Neustart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="0b062-134">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="0b062-135">Lebenslauf-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="0b062-135">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="0b062-136">Satz-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="0b062-136">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="0b062-137">Anfang-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="0b062-137">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="0b062-138">Stopp-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="0b062-138">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)


