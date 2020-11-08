---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 69974370-4542-4417-BD9D-3928EB005C31
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81d6e523978196a47b01d21aa8e857027b0b4f40
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006157"
---
# <span data-ttu-id="6c275-101">Set-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="6c275-101">Set-AzureSubnet</span></span>

## <span data-ttu-id="6c275-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c275-102">SYNOPSIS</span></span>
<span data-ttu-id="6c275-103">Definiert die Subnetliste für einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="6c275-103">Defines the subnet list for an Azure virtual machine.</span></span>

## <span data-ttu-id="6c275-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c275-104">SYNTAX</span></span>

```
Set-AzureSubnet [-SubnetNames] <String[]> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6c275-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c275-105">DESCRIPTION</span></span>
<span data-ttu-id="6c275-106">Das Cmdlet " **Set-AzureSubnet** " legt die Subnetliste für eine Konfiguration für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="6c275-106">The **Set-AzureSubnet** cmdlet sets the subnet list for a virtual machine configuration.</span></span>
<span data-ttu-id="6c275-107">Verwenden Sie mit **New-AzureVM** , um die Subnetze für einen virtuellen Computer einzurichten.</span><span class="sxs-lookup"><span data-stu-id="6c275-107">Use with **New-AzureVM** to set the subnets for a virtual machine.</span></span>

## <span data-ttu-id="6c275-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c275-108">EXAMPLES</span></span>

### <span data-ttu-id="6c275-109">Beispiel 1: Hinzufügen eines Subnetzes zu einer Konfiguration für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="6c275-109">Example 1: Add a subnet to a virtual machine configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine04" -ImageName $image -InstanceSize "Small" | Add-AzureProvisioningConfig -Windows -Password "password" | Set-AzureSubnet "PubSubnet","PrivSubnet" | New-AzureVM -ServiceName "ContosoService03"
```

<span data-ttu-id="6c275-110">Dieser Befehl fügt der Konfiguration des virtuellen Computers ein Subnetz hinzu und erstellt dann den virtuellen Computer mit dem Namen VirtualMachine04.</span><span class="sxs-lookup"><span data-stu-id="6c275-110">This command adds a subnet to the virtual machine configuration, and then creates the virtual machine named VirtualMachine04.</span></span>

## <span data-ttu-id="6c275-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c275-111">PARAMETERS</span></span>

### <span data-ttu-id="6c275-112">-Information</span><span class="sxs-lookup"><span data-stu-id="6c275-112">-InformationAction</span></span>
<span data-ttu-id="6c275-113">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="6c275-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6c275-114">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6c275-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6c275-115">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="6c275-115">Continue</span></span>
- <span data-ttu-id="6c275-116">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="6c275-116">Ignore</span></span>
- <span data-ttu-id="6c275-117">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="6c275-117">Inquire</span></span>
- <span data-ttu-id="6c275-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6c275-118">SilentlyContinue</span></span>
- <span data-ttu-id="6c275-119">Beenden</span><span class="sxs-lookup"><span data-stu-id="6c275-119">Stop</span></span>
- <span data-ttu-id="6c275-120">Anhalten</span><span class="sxs-lookup"><span data-stu-id="6c275-120">Suspend</span></span>

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

### <span data-ttu-id="6c275-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6c275-121">-InformationVariable</span></span>
<span data-ttu-id="6c275-122">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="6c275-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6c275-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="6c275-123">-Profile</span></span>
<span data-ttu-id="6c275-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6c275-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6c275-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6c275-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6c275-126">-SubnetNames</span><span class="sxs-lookup"><span data-stu-id="6c275-126">-SubnetNames</span></span>
<span data-ttu-id="6c275-127">Gibt ein Array an, das die Liste der Subnet-Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="6c275-127">Specifies an array that contains the list of subnet names.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c275-128">-VM</span><span class="sxs-lookup"><span data-stu-id="6c275-128">-VM</span></span>
<span data-ttu-id="6c275-129">Gibt das Objekt des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="6c275-129">Specifies the virtual machine object.</span></span>

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

### <span data-ttu-id="6c275-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c275-130">CommonParameters</span></span>
<span data-ttu-id="6c275-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c275-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c275-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c275-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c275-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c275-133">INPUTS</span></span>

## <span data-ttu-id="6c275-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c275-134">OUTPUTS</span></span>

## <span data-ttu-id="6c275-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c275-135">NOTES</span></span>

## <span data-ttu-id="6c275-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c275-136">RELATED LINKS</span></span>

[<span data-ttu-id="6c275-137">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6c275-137">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="6c275-138">Neu – AzureVM</span><span class="sxs-lookup"><span data-stu-id="6c275-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="6c275-139">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6c275-139">Update-AzureVM</span></span>](./Update-AzureVM.md)


