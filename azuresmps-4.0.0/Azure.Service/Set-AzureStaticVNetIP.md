---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E54E4D16-DB2A-4626-B543-773C187B2E08
online version: ''
schema: 2.0.0
ms.openlocfilehash: d242418117b1bb576206f9ebb5fd568bd3e63cd1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006068"
---
# <span data-ttu-id="8723d-101">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="8723d-101">Set-AzureStaticVNetIP</span></span>

## <span data-ttu-id="8723d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8723d-102">SYNOPSIS</span></span>
<span data-ttu-id="8723d-103">Legt die statischen VNet-IP-Adressinformationen für ein Objekt eines virtuellen Computers fest.</span><span class="sxs-lookup"><span data-stu-id="8723d-103">Sets the static VNet IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="8723d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8723d-104">SYNTAX</span></span>

```
Set-AzureStaticVNetIP [-IPAddress] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8723d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8723d-105">DESCRIPTION</span></span>
<span data-ttu-id="8723d-106">Das Cmdlet " **Set-AzureStaticVNetIP** " legt die IP-Adressinformationen (static Virtual Network, VNet) für ein Objekt eines virtuellen Computers fest.</span><span class="sxs-lookup"><span data-stu-id="8723d-106">The **Set-AzureStaticVNetIP** cmdlet sets the static virtual network (VNet) IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="8723d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8723d-107">EXAMPLES</span></span>

### <span data-ttu-id="8723d-108">Beispiel 1: Einrichten der IP-Adresse des virtuellen Netzwerks, die einem virtuellen Computer zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="8723d-108">Example 1: Set the virtual network IP address associated with a virtual machine</span></span>
```
PS C:\> # Prerequisite: VNet has been set up with SubNet
          # Set-AzureVNetConfig -ConfigurationPath $vnetConfigPath;

          $vm = New-AzureVMConfig -Name $vmname -ImageName $img -InstanceSize $sz | Add-AzureProvisioningConfig -Windows -Password $pwd -AdminUsername $usr;
          $vm = Set-AzureSubNet -VM $vm -SubNetNames $sn;
          Set-AzureStaticVNetIP -IPAddress $ip -VM $vm;
          New-AzureVM -ServiceName $svc -VMs $vm -VNetName $vnetName -Location $loc;
```

<span data-ttu-id="8723d-109">Der erste Befehl legt den Konfigurationspfad für ein virtuelles Netzwerk fest.</span><span class="sxs-lookup"><span data-stu-id="8723d-109">The first command sets the configuration path for a virtual network.</span></span>

<span data-ttu-id="8723d-110">Mit dem zweiten Befehl wird eine Konfiguration für einen virtuellen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="8723d-110">The second command creates a virtual machine configuration.</span></span>

<span data-ttu-id="8723d-111">Der dritte Befehl legt das Subnetz für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="8723d-111">The third command sets the subnet for the virtual machine.</span></span>

<span data-ttu-id="8723d-112">Der vierte Befehl legt die IP-Adresse für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="8723d-112">The fourth command sets the IP address for the virtual machine.</span></span>

<span data-ttu-id="8723d-113">Der fünfte Befehl erstellt einen virtuellen Computer, der den virtuellen Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="8723d-113">The fifth command creates a virtual machine using the virtual machine.</span></span>

## <span data-ttu-id="8723d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8723d-114">PARAMETERS</span></span>

### <span data-ttu-id="8723d-115">-Information</span><span class="sxs-lookup"><span data-stu-id="8723d-115">-InformationAction</span></span>
<span data-ttu-id="8723d-116">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="8723d-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8723d-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8723d-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8723d-118">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="8723d-118">Continue</span></span>
- <span data-ttu-id="8723d-119">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="8723d-119">Ignore</span></span>
- <span data-ttu-id="8723d-120">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="8723d-120">Inquire</span></span>
- <span data-ttu-id="8723d-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8723d-121">SilentlyContinue</span></span>
- <span data-ttu-id="8723d-122">Beenden</span><span class="sxs-lookup"><span data-stu-id="8723d-122">Stop</span></span>
- <span data-ttu-id="8723d-123">Anhalten</span><span class="sxs-lookup"><span data-stu-id="8723d-123">Suspend</span></span>

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

### <span data-ttu-id="8723d-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8723d-124">-InformationVariable</span></span>
<span data-ttu-id="8723d-125">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="8723d-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8723d-126">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="8723d-126">-IPAddress</span></span>
<span data-ttu-id="8723d-127">Gibt die statische VNet-IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="8723d-127">Specifies the static VNet IP address</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8723d-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="8723d-128">-Profile</span></span>
<span data-ttu-id="8723d-129">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8723d-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8723d-130">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8723d-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8723d-131">-VM</span><span class="sxs-lookup"><span data-stu-id="8723d-131">-VM</span></span>
<span data-ttu-id="8723d-132">Gibt ein persistentes virtuelles Computerobjekt an, für das die statische VNet-IP-Adresse festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8723d-132">Specifies a persistent virtual machine object for which to set the static VNet IP address.</span></span>

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

### <span data-ttu-id="8723d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8723d-133">CommonParameters</span></span>
<span data-ttu-id="8723d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8723d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8723d-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8723d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8723d-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8723d-136">INPUTS</span></span>

## <span data-ttu-id="8723d-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8723d-137">OUTPUTS</span></span>

## <span data-ttu-id="8723d-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="8723d-138">NOTES</span></span>

## <span data-ttu-id="8723d-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8723d-139">RELATED LINKS</span></span>

[<span data-ttu-id="8723d-140">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="8723d-140">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="8723d-141">Test-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="8723d-141">Test-AzureStaticVNetIP</span></span>](./Test-AzureStaticVNetIP.md)


