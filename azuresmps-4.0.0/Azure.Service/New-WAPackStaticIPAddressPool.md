---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22A9B83D-789D-4722-BDD1-D8C448CFB88A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c809a49e2e8c1a534d6868c99bcc7cab1d20ccd1
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007587"
---
# <span data-ttu-id="fada6-101">New-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="fada6-101">New-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="fada6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fada6-102">SYNOPSIS</span></span>
<span data-ttu-id="fada6-103">Erstellt einen statischen IP-Adresspool.</span><span class="sxs-lookup"><span data-stu-id="fada6-103">Creates a static IP address pool.</span></span>

## <span data-ttu-id="fada6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fada6-104">SYNTAX</span></span>

```
New-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> -IPAddressRangeStart <String>
 -IPAddressRangeEnd <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fada6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fada6-105">DESCRIPTION</span></span>
<span data-ttu-id="fada6-106">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="fada6-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="fada6-107">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fada6-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="fada6-108">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="fada6-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="fada6-109">Mit dem Cmdlet **New-WAPackStaticIPAddressPool** wird ein statischer IP-Adresspool erstellt.</span><span class="sxs-lookup"><span data-stu-id="fada6-109">The **New-WAPackStaticIPAddressPool** cmdlet creates a static IP address pool.</span></span>

## <span data-ttu-id="fada6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fada6-110">EXAMPLES</span></span>

### <span data-ttu-id="fada6-111">Beispiel 1: Erstellen eines statischen IP-Adresspools</span><span class="sxs-lookup"><span data-stu-id="fada6-111">Example 1: Create a static IP address pool</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> $VMSubnet = Get-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01"
PS C:\> New-WAPackStaticIpAddressPool ?VMSubnet $VMSubnet -Name "ContosoStaticIpAddressPool01" -IPAddressRangeStart "192.168.1.0" -IPAddressRangeEnd "192.168.1.10"
```

<span data-ttu-id="fada6-112">Der erste Befehl ruft zuerst das virtuelle Computernetzwerk ab, dem der statische IP-Adresspool hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fada6-112">The first command first retrieves the virtual machine network to which we want to add the static IP address pool.</span></span>
<span data-ttu-id="fada6-113">Dieses Virtual Machine-Netzwerk hat den Namen ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="fada6-113">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="fada6-114">Der zweite Befehl verwendet das zuvor abgerufene Virtual Machine-Netzwerk, um das Subnetz des virtuellen Computers mit dem Namen ContosoVMSubnet01 abzurufen, dem der statische IP-Adresspool hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fada6-114">The second command uses the previously retrieved virtual machine network to get the virtual machine subnet named ContosoVMSubnet01 to which we want to add the static IP address pool.</span></span>

<span data-ttu-id="fada6-115">Mit dem letzten Befehl wird ein neuer statischer IP-Adresspool mit einem Namen ContosoStaticIpAddressPool01 und einem Bereichs Start-192.168.1.0 und einem Bereichsende-192.168.1.10 erstellt.</span><span class="sxs-lookup"><span data-stu-id="fada6-115">The last command creates a new static IP address pool with a name ContosoStaticIpAddressPool01 and a range start 192.168.1.0 and a range end 192.168.1.10.</span></span>

## <span data-ttu-id="fada6-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="fada6-116">PARAMETERS</span></span>

### <span data-ttu-id="fada6-117">-IPAddressRangeEnd</span><span class="sxs-lookup"><span data-stu-id="fada6-117">-IPAddressRangeEnd</span></span>
<span data-ttu-id="fada6-118">Gibt einen IP-Adressbereich an, der für den statischen IP-Adresspool endet.</span><span class="sxs-lookup"><span data-stu-id="fada6-118">Specifies an IP address range end for the static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fada6-119">-IPAddressRangeStart</span><span class="sxs-lookup"><span data-stu-id="fada6-119">-IPAddressRangeStart</span></span>
<span data-ttu-id="fada6-120">Gibt einen IP-Adressbereich an, der für den statischen IP-Adresspool gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="fada6-120">Specifies an IP address range start for the static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fada6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fada6-121">-Name</span></span>
<span data-ttu-id="fada6-122">Gibt einen Namen für den statischen IP-Adresspool an.</span><span class="sxs-lookup"><span data-stu-id="fada6-122">Specifies a name for the static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fada6-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="fada6-123">-Profile</span></span>
<span data-ttu-id="fada6-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="fada6-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fada6-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="fada6-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fada6-126">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="fada6-126">-VMSubnet</span></span>
<span data-ttu-id="fada6-127">Gibt einen VMSubnet an, der dem statischen IP-Adresspool zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fada6-127">Specifies a VMSubnet associated with the static IP address pool.</span></span>

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

### <span data-ttu-id="fada6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fada6-128">CommonParameters</span></span>
<span data-ttu-id="fada6-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fada6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fada6-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fada6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fada6-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fada6-131">INPUTS</span></span>

## <span data-ttu-id="fada6-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fada6-132">OUTPUTS</span></span>

## <span data-ttu-id="fada6-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="fada6-133">NOTES</span></span>

## <span data-ttu-id="fada6-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fada6-134">RELATED LINKS</span></span>

[<span data-ttu-id="fada6-135">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="fada6-135">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="fada6-136">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="fada6-136">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


