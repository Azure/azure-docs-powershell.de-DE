---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 82CF6E71-FFE2-4B2C-8AAD-04C137AD5706
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49f9cce74cb2621d6c9ff51485b7c4bce4a302bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006559"
---
# <span data-ttu-id="4bd7c-101">Get-AzureEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="4bd7c-101">Get-AzureEffectiveRouteTable</span></span>

## <span data-ttu-id="4bd7c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4bd7c-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd7c-103">Ruft die Route ab, die auf einem virtuellen Computer angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-103">Gets the route applied in a virtual machine.</span></span>

## <span data-ttu-id="4bd7c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bd7c-104">SYNTAX</span></span>

### <span data-ttu-id="4bd7c-105">IaaSGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="4bd7c-105">IaaSGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4bd7c-106">SlotGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="4bd7c-106">SlotGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -ServiceName <String> [-Slot <String>] -RoleInstanceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4bd7c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bd7c-107">DESCRIPTION</span></span>
<span data-ttu-id="4bd7c-108">Das Cmdlet " **Get-AzureEffectiveRouteTable** " Ruft die Route ab, die auf einem virtuellen Computer angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-108">The **Get-AzureEffectiveRouteTable** cmdlet gets the route applied in a virtual machine.</span></span>
<span data-ttu-id="4bd7c-109">Dieser Vorgang kann einige Sekunden dauern.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-109">This operation could take several seconds to finish.</span></span>

## <span data-ttu-id="4bd7c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4bd7c-110">EXAMPLES</span></span>

### <span data-ttu-id="4bd7c-111">Beispiel 1: Abrufen der effektiven Route, auf die ein virtueller Computer angewendet wurde</span><span class="sxs-lookup"><span data-stu-id="4bd7c-111">Example 1: Get the effective route applied a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureEffectiveRouteTable
```

<span data-ttu-id="4bd7c-112">Dieser Befehl ruft einen virtuellen Computer mit dem Namen ContosoVM06 für den Dienst mit dem Namen ContosoService ab und übergibt das Objekt des virtuellen Computers an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="4bd7c-113">Das aktuelle Cmdlet ruft die Route ab, die auf diesen virtuellen Computer angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-113">The current cmdlet gets the route applied to that virtual machine.</span></span>

## <span data-ttu-id="4bd7c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bd7c-114">PARAMETERS</span></span>

### <span data-ttu-id="4bd7c-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="4bd7c-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="4bd7c-116">Gibt den Namen des Netzwerkadapters an, für den dieses Cmdlet effektive Routen erhält.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-116">Specifies the name of the network adapter for which this cmdlet gets effective routes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd7c-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="4bd7c-117">-Profile</span></span>
<span data-ttu-id="4bd7c-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="4bd7c-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4bd7c-120">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="4bd7c-120">-RoleInstanceName</span></span>
<span data-ttu-id="4bd7c-121">Gibt den Namen einer PaaS-Rolle an, für die dieses Cmdlet effektive Routen erhält.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-121">Specifies the name of a PaaS role for which this cmdlet gets effective routes.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd7c-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4bd7c-122">-ServiceName</span></span>
<span data-ttu-id="4bd7c-123">Gibt den Namen eines Cloud-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-123">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="4bd7c-124">Die PaaS-Rolle, für die dieses Cmdlet effektive Routen erhält, gehört zu dem Dienst, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-124">The PaaS role for which this cmdlet gets effective routes belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd7c-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="4bd7c-125">-Slot</span></span>
<span data-ttu-id="4bd7c-126">Gibt einen PaaS-Steckplatz an.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-126">Specifies a PaaS slot.</span></span>
<span data-ttu-id="4bd7c-127">Die PaaS-Rolle, für die dieses Cmdlet effektive Routen erhält, weist den Slot auf, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-127">The PaaS role for which this cmdlet gets effective routes has the slot that this parameter specifies.</span></span>
<span data-ttu-id="4bd7c-128">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="4bd7c-128">Valid values are:</span></span> 

- <span data-ttu-id="4bd7c-129">Produktions</span><span class="sxs-lookup"><span data-stu-id="4bd7c-129">Production</span></span>
- <span data-ttu-id="4bd7c-130">Inszenierung</span><span class="sxs-lookup"><span data-stu-id="4bd7c-130">Staging</span></span> 

<span data-ttu-id="4bd7c-131">Der Standardwert ist Production.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-131">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd7c-132">-VM</span><span class="sxs-lookup"><span data-stu-id="4bd7c-132">-VM</span></span>
<span data-ttu-id="4bd7c-133">Gibt das Objekt des virtuellen Computers an, für das dieses Cmdlet effektive Routen erhält.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-133">Specifies the virtual machine object for which this cmdlet gets effective routes.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd7c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd7c-134">CommonParameters</span></span>
<span data-ttu-id="4bd7c-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bd7c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd7c-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd7c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd7c-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4bd7c-137">INPUTS</span></span>

## <span data-ttu-id="4bd7c-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4bd7c-138">OUTPUTS</span></span>

### <span data-ttu-id="4bd7c-139">System. Collections. Generic. IEnumerable<Microsoft. WindowsAzure. Management. Network. Models. EffectiveRouteTable, Microsoft. WindowsAzure. Management. Network></span><span class="sxs-lookup"><span data-stu-id="4bd7c-139">System.Collections.Generic.IEnumerable<Microsoft.WindowsAzure.Management.Network.Models.EffectiveRouteTable, Microsoft.WindowsAzure.Management.Network></span></span>

## <span data-ttu-id="4bd7c-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="4bd7c-140">NOTES</span></span>

## <span data-ttu-id="4bd7c-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4bd7c-141">RELATED LINKS</span></span>

[<span data-ttu-id="4bd7c-142">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="4bd7c-142">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="4bd7c-143">Neu – AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="4bd7c-143">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="4bd7c-144">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="4bd7c-144">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)

[<span data-ttu-id="4bd7c-145">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="4bd7c-145">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="4bd7c-146">Satz-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="4bd7c-146">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


