---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4414EA89-8573-416E-A611-DA2135E350BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75b216b512c364a3285df185a3365b1fc85a3d94
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007637"
---
# <span data-ttu-id="4b686-101">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="4b686-101">Get-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="4b686-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b686-102">SYNOPSIS</span></span>
<span data-ttu-id="4b686-103">Ruft statische IP-Adresspool Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="4b686-103">Gets static IP address pool objects.</span></span>

## <span data-ttu-id="4b686-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b686-104">SYNTAX</span></span>

### <span data-ttu-id="4b686-105">FromVMSubnetObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b686-105">FromVMSubnetObject (Default)</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4b686-106">FromName</span><span class="sxs-lookup"><span data-stu-id="4b686-106">FromName</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b686-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b686-107">DESCRIPTION</span></span>
<span data-ttu-id="4b686-108">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="4b686-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="4b686-109">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4b686-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4b686-110">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4b686-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4b686-111">Das Cmdlet " **Get-WAPackStaticIPAddressPool** " Ruft statische IP-Adresspool Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="4b686-111">The **Get-WAPackStaticIPAddressPool** cmdlet gets static IP address pool objects.</span></span>

## <span data-ttu-id="4b686-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b686-112">EXAMPLES</span></span>

### <span data-ttu-id="4b686-113">Beispiel 1: Abrufen eines statischen IP-Adresspools aus einem bestimmten VMSubnet</span><span class="sxs-lookup"><span data-stu-id="4b686-113">Example 1: Get a static IP address pool from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet -Name "ContosoStaticIPAddressPool01"
```

<span data-ttu-id="4b686-114">Dieser Befehl ruft den statischen IP-Adresspool mit dem Namen ContosoStaticIPAddressPool01 aus einem angegebenen VMSubnet ab.</span><span class="sxs-lookup"><span data-stu-id="4b686-114">This command gets the static IP address pool named ContosoStaticIPAddressPool01 from a specified VMSubnet.</span></span>

### <span data-ttu-id="4b686-115">Beispiel 2: Abrufen aller statischen IP-Adresspools aus einem bestimmten VMSubnet</span><span class="sxs-lookup"><span data-stu-id="4b686-115">Example 2: Get all static IP address pools from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet
```

<span data-ttu-id="4b686-116">Dieser Befehl ruft alle statischen IP-Pools aus einem angegebenen VMSubet ab.</span><span class="sxs-lookup"><span data-stu-id="4b686-116">This command gets all the static IP pools from a specified VMSubet.</span></span>

## <span data-ttu-id="4b686-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b686-117">PARAMETERS</span></span>

### <span data-ttu-id="4b686-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4b686-118">-Name</span></span>
<span data-ttu-id="4b686-119">Gibt den Namen eines statischen IP-Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="4b686-119">Specifies the name of a static IP address pool.</span></span>

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

### <span data-ttu-id="4b686-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="4b686-120">-Profile</span></span>
<span data-ttu-id="4b686-121">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="4b686-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4b686-122">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="4b686-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4b686-123">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="4b686-123">-VMSubnet</span></span>
<span data-ttu-id="4b686-124">Gibt das **VMSubnet** -Objekt an, das dem statischen IP-Adresspool zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4b686-124">Specifies the **VMSubnet** object associated to the static IP address pool.</span></span>

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

### <span data-ttu-id="4b686-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b686-125">CommonParameters</span></span>
<span data-ttu-id="4b686-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b686-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b686-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b686-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b686-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b686-128">INPUTS</span></span>

## <span data-ttu-id="4b686-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b686-129">OUTPUTS</span></span>

## <span data-ttu-id="4b686-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b686-130">NOTES</span></span>

## <span data-ttu-id="4b686-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b686-131">RELATED LINKS</span></span>

[<span data-ttu-id="4b686-132">Neu – WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="4b686-132">New-WAPackStaticIPAddressPool</span></span>](./New-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="4b686-133">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="4b686-133">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


