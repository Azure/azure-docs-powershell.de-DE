---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BE661AC7-BA39-4D6A-8083-16CE9327DC08
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4c84155484435a9601af005393593040c9cfe4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006554"
---
# <span data-ttu-id="a62a1-101">Get-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="a62a1-101">Get-AzureIPForwarding</span></span>

## <span data-ttu-id="a62a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a62a1-102">SYNOPSIS</span></span>
<span data-ttu-id="a62a1-103">Ruft den Status der IP-Weiterleitung ab.</span><span class="sxs-lookup"><span data-stu-id="a62a1-103">Gets the status of IP forwarding.</span></span>

## <span data-ttu-id="a62a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a62a1-104">SYNTAX</span></span>

### <span data-ttu-id="a62a1-105">IaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="a62a1-105">IaaSIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a62a1-106">SlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="a62a1-106">SlotIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a62a1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a62a1-107">DESCRIPTION</span></span>
<span data-ttu-id="a62a1-108">Das Cmdlet " **Get-AzureIPForwarding** " Ruft den Status der IP-Weiterleitung ab.</span><span class="sxs-lookup"><span data-stu-id="a62a1-108">The **Get-AzureIPForwarding** cmdlet gets the status of IP forwarding.</span></span>

## <span data-ttu-id="a62a1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a62a1-109">EXAMPLES</span></span>

### <span data-ttu-id="a62a1-110">Beispiel 1: Abrufen des IP-Weiterleitungsstatus für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="a62a1-110">Example 1: Get IP forwarding status for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureIPForwarding
Disabled
```

<span data-ttu-id="a62a1-111">Dieser Befehl ruft einen virtuellen Computer mit dem Namen ContosoVM06 für den Dienst mit dem Namen ContosoService ab und übergibt das Objekt des virtuellen Computers an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a62a1-111">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="a62a1-112">Das aktuelle Cmdlet ruft den Status der IP-Weiterleitung für diesen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="a62a1-112">The current cmdlet gets the status of IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="a62a1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a62a1-113">PARAMETERS</span></span>

### <span data-ttu-id="a62a1-114">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="a62a1-114">-NetworkInterfaceName</span></span>
<span data-ttu-id="a62a1-115">Gibt den Namen des Netzwerkadapters an, für den das Cmdlet den IP-Weiterleitungsstatus erhält.</span><span class="sxs-lookup"><span data-stu-id="a62a1-115">Specifies the name of the network adapter for which this cmdlet gets IP forwarding status.</span></span>

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

### <span data-ttu-id="a62a1-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="a62a1-116">-Profile</span></span>
<span data-ttu-id="a62a1-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a62a1-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a62a1-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a62a1-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a62a1-119">-RoleName</span><span class="sxs-lookup"><span data-stu-id="a62a1-119">-RoleName</span></span>
<span data-ttu-id="a62a1-120">Gibt den Namen einer PaaS-Rolle an, für die dieses Cmdlet den IP-Weiterleitungsstatus erhält.</span><span class="sxs-lookup"><span data-stu-id="a62a1-120">Specifies the name of a PaaS role for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a62a1-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a62a1-121">-ServiceName</span></span>
<span data-ttu-id="a62a1-122">Gibt den Namen eines Cloud-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="a62a1-122">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="a62a1-123">Die PaaS-Rolle gehört zu dem Dienst, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a62a1-123">The PaaS role belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="a62a1-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="a62a1-124">-Slot</span></span>
<span data-ttu-id="a62a1-125">Gibt einen PaaS-Steckplatz an.</span><span class="sxs-lookup"><span data-stu-id="a62a1-125">Specifies a PaaS slot.</span></span>
<span data-ttu-id="a62a1-126">Die PaaS-Rolle, für die dieses Cmdlet den Weiterleitungsstatus erhält, weist den Slot auf, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a62a1-126">The PaaS role for which this cmdlet gets forwarding status has the slot that this parameter specifies.</span></span>
<span data-ttu-id="a62a1-127">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="a62a1-127">Valid values are:</span></span> 

- <span data-ttu-id="a62a1-128">Produktions</span><span class="sxs-lookup"><span data-stu-id="a62a1-128">Production</span></span>
- <span data-ttu-id="a62a1-129">Inszenierung</span><span class="sxs-lookup"><span data-stu-id="a62a1-129">Staging</span></span> 

<span data-ttu-id="a62a1-130">Der Standardwert ist Production.</span><span class="sxs-lookup"><span data-stu-id="a62a1-130">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a62a1-131">-VM</span><span class="sxs-lookup"><span data-stu-id="a62a1-131">-VM</span></span>
<span data-ttu-id="a62a1-132">Gibt das Objekt des virtuellen Computers an, für das dieses Cmdlet den IP-Weiterleitungsstatus erhält.</span><span class="sxs-lookup"><span data-stu-id="a62a1-132">Specifies the virtual machine object for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a62a1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a62a1-133">CommonParameters</span></span>
<span data-ttu-id="a62a1-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a62a1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a62a1-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a62a1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a62a1-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a62a1-136">INPUTS</span></span>

## <span data-ttu-id="a62a1-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a62a1-137">OUTPUTS</span></span>

### <span data-ttu-id="a62a1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a62a1-138">System.String</span></span>

## <span data-ttu-id="a62a1-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="a62a1-139">NOTES</span></span>

## <span data-ttu-id="a62a1-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a62a1-140">RELATED LINKS</span></span>

[<span data-ttu-id="a62a1-141">Satz-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="a62a1-141">Set-AzureIPForwarding</span></span>](./Set-AzureIPForwarding.md)


