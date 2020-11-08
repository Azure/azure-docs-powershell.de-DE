---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 83D18A17-94A4-4FB8-9DA6-F652D5BB84C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf06561ac5f8c9e0c19edb88b7a8ff5ef816c609
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006092"
---
# <span data-ttu-id="2369c-101">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="2369c-101">New-WAPackVMSubnet</span></span>

## <span data-ttu-id="2369c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2369c-102">SYNOPSIS</span></span>
<span data-ttu-id="2369c-103">Erstellt ein Subnetz eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="2369c-103">Creates a virtual machine subnet.</span></span>

## <span data-ttu-id="2369c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2369c-104">SYNTAX</span></span>

```
New-WAPackVMSubnet -VNet <VMNetwork> -Name <String> -Subnet <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="2369c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2369c-105">DESCRIPTION</span></span>
<span data-ttu-id="2369c-106">Das Cmdlet **New-WAPackVMSubnet** erstellt ein Subnetz eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="2369c-106">The **New-WAPackVMSubnet** cmdlet creates a virtual machine subnet.</span></span>

## <span data-ttu-id="2369c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2369c-107">EXAMPLES</span></span>

### <span data-ttu-id="2369c-108">Beispiel 1: Erstellen eines virtuellen Computer-Subnetzes</span><span class="sxs-lookup"><span data-stu-id="2369c-108">Example 1: Create a virtual machine subnet</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> New-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01" -Subnet "192.168.1.0/24"
```

<span data-ttu-id="2369c-109">Der erste Befehl ruft zuerst das virtuelle Computernetzwerk ab, dem ein neues Subnetz für virtuelle Maschinen hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2369c-109">The first command first retrieves the virtual machine network to which we want to add a new virtual machine subnet.</span></span>
<span data-ttu-id="2369c-110">Dieses Virtual Machine-Netzwerk hat den Namen ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="2369c-110">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="2369c-111">Der zweite Befehl erstellt ein Subnetz eines virtuellen Computers mit dem zuvor abgerufenen virtuellen Computernetzwerk, einem Namen ContosoVMSubnet01 und einem Subnetz 192.168.1.0/24.</span><span class="sxs-lookup"><span data-stu-id="2369c-111">The second command creates a virtual machine subnet using the previously retrieve virtual machine network, a name ContosoVMSubnet01 and a subnet 192.168.1.0/24.</span></span>

## <span data-ttu-id="2369c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2369c-112">PARAMETERS</span></span>

### <span data-ttu-id="2369c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="2369c-113">-Name</span></span>
<span data-ttu-id="2369c-114">Gibt einen Namen für das Subnetz des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="2369c-114">Specifies a name for the virtual machine subnet.</span></span>

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

### <span data-ttu-id="2369c-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="2369c-115">-Profile</span></span>
<span data-ttu-id="2369c-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="2369c-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2369c-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="2369c-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2369c-118">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="2369c-118">-Subnet</span></span>
<span data-ttu-id="2369c-119">Gibt ein Subnetz für das Subnetz des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="2369c-119">Specifies a subnet for the virtual machine subnet.</span></span>

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

### <span data-ttu-id="2369c-120">-VNet</span><span class="sxs-lookup"><span data-stu-id="2369c-120">-VNet</span></span>
<span data-ttu-id="2369c-121">Gibt einen VNet an, der dem Subnetz des virtuellen Computers zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2369c-121">Specifies a VNet associated with the virtual machine subnet.</span></span>

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

### <span data-ttu-id="2369c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2369c-122">CommonParameters</span></span>
<span data-ttu-id="2369c-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2369c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2369c-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2369c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2369c-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2369c-125">INPUTS</span></span>

## <span data-ttu-id="2369c-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2369c-126">OUTPUTS</span></span>

## <span data-ttu-id="2369c-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="2369c-127">NOTES</span></span>

## <span data-ttu-id="2369c-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2369c-128">RELATED LINKS</span></span>

[<span data-ttu-id="2369c-129">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="2369c-129">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="2369c-130">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="2369c-130">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="2369c-131">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="2369c-131">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)


