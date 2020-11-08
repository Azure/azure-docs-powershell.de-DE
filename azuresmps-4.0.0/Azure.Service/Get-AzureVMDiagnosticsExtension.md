---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 97E1A3FF-E479-44CD-8147-15408DF3F79A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f8290b0e4f40305495b535b28b2a8f61d7911ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006749"
---
# <span data-ttu-id="ba20c-101">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ba20c-101">Get-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="ba20c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba20c-102">SYNOPSIS</span></span>
<span data-ttu-id="ba20c-103">Ruft die Einstellungen der Azure Diagnostics-Erweiterung auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="ba20c-103">Gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="ba20c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba20c-104">SYNTAX</span></span>

```
Get-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ba20c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba20c-105">DESCRIPTION</span></span>
<span data-ttu-id="ba20c-106">Das Cmdlet " **Get-AzureVMDiagnosticsExtension** " Ruft die Einstellungen der Microsoft Azure Diagnostics-Erweiterung auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="ba20c-106">The **Get-AzureVMDiagnosticsExtension** cmdlet gets the settings of the Microsoft Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="ba20c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba20c-107">EXAMPLES</span></span>

### <span data-ttu-id="ba20c-108">Beispiel 1: Abrufen der auf einen virtuellen Computer angewendeten Diagnose Erweiterung</span><span class="sxs-lookup"><span data-stu-id="ba20c-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureVMDiagnosticsExtension -VM $VM
```

<span data-ttu-id="ba20c-109">Dieser Befehl ruft die auf den angegebenen virtuellen Computer angewendete Diagnose Erweiterung ab, wie Sie in der Variablen $VM gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ba20c-109">This command gets the diagnostics extension applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="ba20c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba20c-110">PARAMETERS</span></span>

### <span data-ttu-id="ba20c-111">-Information</span><span class="sxs-lookup"><span data-stu-id="ba20c-111">-InformationAction</span></span>
<span data-ttu-id="ba20c-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="ba20c-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ba20c-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ba20c-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ba20c-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="ba20c-114">Continue</span></span>
- <span data-ttu-id="ba20c-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="ba20c-115">Ignore</span></span>
- <span data-ttu-id="ba20c-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="ba20c-116">Inquire</span></span>
- <span data-ttu-id="ba20c-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ba20c-117">SilentlyContinue</span></span>
- <span data-ttu-id="ba20c-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="ba20c-118">Stop</span></span>
- <span data-ttu-id="ba20c-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="ba20c-119">Suspend</span></span>

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

### <span data-ttu-id="ba20c-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ba20c-120">-InformationVariable</span></span>
<span data-ttu-id="ba20c-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="ba20c-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ba20c-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="ba20c-122">-Profile</span></span>
<span data-ttu-id="ba20c-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ba20c-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ba20c-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ba20c-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ba20c-125">-VM</span><span class="sxs-lookup"><span data-stu-id="ba20c-125">-VM</span></span>
<span data-ttu-id="ba20c-126">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="ba20c-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="ba20c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba20c-127">CommonParameters</span></span>
<span data-ttu-id="ba20c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba20c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba20c-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba20c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba20c-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba20c-130">INPUTS</span></span>

## <span data-ttu-id="ba20c-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba20c-131">OUTPUTS</span></span>

## <span data-ttu-id="ba20c-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba20c-132">NOTES</span></span>

## <span data-ttu-id="ba20c-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba20c-133">RELATED LINKS</span></span>

[<span data-ttu-id="ba20c-134">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ba20c-134">Remove-AzureVMDiagnosticsExtension</span></span>](./Remove-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="ba20c-135">Satz-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ba20c-135">Set-AzureVMDiagnosticsExtension</span></span>](./Set-AzureVMDiagnosticsExtension.md)


