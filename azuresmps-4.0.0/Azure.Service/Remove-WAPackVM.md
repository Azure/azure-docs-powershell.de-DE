---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D04D79CE-F183-4A8D-B925-F640D89377BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d7c4e6bd9365ccf45b730024b5841e4356f556a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007614"
---
# <span data-ttu-id="c935c-101">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="c935c-101">Remove-WAPackVM</span></span>

## <span data-ttu-id="c935c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c935c-102">SYNOPSIS</span></span>
<span data-ttu-id="c935c-103">Entfernt Virtual Machine-Objekte.</span><span class="sxs-lookup"><span data-stu-id="c935c-103">Removes virtual machine objects.</span></span>

## <span data-ttu-id="c935c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c935c-104">SYNTAX</span></span>

```
Remove-WAPackVM -VM <VirtualMachine> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c935c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c935c-105">DESCRIPTION</span></span>
<span data-ttu-id="c935c-106">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="c935c-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="c935c-107">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c935c-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c935c-108">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c935c-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c935c-109">Das Cmdlet **Remove-WAPackVM** entfernt virtuelle Computerobjekte.</span><span class="sxs-lookup"><span data-stu-id="c935c-109">The **Remove-WAPackVM** cmdlet removes virtual machine objects.</span></span>

## <span data-ttu-id="c935c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c935c-110">EXAMPLES</span></span>

### <span data-ttu-id="c935c-111">Beispiel 1: Entfernen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="c935c-111">Example 1: Remove a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="c935c-112">Der erste Befehl ruft den virtuellen Computer mit dem Namen ContosoV126 mit dem Cmdlet **Get-WAPackVM** ab und speichert dieses Objekt dann in der $VirtualMachine Variablen.</span><span class="sxs-lookup"><span data-stu-id="c935c-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="c935c-113">Der zweite Befehl entfernt den virtuellen Computer, der in $VirtualMachine gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="c935c-113">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="c935c-114">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="c935c-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="c935c-115">Beispiel 2: Entfernen einer virtuellen Maschine ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="c935c-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine -Force
```

<span data-ttu-id="c935c-116">Der erste Befehl ruft den virtuellen Computer mit dem Namen ContosoV126 mit dem Cmdlet **Get-WAPackVM** ab und speichert dieses Objekt dann in der $VirtualMachine Variablen.</span><span class="sxs-lookup"><span data-stu-id="c935c-116">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="c935c-117">Der zweite Befehl entfernt den virtuellen Computer, der in $VirtualMachine gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="c935c-117">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="c935c-118">Dieser Befehl enthält den Parameter *Force* .</span><span class="sxs-lookup"><span data-stu-id="c935c-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="c935c-119">Der Befehl fordert Sie nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="c935c-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c935c-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="c935c-120">PARAMETERS</span></span>

### <span data-ttu-id="c935c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c935c-121">-Force</span></span>
<span data-ttu-id="c935c-122">Gibt an, dass das Cmdlet einen virtuellen Computer entfernt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="c935c-122">Indicates that the cmdlet removes a virtual machine without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="c935c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c935c-123">-PassThru</span></span>
<span data-ttu-id="c935c-124">Gibt an, dass das Cmdlet einen booleschen Wert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c935c-124">Indicates that the cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="c935c-125">Wenn der Vorgang erfolgreich ausgeführt wird, gibt das Cmdlet den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="c935c-125">If the operation succeeds, the cmdlet returns a value of $True.</span></span>
<span data-ttu-id="c935c-126">Andernfalls wird der Wert $false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c935c-126">Otherwise, it returns a value of $False.</span></span>
<span data-ttu-id="c935c-127">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="c935c-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c935c-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="c935c-128">-Profile</span></span>
<span data-ttu-id="c935c-129">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c935c-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c935c-130">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c935c-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c935c-131">-VM</span><span class="sxs-lookup"><span data-stu-id="c935c-131">-VM</span></span>
<span data-ttu-id="c935c-132">Gibt einen virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="c935c-132">Specifies a virtual machine.</span></span>
<span data-ttu-id="c935c-133">Verwenden Sie zum Abrufen eines virtuellen Computers das Cmdlet **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="c935c-133">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="c935c-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c935c-134">-Confirm</span></span>
<span data-ttu-id="c935c-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c935c-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c935c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c935c-136">-WhatIf</span></span>
<span data-ttu-id="c935c-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c935c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c935c-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c935c-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c935c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c935c-139">CommonParameters</span></span>
<span data-ttu-id="c935c-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c935c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c935c-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c935c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c935c-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c935c-142">INPUTS</span></span>

## <span data-ttu-id="c935c-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c935c-143">OUTPUTS</span></span>

## <span data-ttu-id="c935c-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="c935c-144">NOTES</span></span>

## <span data-ttu-id="c935c-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c935c-145">RELATED LINKS</span></span>

[<span data-ttu-id="c935c-146">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="c935c-146">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="c935c-147">Neu – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="c935c-147">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="c935c-148">Neustart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="c935c-148">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="c935c-149">Lebenslauf-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="c935c-149">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="c935c-150">Satz-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="c935c-150">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="c935c-151">Anfang-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="c935c-151">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="c935c-152">Stopp-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="c935c-152">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="c935c-153">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="c935c-153">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


