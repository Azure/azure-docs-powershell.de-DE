---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 80820C11-92BB-4E75-8722-496CF21C779E
online version: ''
schema: 2.0.0
ms.openlocfilehash: a92ff041f5a3eb245b76501e7758ca62b24887f9
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007593"
---
# <span data-ttu-id="f849c-101">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f849c-101">Restart-WAPackVM</span></span>

## <span data-ttu-id="f849c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f849c-102">SYNOPSIS</span></span>
<span data-ttu-id="f849c-103">Startet virtuelle Computer neu.</span><span class="sxs-lookup"><span data-stu-id="f849c-103">Restarts virtual machines.</span></span>

## <span data-ttu-id="f849c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f849c-104">SYNTAX</span></span>

```
Restart-WAPackVM -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f849c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f849c-105">DESCRIPTION</span></span>
<span data-ttu-id="f849c-106">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="f849c-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="f849c-107">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f849c-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f849c-108">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f849c-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f849c-109">Mit dem Cmdlet " **Restart-WAPackVM** " werden virtuelle Computer neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="f849c-109">The **Restart-WAPackVM** cmdlet restarts virtual machines.</span></span>

## <span data-ttu-id="f849c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f849c-110">EXAMPLES</span></span>

### <span data-ttu-id="f849c-111">Beispiel 1: Erneutes Starten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="f849c-111">Example 1: Restart a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Restart-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="f849c-112">Der erste Befehl ruft den virtuellen Computer mit dem Namen ContosoV126 mit dem Cmdlet **Get-WAPackVM** ab und speichert dieses Objekt dann in der $VirtualMachine Variablen.</span><span class="sxs-lookup"><span data-stu-id="f849c-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="f849c-113">Der zweite Befehl startet den in $VirtualMachine gespeicherten virtuellen Computer neu.</span><span class="sxs-lookup"><span data-stu-id="f849c-113">The second command restarts the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="f849c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f849c-114">PARAMETERS</span></span>

### <span data-ttu-id="f849c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f849c-115">-PassThru</span></span>
<span data-ttu-id="f849c-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f849c-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f849c-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="f849c-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f849c-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="f849c-118">-Profile</span></span>
<span data-ttu-id="f849c-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="f849c-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f849c-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f849c-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f849c-121">-VM</span><span class="sxs-lookup"><span data-stu-id="f849c-121">-VM</span></span>
<span data-ttu-id="f849c-122">Gibt einen virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="f849c-122">Specifies a virtual machine.</span></span>
<span data-ttu-id="f849c-123">Verwenden Sie zum Abrufen eines virtuellen Computers das Cmdlet **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="f849c-123">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="f849c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f849c-124">CommonParameters</span></span>
<span data-ttu-id="f849c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f849c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f849c-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f849c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f849c-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f849c-127">INPUTS</span></span>

## <span data-ttu-id="f849c-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f849c-128">OUTPUTS</span></span>

## <span data-ttu-id="f849c-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="f849c-129">NOTES</span></span>

## <span data-ttu-id="f849c-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f849c-130">RELATED LINKS</span></span>

[<span data-ttu-id="f849c-131">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f849c-131">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="f849c-132">Neu – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f849c-132">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="f849c-133">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f849c-133">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="f849c-134">Lebenslauf-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f849c-134">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="f849c-135">Satz-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f849c-135">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="f849c-136">Anfang-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f849c-136">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="f849c-137">Stopp-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f849c-137">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="f849c-138">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f849c-138">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


