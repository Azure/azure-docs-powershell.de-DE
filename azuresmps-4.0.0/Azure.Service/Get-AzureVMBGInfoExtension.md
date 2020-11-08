---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4CB958B-AC85-4036-A6D6-002FAF40BB66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e74be3310b895ef4c941a59541a64f9c6d1b279
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005738"
---
# <span data-ttu-id="02170-101">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="02170-101">Get-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="02170-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02170-102">SYNOPSIS</span></span>
<span data-ttu-id="02170-103">Ruft die BGInfo-Erweiterung ab, die auf einem virtuellen Computer angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="02170-103">Gets the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="02170-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="02170-104">SYNTAX</span></span>

```
Get-AzureVMBGInfoExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="02170-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02170-105">DESCRIPTION</span></span>
<span data-ttu-id="02170-106">Das Cmdlet " **Get-AzureVMBGInfoExtension** " Ruft die BGInfo-Erweiterung ab, die auf einem virtuellen Computer angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="02170-106">The **Get-AzureVMBGInfoExtension** cmdlet gets the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="02170-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02170-107">EXAMPLES</span></span>

### <span data-ttu-id="02170-108">Beispiel 1: Abrufen der auf einem angegebenen virtuellen Computer angewendeten BGInfo-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="02170-108">Example 1: Get the BGInfo extension applied on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVMBGInfoExtension -VM $VM;
```

<span data-ttu-id="02170-109">Dieser Befehl ruft die BGInfo-Erweiterung ab, die auf einem angegebenen virtuellen Computer angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="02170-109">This command gets the BGInfo extension applied on a specified virtual machine</span></span>

## <span data-ttu-id="02170-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="02170-110">PARAMETERS</span></span>

### <span data-ttu-id="02170-111">-Information</span><span class="sxs-lookup"><span data-stu-id="02170-111">-InformationAction</span></span>
<span data-ttu-id="02170-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="02170-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="02170-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="02170-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="02170-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="02170-114">Continue</span></span>
- <span data-ttu-id="02170-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="02170-115">Ignore</span></span>
- <span data-ttu-id="02170-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="02170-116">Inquire</span></span>
- <span data-ttu-id="02170-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="02170-117">SilentlyContinue</span></span>
- <span data-ttu-id="02170-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="02170-118">Stop</span></span>
- <span data-ttu-id="02170-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="02170-119">Suspend</span></span>

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

### <span data-ttu-id="02170-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="02170-120">-InformationVariable</span></span>
<span data-ttu-id="02170-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="02170-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="02170-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="02170-122">-Profile</span></span>
<span data-ttu-id="02170-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="02170-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="02170-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="02170-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="02170-125">-VM</span><span class="sxs-lookup"><span data-stu-id="02170-125">-VM</span></span>
<span data-ttu-id="02170-126">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="02170-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="02170-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02170-127">CommonParameters</span></span>
<span data-ttu-id="02170-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02170-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02170-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02170-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02170-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02170-130">INPUTS</span></span>

## <span data-ttu-id="02170-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02170-131">OUTPUTS</span></span>

## <span data-ttu-id="02170-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="02170-132">NOTES</span></span>

## <span data-ttu-id="02170-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02170-133">RELATED LINKS</span></span>

[<span data-ttu-id="02170-134">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="02170-134">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)

[<span data-ttu-id="02170-135">Satz-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="02170-135">Set-AzureVMBGInfoExtension</span></span>](./Set-AzureVMBGInfoExtension.md)


