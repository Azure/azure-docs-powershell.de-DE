---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0E358CEF-69E4-4639-918C-CE593E97B189
online version: ''
schema: 2.0.0
ms.openlocfilehash: d534a1734a49739db648558e8d7e62b22e43d561
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007561"
---
# <span data-ttu-id="b8ab9-101">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="b8ab9-101">Get-WAPackVMSubnet</span></span>

## <span data-ttu-id="b8ab9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b8ab9-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ab9-103">Ruft Subnetz-Objekte des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="b8ab9-103">Gets virtual machine subnet objects.</span></span>

## <span data-ttu-id="b8ab9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8ab9-104">SYNTAX</span></span>

### <span data-ttu-id="b8ab9-105">FromVMNetworkObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="b8ab9-105">FromVMNetworkObject (Default)</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b8ab9-106">FromName</span><span class="sxs-lookup"><span data-stu-id="b8ab9-106">FromName</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b8ab9-107">FromId</span><span class="sxs-lookup"><span data-stu-id="b8ab9-107">FromId</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b8ab9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8ab9-108">DESCRIPTION</span></span>
<span data-ttu-id="b8ab9-109">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="b8ab9-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="b8ab9-110">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b8ab9-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b8ab9-111">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b8ab9-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b8ab9-112">Das Cmdlet " **Get-WAPackVMSubnet** " ruft Subnetze von virtuellen Maschinen ab.</span><span class="sxs-lookup"><span data-stu-id="b8ab9-112">The **Get-WAPackVMSubnet** cmdlet gets virtual machine subnet objects.</span></span>

## <span data-ttu-id="b8ab9-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b8ab9-113">EXAMPLES</span></span>

### <span data-ttu-id="b8ab9-114">Beispiel 1: Abrufen eines virtuellen Computer-Subnetzes mithilfe eines Namens</span><span class="sxs-lookup"><span data-stu-id="b8ab9-114">Example 1: Get a virtual machine subnet by using a name</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMTemplate -VNet $VNet -Name "ContosoSubnet01"
```

<span data-ttu-id="b8ab9-115">Dieser Befehl ruft das Subnetz des virtuellen Computers mit dem Namen ContosoSubnet01 ab.</span><span class="sxs-lookup"><span data-stu-id="b8ab9-115">This command gets the virtual machine subnet named ContosoSubnet01.</span></span>

### <span data-ttu-id="b8ab9-116">Beispiel 2: Abrufen eines virtuellen Computer-Subnets mithilfe einer ID</span><span class="sxs-lookup"><span data-stu-id="b8ab9-116">Example 2: Get a virtual machine subnet by using an ID</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="b8ab9-117">Dieser Befehl ruft das Subnetz des virtuellen Computers ab, das die angegebene ID hat.</span><span class="sxs-lookup"><span data-stu-id="b8ab9-117">This command gets the virtual machine subnet that has the specified ID.</span></span>

### <span data-ttu-id="b8ab9-118">Beispiel 3: Abrufen aller Subnetze virtueller Maschinen aus einem bestimmten virtualisierten Netzwerk</span><span class="sxs-lookup"><span data-stu-id="b8ab9-118">Example 3: Get all virtual machine subnets from a given virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet
```

<span data-ttu-id="b8ab9-119">Dieser Befehl ruft alle Subnetze virtueller Maschinen aus einem gegebenen virtualisierten Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="b8ab9-119">This command gets all the virtual machine subnets from a given virtualized network.</span></span>

## <span data-ttu-id="b8ab9-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8ab9-120">PARAMETERS</span></span>

### <span data-ttu-id="b8ab9-121">-ID</span><span class="sxs-lookup"><span data-stu-id="b8ab9-121">-ID</span></span>
<span data-ttu-id="b8ab9-122">Gibt die eindeutige ID für ein Subnetz eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="b8ab9-122">Specifies the unique ID of a virtual machine subnet.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ab9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b8ab9-123">-Name</span></span>
<span data-ttu-id="b8ab9-124">Gibt den Namen eines Subnetzes für virtuelle Computer an.</span><span class="sxs-lookup"><span data-stu-id="b8ab9-124">Specifies the name of a virtual machine subnet.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ab9-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="b8ab9-125">-Profile</span></span>
<span data-ttu-id="b8ab9-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b8ab9-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b8ab9-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b8ab9-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b8ab9-128">-VNet</span><span class="sxs-lookup"><span data-stu-id="b8ab9-128">-VNet</span></span>
<span data-ttu-id="b8ab9-129">Gibt den VNet an, der einem Subnetz eines virtuellen Computers zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b8ab9-129">Specifies the VNet associated with a virtual machine subnet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ab9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ab9-130">CommonParameters</span></span>
<span data-ttu-id="b8ab9-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8ab9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ab9-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8ab9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ab9-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b8ab9-133">INPUTS</span></span>

## <span data-ttu-id="b8ab9-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b8ab9-134">OUTPUTS</span></span>

## <span data-ttu-id="b8ab9-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b8ab9-135">NOTES</span></span>

## <span data-ttu-id="b8ab9-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b8ab9-136">RELATED LINKS</span></span>

[<span data-ttu-id="b8ab9-137">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="b8ab9-137">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="b8ab9-138">Neu – WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="b8ab9-138">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)

[<span data-ttu-id="b8ab9-139">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="b8ab9-139">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)


