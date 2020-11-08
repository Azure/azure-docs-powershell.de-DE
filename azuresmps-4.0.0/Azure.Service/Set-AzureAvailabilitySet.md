---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E0590AD4-F67B-48EF-8657-8890A2204CB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 607cd288bcc9c86209a3ae0af569e964205f5cb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006273"
---
# <span data-ttu-id="ef355-101">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ef355-101">Set-AzureAvailabilitySet</span></span>

## <span data-ttu-id="ef355-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef355-102">SYNOPSIS</span></span>
<span data-ttu-id="ef355-103">Legt den Namen der verfügbaren Verfügbarkeit auf einem virtuellen Azure-Computer fest.</span><span class="sxs-lookup"><span data-stu-id="ef355-103">Sets the name of the availability set on an Azure virtual machine.</span></span>

## <span data-ttu-id="ef355-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef355-104">SYNTAX</span></span>

```
Set-AzureAvailabilitySet [-AvailabilitySetName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ef355-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef355-105">DESCRIPTION</span></span>
<span data-ttu-id="ef355-106">Das Cmdlet " **Set-AzureAvailabilitySet** " legt den Namen der verfügbaren Verfügbarkeit auf einem Azure Virtual Machine nach der Bereitstellung fest.</span><span class="sxs-lookup"><span data-stu-id="ef355-106">The **Set-AzureAvailabilitySet** cmdlet sets the name of the availability set on an Azure virtual machine after deployment.</span></span>

## <span data-ttu-id="ef355-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef355-107">EXAMPLES</span></span>

### <span data-ttu-id="ef355-108">Beispiel 1: Ändern des Namens eines Verfügbarkeits Satzes</span><span class="sxs-lookup"><span data-stu-id="ef355-108">Example 1: Modify the name of an availability set</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine24" | Set-AzureAvailabilitySet -AvailabilitySetName "AvailabilitySet14" | Update-AzureVM
```

<span data-ttu-id="ef355-109">Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 im Dienst ContosoService mit dem Cmdlet **Get-AzureVM** ab.</span><span class="sxs-lookup"><span data-stu-id="ef355-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="ef355-110">Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef355-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ef355-111">Dieses Cmdlet ändert den Namen des Verfügbarkeits Satzes für diesen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="ef355-111">That cmdlet modifies the name of the availability set for that virtual machine.</span></span>
<span data-ttu-id="ef355-112">Der Befehl aktualisiert den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="ef355-112">The command updates the virtual machine.</span></span>

## <span data-ttu-id="ef355-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef355-113">PARAMETERS</span></span>

### <span data-ttu-id="ef355-114">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="ef355-114">-AvailabilitySetName</span></span>
<span data-ttu-id="ef355-115">Gibt den Namen des Verfügbarkeits Satzes an, zu dem der virtuelle Computer gehört.</span><span class="sxs-lookup"><span data-stu-id="ef355-115">Specifies the name of the availability set to which the virtual machine belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef355-116">-Information</span><span class="sxs-lookup"><span data-stu-id="ef355-116">-InformationAction</span></span>
<span data-ttu-id="ef355-117">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="ef355-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ef355-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ef355-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ef355-119">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="ef355-119">Continue</span></span>
- <span data-ttu-id="ef355-120">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="ef355-120">Ignore</span></span>
- <span data-ttu-id="ef355-121">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="ef355-121">Inquire</span></span>
- <span data-ttu-id="ef355-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ef355-122">SilentlyContinue</span></span>
- <span data-ttu-id="ef355-123">Beenden</span><span class="sxs-lookup"><span data-stu-id="ef355-123">Stop</span></span>
- <span data-ttu-id="ef355-124">Anhalten</span><span class="sxs-lookup"><span data-stu-id="ef355-124">Suspend</span></span>

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

### <span data-ttu-id="ef355-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ef355-125">-InformationVariable</span></span>
<span data-ttu-id="ef355-126">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="ef355-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ef355-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="ef355-127">-Profile</span></span>
<span data-ttu-id="ef355-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ef355-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ef355-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ef355-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ef355-130">-VM</span><span class="sxs-lookup"><span data-stu-id="ef355-130">-VM</span></span>
<span data-ttu-id="ef355-131">Gibt die Konfiguration des virtuellen Computers an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ef355-131">Specifies the virtual machine configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ef355-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef355-132">CommonParameters</span></span>
<span data-ttu-id="ef355-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef355-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef355-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef355-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef355-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef355-135">INPUTS</span></span>

## <span data-ttu-id="ef355-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef355-136">OUTPUTS</span></span>

## <span data-ttu-id="ef355-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef355-137">NOTES</span></span>

## <span data-ttu-id="ef355-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef355-138">RELATED LINKS</span></span>

[<span data-ttu-id="ef355-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ef355-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="ef355-140">Remove-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ef355-140">Remove-AzureAvailabilitySet</span></span>](./Remove-AzureAvailabilitySet.md)


