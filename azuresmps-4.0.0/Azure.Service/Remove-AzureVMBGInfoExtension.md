---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C735528-3844-452F-983B-41AC5CD4E414
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ea39b2c06a5daf7540009f480e7c2ec211e7f47
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005714"
---
# <span data-ttu-id="b4f71-101">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="b4f71-101">Remove-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="b4f71-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4f71-102">SYNOPSIS</span></span>
<span data-ttu-id="b4f71-103">Entfernt die auf einem virtuellen Computer angewendete BGInfo-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="b4f71-103">Removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="b4f71-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4f71-104">SYNTAX</span></span>

```
Remove-AzureVMBGInfoExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b4f71-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4f71-105">DESCRIPTION</span></span>
<span data-ttu-id="b4f71-106">Das Cmdlet **Remove-AzureVMBGInfoExtension** entfernt die auf einem virtuellen Computer angewendete BGInfo-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="b4f71-106">The **Remove-AzureVMBGInfoExtension** cmdlet removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="b4f71-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4f71-107">EXAMPLES</span></span>

### <span data-ttu-id="b4f71-108">Beispiel 1: Entfernen der BGInfo-Erweiterung auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="b4f71-108">Example 1: Remove the BGInfo extension on a virtual machine</span></span>
```
PS C:\> Remove-AzureVMBGInfoExtension -VM $VM;
```

<span data-ttu-id="b4f71-109">Mit diesem Befehl wird die auf einem virtuellen Computer angewendete BGInfo-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="b4f71-109">This command removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="b4f71-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4f71-110">PARAMETERS</span></span>

### <span data-ttu-id="b4f71-111">-Information</span><span class="sxs-lookup"><span data-stu-id="b4f71-111">-InformationAction</span></span>
<span data-ttu-id="b4f71-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="b4f71-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b4f71-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b4f71-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4f71-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="b4f71-114">Continue</span></span>
- <span data-ttu-id="b4f71-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="b4f71-115">Ignore</span></span>
- <span data-ttu-id="b4f71-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="b4f71-116">Inquire</span></span>
- <span data-ttu-id="b4f71-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b4f71-117">SilentlyContinue</span></span>
- <span data-ttu-id="b4f71-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="b4f71-118">Stop</span></span>
- <span data-ttu-id="b4f71-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="b4f71-119">Suspend</span></span>

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

### <span data-ttu-id="b4f71-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b4f71-120">-InformationVariable</span></span>
<span data-ttu-id="b4f71-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="b4f71-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b4f71-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="b4f71-122">-Profile</span></span>
<span data-ttu-id="b4f71-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b4f71-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4f71-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b4f71-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4f71-125">-VM</span><span class="sxs-lookup"><span data-stu-id="b4f71-125">-VM</span></span>
<span data-ttu-id="b4f71-126">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="b4f71-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="b4f71-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4f71-127">CommonParameters</span></span>
<span data-ttu-id="b4f71-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4f71-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4f71-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4f71-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4f71-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4f71-130">INPUTS</span></span>

## <span data-ttu-id="b4f71-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4f71-131">OUTPUTS</span></span>

## <span data-ttu-id="b4f71-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4f71-132">NOTES</span></span>

## <span data-ttu-id="b4f71-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4f71-133">RELATED LINKS</span></span>

[<span data-ttu-id="b4f71-134">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="b4f71-134">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="b4f71-135">Satz-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="b4f71-135">Set-AzureVMBGInfoExtension</span></span>](./Set-AzureVMBGInfoExtension.md)


