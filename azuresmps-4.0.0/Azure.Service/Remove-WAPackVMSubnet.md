---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7766E3D-D8C2-42F1-840A-8EA633E98500
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8a85934deb617b4f0d8e85ee3162222f16dd294
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007613"
---
# <span data-ttu-id="829e5-101">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="829e5-101">Remove-WAPackVMSubnet</span></span>

## <span data-ttu-id="829e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="829e5-102">SYNOPSIS</span></span>
<span data-ttu-id="829e5-103">Entfernt Subnetz-Objekte des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="829e5-103">Removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="829e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="829e5-104">SYNTAX</span></span>

```
Remove-WAPackVMSubnet -VMSubnet <VMSubnet> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="829e5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="829e5-105">DESCRIPTION</span></span>
<span data-ttu-id="829e5-106">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="829e5-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="829e5-107">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="829e5-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="829e5-108">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="829e5-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="829e5-109">Das Cmdlet **Remove-WAPackVMSubnet** entfernt Subnetzmasken virtueller Maschinen.</span><span class="sxs-lookup"><span data-stu-id="829e5-109">The **Remove-WAPackVMSubnet** cmdlet removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="829e5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="829e5-110">EXAMPLES</span></span>

### <span data-ttu-id="829e5-111">Beispiel 1: Entfernen eines virtuellen Computer-Subnets</span><span class="sxs-lookup"><span data-stu-id="829e5-111">Example 1: Remove a virtual machine subnet</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet01"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet
```

<span data-ttu-id="829e5-112">Der erste Befehl ruft das Subnetz des virtuellen Computers mit dem Namen ContosoVMSubnet01 mit dem Cmdlet **Get-WAPackVMSubnet** ab und speichert dieses Objekt dann in der $VMSubnet Variablen.</span><span class="sxs-lookup"><span data-stu-id="829e5-112">The first command gets the virtual machine subnet named ContosoVMSubnet01 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="829e5-113">Mit dem zweiten Befehl wird das in $VMSubnet gespeicherte Virtual Machine-Subnetz entfernt.</span><span class="sxs-lookup"><span data-stu-id="829e5-113">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="829e5-114">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="829e5-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="829e5-115">Beispiel 2: Entfernen einer virtuellen Maschine ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="829e5-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet02"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet -Force
```

<span data-ttu-id="829e5-116">Der erste Befehl ruft den clouddienst mit dem Namen ContosoVMSubnet02 mit dem Cmdlet **Get-WAPackVMSubnet** ab und speichert dieses Objekt dann in der $VMSubnet Variablen.</span><span class="sxs-lookup"><span data-stu-id="829e5-116">The first command gets the cloud service named ContosoVMSubnet02 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="829e5-117">Mit dem zweiten Befehl wird das in $VMSubnet gespeicherte Virtual Machine-Subnetz entfernt.</span><span class="sxs-lookup"><span data-stu-id="829e5-117">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="829e5-118">Dieser Befehl enthält den Parameter *Force* .</span><span class="sxs-lookup"><span data-stu-id="829e5-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="829e5-119">Der Befehl fordert Sie nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="829e5-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="829e5-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="829e5-120">PARAMETERS</span></span>

### <span data-ttu-id="829e5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="829e5-121">-Force</span></span>
<span data-ttu-id="829e5-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="829e5-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="829e5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="829e5-123">-PassThru</span></span>
<span data-ttu-id="829e5-124">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="829e5-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="829e5-125">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="829e5-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="829e5-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="829e5-126">-Profile</span></span>
<span data-ttu-id="829e5-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="829e5-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="829e5-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="829e5-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="829e5-129">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="829e5-129">-VMSubnet</span></span>
<span data-ttu-id="829e5-130">Gibt ein Subnetz eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="829e5-130">Specifies a virtual machine subnet.</span></span>
<span data-ttu-id="829e5-131">Um ein Subnetz eines virtuellen Computers zu erhalten, verwenden Sie das Cmdlet **Get-WAPackVMSubnet** .</span><span class="sxs-lookup"><span data-stu-id="829e5-131">To obtain a virtual machine subnet, use the **Get-WAPackVMSubnet** cmdlet.</span></span>

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="829e5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="829e5-132">CommonParameters</span></span>
<span data-ttu-id="829e5-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="829e5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="829e5-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="829e5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="829e5-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="829e5-135">INPUTS</span></span>

## <span data-ttu-id="829e5-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="829e5-136">OUTPUTS</span></span>

## <span data-ttu-id="829e5-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="829e5-137">NOTES</span></span>

## <span data-ttu-id="829e5-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="829e5-138">RELATED LINKS</span></span>

[<span data-ttu-id="829e5-139">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="829e5-139">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="829e5-140">Neu – WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="829e5-140">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)


