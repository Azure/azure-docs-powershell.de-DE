---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A269A53-8FB2-4D4E-8FBB-A84BE658F75F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 002834bda663dda1c9ebe5f24bb0f1aa0007655c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006538"
---
# <span data-ttu-id="96e0b-101">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="96e0b-101">Get-AzureOSDisk</span></span>

## <span data-ttu-id="96e0b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="96e0b-103">Ruft den Betriebssystemdatenträger eines Azure Virtual Machine ab.</span><span class="sxs-lookup"><span data-stu-id="96e0b-103">Gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="96e0b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96e0b-104">SYNTAX</span></span>

```
Get-AzureOSDisk -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="96e0b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96e0b-105">DESCRIPTION</span></span>
<span data-ttu-id="96e0b-106">Das Cmdlet " **Get-AzureOSDisk** " Ruft den Betriebssystemdatenträger eines Azure Virtual Machine ab.</span><span class="sxs-lookup"><span data-stu-id="96e0b-106">The **Get-AzureOSDisk** cmdlet gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="96e0b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96e0b-107">EXAMPLES</span></span>

### <span data-ttu-id="96e0b-108">Beispiel 1: Abrufen eines Betriebssystemdatenträgers</span><span class="sxs-lookup"><span data-stu-id="96e0b-108">Example 1: Get an operating system disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Get-AzureOSDisk
```

<span data-ttu-id="96e0b-109">Dieser Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine02 im Dienst ContosoService mit dem Cmdlet **Get-AzureVM** ab.</span><span class="sxs-lookup"><span data-stu-id="96e0b-109">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="96e0b-110">Der Befehl übergibt den virtuellen Computer mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96e0b-110">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="96e0b-111">Das aktuelle Cmdlet ruft den Betriebssystemdatenträger dieses virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="96e0b-111">The current cmdlet gets the operating system disk of that virtual machine.</span></span>

## <span data-ttu-id="96e0b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="96e0b-112">PARAMETERS</span></span>

### <span data-ttu-id="96e0b-113">-Information</span><span class="sxs-lookup"><span data-stu-id="96e0b-113">-InformationAction</span></span>
<span data-ttu-id="96e0b-114">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="96e0b-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="96e0b-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="96e0b-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="96e0b-116">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="96e0b-116">Continue</span></span>
- <span data-ttu-id="96e0b-117">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="96e0b-117">Ignore</span></span>
- <span data-ttu-id="96e0b-118">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="96e0b-118">Inquire</span></span>
- <span data-ttu-id="96e0b-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="96e0b-119">SilentlyContinue</span></span>
- <span data-ttu-id="96e0b-120">Beenden</span><span class="sxs-lookup"><span data-stu-id="96e0b-120">Stop</span></span>
- <span data-ttu-id="96e0b-121">Anhalten</span><span class="sxs-lookup"><span data-stu-id="96e0b-121">Suspend</span></span>

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

### <span data-ttu-id="96e0b-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="96e0b-122">-InformationVariable</span></span>
<span data-ttu-id="96e0b-123">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="96e0b-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="96e0b-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="96e0b-124">-Profile</span></span>
<span data-ttu-id="96e0b-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="96e0b-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="96e0b-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="96e0b-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="96e0b-127">-VM</span><span class="sxs-lookup"><span data-stu-id="96e0b-127">-VM</span></span>
<span data-ttu-id="96e0b-128">Gibt den virtuellen Computer an, für den dieses Cmdlet den Betriebssystemdatenträger abruft.</span><span class="sxs-lookup"><span data-stu-id="96e0b-128">Specifies the virtual machine for which this cmdlet gets the operating system disk.</span></span>
<span data-ttu-id="96e0b-129">Verwenden Sie das Cmdlet **Get-AzureVM** , um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="96e0b-129">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="96e0b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e0b-130">CommonParameters</span></span>
<span data-ttu-id="96e0b-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96e0b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e0b-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96e0b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e0b-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96e0b-133">INPUTS</span></span>

## <span data-ttu-id="96e0b-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96e0b-134">OUTPUTS</span></span>

## <span data-ttu-id="96e0b-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="96e0b-135">NOTES</span></span>

## <span data-ttu-id="96e0b-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96e0b-136">RELATED LINKS</span></span>

[<span data-ttu-id="96e0b-137">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="96e0b-137">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="96e0b-138">Satz-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="96e0b-138">Set-AzureOSDisk</span></span>](./Set-AzureOSDisk.md)


