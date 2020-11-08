---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA9686AF-2D03-43DB-A91B-50D06D674A3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8da83231a16f4c846f09d03374d6e35757e1ba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006162"
---
# <span data-ttu-id="0c6be-101">Set-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="0c6be-101">Set-AzureIPForwarding</span></span>

## <span data-ttu-id="0c6be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c6be-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6be-103">Aktiviert oder deaktiviert die IP-Weiterleitung.</span><span class="sxs-lookup"><span data-stu-id="0c6be-103">Enables or disables IP forwarding.</span></span>

## <span data-ttu-id="0c6be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c6be-104">SYNTAX</span></span>

### <span data-ttu-id="0c6be-105">EnableIaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="0c6be-105">EnableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0c6be-106">DisableIaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="0c6be-106">DisableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0c6be-107">EnableSlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="0c6be-107">EnableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0c6be-108">DisableSlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="0c6be-108">DisableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0c6be-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c6be-109">DESCRIPTION</span></span>
<span data-ttu-id="0c6be-110">Das Cmdlet " **Satz-AzureIPForwarding** " aktiviert oder deaktiviert die IP-Weiterleitung für einen virtuellen Computer, für eine Plattform als Dienst (PaaS)-Rolle oder einen Netzwerkadapter, der zu einer virtuellen Maschine oder PaaS-Rolle gehört.</span><span class="sxs-lookup"><span data-stu-id="0c6be-110">The **Set-AzureIPForwarding** cmdlet enables or disables IP forwarding for a virtual machine, for a platform as a service (PaaS) role, or a network adapter that belongs to a virtual machine or PaaS role.</span></span>

## <span data-ttu-id="0c6be-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c6be-111">EXAMPLES</span></span>

### <span data-ttu-id="0c6be-112">Beispiel 1: Aktivieren der IP-Weiterleitung für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="0c6be-112">Example 1: Enable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Enable
```

<span data-ttu-id="0c6be-113">Dieser Befehl ruft einen virtuellen Computer mit dem Namen ContosoVM06 für den Dienst mit dem Namen ContosoService ab und übergibt das Objekt des virtuellen Computers an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c6be-113">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="0c6be-114">Das aktuelle Cmdlet aktiviert die IP-Weiterleitung für diesen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="0c6be-114">The current cmdlet enables IP forwarding for that virtual machine.</span></span>

### <span data-ttu-id="0c6be-115">Beispiel 2: Deaktivieren der IP-Weiterleitung für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="0c6be-115">Example 2: Disable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Disable
```

<span data-ttu-id="0c6be-116">Dieser Befehl ruft einen virtuellen Computer mit dem Namen ContosoVM06 für den Dienst mit dem Namen ContosoService ab und übergibt das Objekt des virtuellen Computers an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c6be-116">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="0c6be-117">Das aktuelle Cmdlet deaktiviert die IP-Weiterleitung für diesen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="0c6be-117">The current cmdlet disables IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="0c6be-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c6be-118">PARAMETERS</span></span>

### <span data-ttu-id="0c6be-119">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="0c6be-119">-Disable</span></span>
<span data-ttu-id="0c6be-120">Gibt an, dass dieses Cmdlet die IP-Weiterleitung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0c6be-120">Indicates that this cmdlet disables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableIaaSIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6be-121">-Enable</span><span class="sxs-lookup"><span data-stu-id="0c6be-121">-Enable</span></span>
<span data-ttu-id="0c6be-122">Gibt an, dass dieses Cmdlet IP-Weiterleitung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0c6be-122">Indicates that this cmdlet enables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableIaaSIPForwardingParamSet, EnableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6be-123">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="0c6be-123">-NetworkInterfaceName</span></span>
<span data-ttu-id="0c6be-124">Gibt den Namen des Netzwerkadapters an, auf dem dieses Cmdlet IP-Weiterleitung festlegt.</span><span class="sxs-lookup"><span data-stu-id="0c6be-124">Specifies the name of the network adapter on which this cmdlet sets IP forwarding.</span></span>

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

### <span data-ttu-id="0c6be-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c6be-125">-PassThru</span></span>
<span data-ttu-id="0c6be-126">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="0c6be-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0c6be-127">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="0c6be-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0c6be-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="0c6be-128">-Profile</span></span>
<span data-ttu-id="0c6be-129">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0c6be-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0c6be-130">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0c6be-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0c6be-131">-RoleName</span><span class="sxs-lookup"><span data-stu-id="0c6be-131">-RoleName</span></span>
<span data-ttu-id="0c6be-132">Gibt den Namen einer PaaS-Rolle an, auf der dieses Cmdlet IP-Weiterleitung festlegt.</span><span class="sxs-lookup"><span data-stu-id="0c6be-132">Specifies the name of a PaaS role on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6be-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0c6be-133">-ServiceName</span></span>
<span data-ttu-id="0c6be-134">Gibt den Namen eines Cloud-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="0c6be-134">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="0c6be-135">Die PaaS-Rolle gehört zu dem Dienst, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0c6be-135">The PaaS role belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="0c6be-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="0c6be-136">-Slot</span></span>
<span data-ttu-id="0c6be-137">Gibt einen PaaS-Steckplatz an.</span><span class="sxs-lookup"><span data-stu-id="0c6be-137">Specifies a PaaS slot.</span></span>
<span data-ttu-id="0c6be-138">Die PaaS-Rolle, für die dieses Cmdlet die Weiterleitung festlegt, hat den Slot, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0c6be-138">The PaaS role for which this cmdlet sets forwarding has the slot that this parameter specifies.</span></span>
<span data-ttu-id="0c6be-139">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="0c6be-139">Valid values are:</span></span>

- <span data-ttu-id="0c6be-140">Produktions</span><span class="sxs-lookup"><span data-stu-id="0c6be-140">Production</span></span>
- <span data-ttu-id="0c6be-141">Inszenierung</span><span class="sxs-lookup"><span data-stu-id="0c6be-141">Staging</span></span>

<span data-ttu-id="0c6be-142">Der Standardwert ist Production.</span><span class="sxs-lookup"><span data-stu-id="0c6be-142">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6be-143">-VM</span><span class="sxs-lookup"><span data-stu-id="0c6be-143">-VM</span></span>
<span data-ttu-id="0c6be-144">Gibt das Objekt des virtuellen Computers an, auf dem dieses Cmdlet IP-Weiterleitung festlegt.</span><span class="sxs-lookup"><span data-stu-id="0c6be-144">Specifies the virtual machine object on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: EnableIaaSIPForwardingParamSet, DisableIaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6be-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c6be-145">CommonParameters</span></span>
<span data-ttu-id="0c6be-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c6be-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c6be-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c6be-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c6be-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c6be-148">INPUTS</span></span>

## <span data-ttu-id="0c6be-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c6be-149">OUTPUTS</span></span>

### <span data-ttu-id="0c6be-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c6be-150">System.Boolean</span></span>

## <span data-ttu-id="0c6be-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c6be-151">NOTES</span></span>

## <span data-ttu-id="0c6be-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c6be-152">RELATED LINKS</span></span>

[<span data-ttu-id="0c6be-153">Get-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="0c6be-153">Get-AzureIPForwarding</span></span>](./Get-AzureIPForwarding.md)
