---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 73CEA6A8-46C9-4772-9A67-03F532696CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1287b3a0bb1cc39dea78fb4e92d2dcc4508c6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005749"
---
# <span data-ttu-id="7c208-101">Get-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="7c208-101">Get-AzureSubnet</span></span>

## <span data-ttu-id="7c208-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c208-102">SYNOPSIS</span></span>
<span data-ttu-id="7c208-103">Ruft eine Liste der Subnetze ab, die dem angegebenen Azure Virtual Machine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7c208-103">Gets a list of subnets associated with the specified Azure virtual machine.</span></span>

## <span data-ttu-id="7c208-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c208-104">SYNTAX</span></span>

```
Get-AzureSubnet -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7c208-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c208-105">DESCRIPTION</span></span>
<span data-ttu-id="7c208-106">Das Cmdlet " **Get-AzureSubnet** " gibt eine Liste der Subnetze zurück, die dem angegebenen virtuellen Computer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7c208-106">The **Get-AzureSubnet** cmdlet returns a list the subnets associated with the specified virtual machine.</span></span>
<span data-ttu-id="7c208-107">Verwenden Sie " **Get-AzureVM** ", um den virtuellen Computer anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7c208-107">Use **Get-AzureVM** to specify the virtual machine.</span></span>

## <span data-ttu-id="7c208-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c208-108">EXAMPLES</span></span>

### <span data-ttu-id="7c208-109">Beispiel 1: Abrufen von Subnetzen für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="7c208-109">Example 1: Get subnets for a virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine01"
C:\PS> Get-AzureSubnet -VM $VM
```

<span data-ttu-id="7c208-110">Der erste Befehl ruft einen virtuellen Computer mit dem Namen VirtualMachine01 im Dienst mit dem Namen ContosoService03 ab und speichert ihn dann in der $VM-Variablen.</span><span class="sxs-lookup"><span data-stu-id="7c208-110">The first command gets a virtual machine named VirtualMachine01 in the service named ContosoService03, and then stores it in the $VM variable.</span></span>

<span data-ttu-id="7c208-111">Der zweite Befehl ruft die Azure-Subnetze für den virtuellen Computer in $VM ab.</span><span class="sxs-lookup"><span data-stu-id="7c208-111">The second command gets the Azure subnets for the virtual machine in $VM.</span></span>

## <span data-ttu-id="7c208-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c208-112">PARAMETERS</span></span>

### <span data-ttu-id="7c208-113">-Information</span><span class="sxs-lookup"><span data-stu-id="7c208-113">-InformationAction</span></span>
<span data-ttu-id="7c208-114">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="7c208-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7c208-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7c208-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7c208-116">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="7c208-116">Continue</span></span>
- <span data-ttu-id="7c208-117">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="7c208-117">Ignore</span></span>
- <span data-ttu-id="7c208-118">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="7c208-118">Inquire</span></span>
- <span data-ttu-id="7c208-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7c208-119">SilentlyContinue</span></span>
- <span data-ttu-id="7c208-120">Beenden</span><span class="sxs-lookup"><span data-stu-id="7c208-120">Stop</span></span>
- <span data-ttu-id="7c208-121">Anhalten</span><span class="sxs-lookup"><span data-stu-id="7c208-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c208-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7c208-122">-InformationVariable</span></span>
<span data-ttu-id="7c208-123">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="7c208-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c208-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="7c208-124">-Profile</span></span>
<span data-ttu-id="7c208-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="7c208-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7c208-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="7c208-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7c208-127">-VM</span><span class="sxs-lookup"><span data-stu-id="7c208-127">-VM</span></span>
<span data-ttu-id="7c208-128">Gibt das Objekt des virtuellen Computers an, aus dem die Subnetliste abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c208-128">Specifies the virtual machine object from which to get the subnet list.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c208-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c208-129">CommonParameters</span></span>
<span data-ttu-id="7c208-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c208-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c208-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c208-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c208-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c208-132">INPUTS</span></span>

## <span data-ttu-id="7c208-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c208-133">OUTPUTS</span></span>

## <span data-ttu-id="7c208-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c208-134">NOTES</span></span>

## <span data-ttu-id="7c208-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c208-135">RELATED LINKS</span></span>

[<span data-ttu-id="7c208-136">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="7c208-136">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="7c208-137">Satz-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="7c208-137">Set-AzureSubnet</span></span>](./Set-AzureSubnet.md)


