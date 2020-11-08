---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A6964C80-1991-46FC-84C8-5B00616386BE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e43f841fea77626c18edbda541fa011e95faceb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006342"
---
# <span data-ttu-id="156cd-101">Remove-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="156cd-101">Remove-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="156cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="156cd-102">SYNOPSIS</span></span>
<span data-ttu-id="156cd-103">Entfernt die Zuordnung aus der reservierten IP-Adresse zum VM-oder clouddienst.</span><span class="sxs-lookup"><span data-stu-id="156cd-103">Removes the association from the reserved IP address to the VM or cloud service.</span></span>

## <span data-ttu-id="156cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="156cd-104">SYNTAX</span></span>

```
Remove-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="156cd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="156cd-105">DESCRIPTION</span></span>
<span data-ttu-id="156cd-106">Das Cmdlet **Remove-AzureReservedIPAssociation** trennt eine reservierte IP-Adresse von einem virtuellen Computer (VM) oder einem clouddienst.</span><span class="sxs-lookup"><span data-stu-id="156cd-106">The **Remove-AzureReservedIPAssociation** cmdlet disassociates a reserved IP address from a virtual machine (VM) or Cloud Service.</span></span>
<span data-ttu-id="156cd-107">Nach Abschluss des Vorgangs ist die reservierte IP-Adresse kostenlos, und die VM/VIP Ruft eine dynamische öffentliche IP-Adresse aus dem Azure-Inventar ab.</span><span class="sxs-lookup"><span data-stu-id="156cd-107">When the operation completes, the reserved IP address is free and the VM/VIP gets a dynamic public IP Address from the Azure Inventory.</span></span>

## <span data-ttu-id="156cd-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="156cd-108">EXAMPLES</span></span>

### <span data-ttu-id="156cd-109">Beispiel 1: Entfernen einer reservierten IP-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="156cd-109">Example 1: Remove a reserved IP association</span></span>
```
PS C:\> Remove-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="156cd-110">Dieser Befehl trennt die reservierte IP-Adresse namens ResIp14 vom Dienst mit dem Namen PipTestWestEurope.</span><span class="sxs-lookup"><span data-stu-id="156cd-110">This command disassociates the reserved IP address named ResIp14 from the service named PipTestWestEurope.</span></span>
<span data-ttu-id="156cd-111">PipTestWestEurope wird eine neue dynamische VIP-Nummer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="156cd-111">PipTestWestEurope will be assigned a new dynamic VIP.</span></span>

## <span data-ttu-id="156cd-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="156cd-112">PARAMETERS</span></span>

### <span data-ttu-id="156cd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="156cd-113">-Force</span></span>
<span data-ttu-id="156cd-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="156cd-114">Forces the command to run without asking for user confirmation.</span></span>

<span data-ttu-id="156cd-115">Verwenden Sie dieses Flag, um Warnmeldungen zu umgehen, wenn die reservierte IP-Zuordnung entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="156cd-115">Use this flag to bypass warning messages when removing the reserved IP association.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="156cd-116">-Information</span><span class="sxs-lookup"><span data-stu-id="156cd-116">-InformationAction</span></span>
<span data-ttu-id="156cd-117">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="156cd-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="156cd-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="156cd-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="156cd-119">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="156cd-119">Continue</span></span>
- <span data-ttu-id="156cd-120">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="156cd-120">Ignore</span></span>
- <span data-ttu-id="156cd-121">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="156cd-121">Inquire</span></span>
- <span data-ttu-id="156cd-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="156cd-122">SilentlyContinue</span></span>
- <span data-ttu-id="156cd-123">Beenden</span><span class="sxs-lookup"><span data-stu-id="156cd-123">Stop</span></span>
- <span data-ttu-id="156cd-124">Anhalten</span><span class="sxs-lookup"><span data-stu-id="156cd-124">Suspend</span></span>

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

### <span data-ttu-id="156cd-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="156cd-125">-InformationVariable</span></span>
<span data-ttu-id="156cd-126">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="156cd-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="156cd-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="156cd-127">-Profile</span></span>
<span data-ttu-id="156cd-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="156cd-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="156cd-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="156cd-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="156cd-130">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="156cd-130">-ReservedIPName</span></span>
<span data-ttu-id="156cd-131">Gibt den Namen der reservierten IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="156cd-131">Specifies the name of the reserved IP address.</span></span>

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

### <span data-ttu-id="156cd-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="156cd-132">-ServiceName</span></span>
<span data-ttu-id="156cd-133">Gibt den Namen des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="156cd-133">Specifies the  name of the service.</span></span>

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

### <span data-ttu-id="156cd-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="156cd-134">-Slot</span></span>
<span data-ttu-id="156cd-135">Gibt die Bereitstellungsumgebung an.</span><span class="sxs-lookup"><span data-stu-id="156cd-135">Specifies the deployment environment.</span></span>
<span data-ttu-id="156cd-136">Die akzeptablen Werte für diesen Parameter sind: Production, Staging.</span><span class="sxs-lookup"><span data-stu-id="156cd-136">The acceptable values for this parameter are: Production, Staging.</span></span>

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

### <span data-ttu-id="156cd-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="156cd-137">-VirtualIPName</span></span>
<span data-ttu-id="156cd-138">Gibt eine virtuelle IP-Adresse an, aus der die Zuordnung zu einem Dienst oder einem virtuellen Computer entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="156cd-138">Specifies a virtual IP address from which to remove the association with a service or VM.</span></span>

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

### <span data-ttu-id="156cd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="156cd-139">CommonParameters</span></span>
<span data-ttu-id="156cd-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="156cd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="156cd-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="156cd-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="156cd-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="156cd-142">INPUTS</span></span>

## <span data-ttu-id="156cd-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="156cd-143">OUTPUTS</span></span>

### <span data-ttu-id="156cd-144">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="156cd-144">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="156cd-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="156cd-145">NOTES</span></span>

## <span data-ttu-id="156cd-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="156cd-146">RELATED LINKS</span></span>

[<span data-ttu-id="156cd-147">Satz-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="156cd-147">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


