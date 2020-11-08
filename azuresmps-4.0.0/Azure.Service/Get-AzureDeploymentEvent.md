---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6715B3E8-6880-4B86-B831-41664766E12B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 026e06a0071084f07ed0b609b8b686e6cba44cc5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005856"
---
# <span data-ttu-id="22137-101">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="22137-101">Get-AzureDeploymentEvent</span></span>

## <span data-ttu-id="22137-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22137-102">SYNOPSIS</span></span>
<span data-ttu-id="22137-103">Ruft Informationen zu den von Azure initiierten Ereignissen ab, die sich auf virtuelle Computer und Cloud-Dienste auswirken.</span><span class="sxs-lookup"><span data-stu-id="22137-103">Gets information about events that Azure initiates that impact virtual machines and cloud services.</span></span>

## <span data-ttu-id="22137-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22137-104">SYNTAX</span></span>

### <span data-ttu-id="22137-105">GetDeploymentEventBySlot (Standard)</span><span class="sxs-lookup"><span data-stu-id="22137-105">GetDeploymentEventBySlot (Default)</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="22137-106">GetDeploymentEventByName</span><span class="sxs-lookup"><span data-stu-id="22137-106">GetDeploymentEventByName</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [-DeploymentName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="22137-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22137-107">DESCRIPTION</span></span>
<span data-ttu-id="22137-108">Das Cmdlet " **Get-AzureDeploymentEvent** " Ruft Informationen zu Ereignissen ab, die Azure initiiert, die Auswirkungen auf virtuelle Computer und Cloud-Dienste haben.</span><span class="sxs-lookup"><span data-stu-id="22137-108">The **Get-AzureDeploymentEvent** cmdlet gets information regarding events that Azure initiates that impact virtual machines and cloud services.</span></span>
<span data-ttu-id="22137-109">Zu diesen Ereignissen gehören geplante Wartungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="22137-109">These events include planned maintenance events.</span></span>
<span data-ttu-id="22137-110">Dieses Cmdlet gibt eine Liste von Ereignissen zurück, die die Rolleninstanz oder den virtuellen Computer identifizieren, die sich auf den Grund für die Auswirkung und die Startzeit des Ereignisses auswirkt.</span><span class="sxs-lookup"><span data-stu-id="22137-110">This cmdlet returns a list of events that identify the role instance or virtual machine impacted, the reason for the impact, and the start time of the event.</span></span>

## <span data-ttu-id="22137-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22137-111">EXAMPLES</span></span>

### <span data-ttu-id="22137-112">1:</span><span class="sxs-lookup"><span data-stu-id="22137-112">1:</span></span>
```
Get-AzureDeploymentEvent -DeploymentName "ConstosoDeployment" -ServiceName "ContosoService"
```

## <span data-ttu-id="22137-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="22137-113">PARAMETERS</span></span>

### <span data-ttu-id="22137-114">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="22137-114">-DeploymentName</span></span>
<span data-ttu-id="22137-115">Gibt den Namen der Bereitstellung an, für die dieses Cmdlet Ereignisse abruft.</span><span class="sxs-lookup"><span data-stu-id="22137-115">Specifies the name of the deployment for which this cmdlet gets events.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22137-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="22137-116">-EndTime</span></span>
<span data-ttu-id="22137-117">Gibt die Endzeit für die geplanten Ereignisse an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="22137-117">Specifies the ending time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22137-118">-Information</span><span class="sxs-lookup"><span data-stu-id="22137-118">-InformationAction</span></span>
<span data-ttu-id="22137-119">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="22137-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="22137-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="22137-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="22137-121">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="22137-121">Continue</span></span>
- <span data-ttu-id="22137-122">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="22137-122">Ignore</span></span>
- <span data-ttu-id="22137-123">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="22137-123">Inquire</span></span>
- <span data-ttu-id="22137-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="22137-124">SilentlyContinue</span></span>
- <span data-ttu-id="22137-125">Beenden</span><span class="sxs-lookup"><span data-stu-id="22137-125">Stop</span></span>
- <span data-ttu-id="22137-126">Anhalten</span><span class="sxs-lookup"><span data-stu-id="22137-126">Suspend</span></span>

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

### <span data-ttu-id="22137-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="22137-127">-InformationVariable</span></span>
<span data-ttu-id="22137-128">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="22137-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="22137-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="22137-129">-Profile</span></span>
<span data-ttu-id="22137-130">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="22137-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="22137-131">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="22137-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="22137-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="22137-132">-ServiceName</span></span>
<span data-ttu-id="22137-133">Gibt den Namen des gehosteten Diensts an, für den dieses Cmdlet geplante Ereignisse erhält.</span><span class="sxs-lookup"><span data-stu-id="22137-133">Specifies the name of the hosted service for which this cmdlet gets scheduled events.</span></span>

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

### <span data-ttu-id="22137-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="22137-134">-Slot</span></span>
<span data-ttu-id="22137-135">Gibt die Umgebung der Bereitstellung an, für die dieses Cmdlet geplante Ereignisse erhält.</span><span class="sxs-lookup"><span data-stu-id="22137-135">Specifies the environment of the deployment for which this cmdlet gets scheduled events.</span></span>
<span data-ttu-id="22137-136">Gültige Werte sind: Staging und Production.</span><span class="sxs-lookup"><span data-stu-id="22137-136">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="22137-137">Der Standardwert ist Production.</span><span class="sxs-lookup"><span data-stu-id="22137-137">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventBySlot
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22137-138">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="22137-138">-StartTime</span></span>
<span data-ttu-id="22137-139">Gibt die Startzeit für die geplanten Ereignisse an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="22137-139">Specifies the starting time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22137-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22137-140">CommonParameters</span></span>
<span data-ttu-id="22137-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22137-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22137-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22137-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22137-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22137-143">INPUTS</span></span>

## <span data-ttu-id="22137-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22137-144">OUTPUTS</span></span>

## <span data-ttu-id="22137-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="22137-145">NOTES</span></span>

## <span data-ttu-id="22137-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22137-146">RELATED LINKS</span></span>

[<span data-ttu-id="22137-147">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="22137-147">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)


