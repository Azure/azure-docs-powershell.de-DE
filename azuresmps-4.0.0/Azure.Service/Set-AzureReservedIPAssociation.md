---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3249E908-B1D9-4707-844D-168274F1A466
online version: ''
schema: 2.0.0
ms.openlocfilehash: ae16609adf70b2e5a0edcd05c36b30860a3920cf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006031"
---
# <span data-ttu-id="1758d-101">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="1758d-101">Set-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="1758d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1758d-102">SYNOPSIS</span></span>
<span data-ttu-id="1758d-103">Ordnet eine reservierte IP-Adresse einem vorhandenen virtuellen Computer oder einem cloudbasierten Dienst zu.</span><span class="sxs-lookup"><span data-stu-id="1758d-103">Associates a reserved IP address with an existing virtual machine or cloud service.</span></span>

## <span data-ttu-id="1758d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1758d-104">SYNTAX</span></span>

```
Set-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String> [[-VirtualIPName] <String>]
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1758d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1758d-105">DESCRIPTION</span></span>
<span data-ttu-id="1758d-106">Das Cmdlet " **Satz-AzureReservedIPAssociation** " ordnet eine reservierte IP-Adresse der virtuellen IP-Adresse (VIP) eines ausgeführten virtuellen Computers oder Cloud-Diensts zu.</span><span class="sxs-lookup"><span data-stu-id="1758d-106">The **Set-AzureReservedIPAssociation** cmdlet associates a reserved IP address with the Virtual IP address (VIP) of a running virtual machine or cloud service.</span></span>
<span data-ttu-id="1758d-107">Die reservierte IP-Adresse darf zum Zeitpunkt des Aufrufs dieses Cmdlets nicht verwendet werden und muss sich in der gleichen Region wie der virtuelle Computer oder der Cloud-Dienst befinden.</span><span class="sxs-lookup"><span data-stu-id="1758d-107">The reserved IP address must not be in use at the time of invocation of this cmdlet, and must be in the same region as the virtual machine or cloud service.</span></span>

<span data-ttu-id="1758d-108">Der Vorgang dauert etwa 30 Sekunden, nachdem auf den virtuellen Computer oder Dienst über die reservierte IP-Adresse zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="1758d-108">The operation takes about 30 seconds to complete, after which the virtual machine or service is accessible using the reserved IP address.</span></span>

## <span data-ttu-id="1758d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1758d-109">EXAMPLES</span></span>

### <span data-ttu-id="1758d-110">Beispiel 1: Einrichten einer reservierten IP-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="1758d-110">Example 1: Set a reserved IP association</span></span>
```
PS C:\> Set-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="1758d-111">Dieser Befehl weist die reservierte IP-Adresse mit dem Namen ResIp14 dem Dienst PipTestWestEurope zu.</span><span class="sxs-lookup"><span data-stu-id="1758d-111">This command assigns the reserved IP address named ResIp14 to the service PipTestWestEurope.</span></span>
<span data-ttu-id="1758d-112">ResIp14 ist eine reservierte IP-Adresse in der Region West Europa.</span><span class="sxs-lookup"><span data-stu-id="1758d-112">ResIp14 is a reserved IP in the West Europe region.</span></span>

## <span data-ttu-id="1758d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1758d-113">PARAMETERS</span></span>

### <span data-ttu-id="1758d-114">-Information</span><span class="sxs-lookup"><span data-stu-id="1758d-114">-InformationAction</span></span>
<span data-ttu-id="1758d-115">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="1758d-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1758d-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1758d-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1758d-117">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="1758d-117">Continue</span></span>
- <span data-ttu-id="1758d-118">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="1758d-118">Ignore</span></span>
- <span data-ttu-id="1758d-119">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="1758d-119">Inquire</span></span>
- <span data-ttu-id="1758d-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1758d-120">SilentlyContinue</span></span>
- <span data-ttu-id="1758d-121">Beenden</span><span class="sxs-lookup"><span data-stu-id="1758d-121">Stop</span></span>
- <span data-ttu-id="1758d-122">Anhalten</span><span class="sxs-lookup"><span data-stu-id="1758d-122">Suspend</span></span>

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

### <span data-ttu-id="1758d-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1758d-123">-InformationVariable</span></span>
<span data-ttu-id="1758d-124">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="1758d-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1758d-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="1758d-125">-Profile</span></span>
<span data-ttu-id="1758d-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="1758d-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1758d-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="1758d-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1758d-128">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="1758d-128">-ReservedIPName</span></span>
<span data-ttu-id="1758d-129">Gibt den Namen der reservierten IP-Adresse an, die einem virtuellen Computer oder Dienst zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1758d-129">Specifies the name of the reserved IP address to associate with a virtual machine or service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1758d-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1758d-130">-ServiceName</span></span>
<span data-ttu-id="1758d-131">Gibt den Namen des Diensts an, der über die Bereitstellung verfügt, mit der die reservierte IP-Adresse verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="1758d-131">Specifies the name of the service that has the deployment with which to associate the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1758d-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="1758d-132">-Slot</span></span>
<span data-ttu-id="1758d-133">Gibt den Bereitstellungs Steckplatz an.</span><span class="sxs-lookup"><span data-stu-id="1758d-133">Specifies the deployment slot.</span></span>
<span data-ttu-id="1758d-134">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1758d-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1758d-135">Inszenierung</span><span class="sxs-lookup"><span data-stu-id="1758d-135">Staging</span></span>
- <span data-ttu-id="1758d-136">Produktions</span><span class="sxs-lookup"><span data-stu-id="1758d-136">Production</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1758d-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="1758d-137">-VirtualIPName</span></span>
<span data-ttu-id="1758d-138">Gibt den Namen einer vorhandenen VIP-Datei an, die mit einer reservierten IP verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="1758d-138">Specifies the name of an existing VIP to associate with a reserved IP.</span></span>
<span data-ttu-id="1758d-139">Weitere Informationen finden Sie unter Add-AzureVirtualIP zum Hinzufügen von VIPs zu Ihrem clouddienst.</span><span class="sxs-lookup"><span data-stu-id="1758d-139">See Add-AzureVirtualIP to add VIPs to your cloud service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1758d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1758d-140">CommonParameters</span></span>
<span data-ttu-id="1758d-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1758d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1758d-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1758d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1758d-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1758d-143">INPUTS</span></span>

## <span data-ttu-id="1758d-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1758d-144">OUTPUTS</span></span>

### <span data-ttu-id="1758d-145">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="1758d-145">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="1758d-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="1758d-146">NOTES</span></span>

## <span data-ttu-id="1758d-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1758d-147">RELATED LINKS</span></span>

[<span data-ttu-id="1758d-148">Remove-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="1758d-148">Remove-AzureReservedIPAssociation</span></span>](./Remove-AzureReservedIPAssociation.md)


