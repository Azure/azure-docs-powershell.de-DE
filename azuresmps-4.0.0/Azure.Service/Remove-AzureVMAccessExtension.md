---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 93A8B8EC-4ED0-4C87-AF92-9A246ECEF4F0
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1b516722b0555c84400c0c8f5acd7f1b5c43d9c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005716"
---
# <span data-ttu-id="9f3e3-101">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9f3e3-101">Remove-AzureVMAccessExtension</span></span>

## <span data-ttu-id="9f3e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9f3e3-102">SYNOPSIS</span></span>
<span data-ttu-id="9f3e3-103">Entfernt die auf einem virtuellen Computer angewendete VMAccess-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="9f3e3-103">Removes the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="9f3e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f3e3-104">SYNTAX</span></span>

```
Remove-AzureVMAccessExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9f3e3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f3e3-105">DESCRIPTION</span></span>
<span data-ttu-id="9f3e3-106">Das Cmdlet **Remove-AzureVMAccessExtension** entfernt die auf einem virtuellen Computer angewendete VMAccess-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="9f3e3-106">The **Remove-AzureVMAccessExtension** cmdlet removes the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="9f3e3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f3e3-107">EXAMPLES</span></span>

### <span data-ttu-id="9f3e3-108">Beispiel 1: Entfernen einer VMAccess-Erweiterung von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="9f3e3-108">Example 1: Remove a VMAccess extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMAccessExtension -VM $VM;
```

<span data-ttu-id="9f3e3-109">Mit diesem Befehl wird eine VMAccess-Erweiterung von einem virtuellen Computer entfernt.</span><span class="sxs-lookup"><span data-stu-id="9f3e3-109">This command removes a VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="9f3e3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f3e3-110">PARAMETERS</span></span>

### <span data-ttu-id="9f3e3-111">-Information</span><span class="sxs-lookup"><span data-stu-id="9f3e3-111">-InformationAction</span></span>
<span data-ttu-id="9f3e3-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="9f3e3-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9f3e3-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9f3e3-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9f3e3-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="9f3e3-114">Continue</span></span>
- <span data-ttu-id="9f3e3-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="9f3e3-115">Ignore</span></span>
- <span data-ttu-id="9f3e3-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="9f3e3-116">Inquire</span></span>
- <span data-ttu-id="9f3e3-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9f3e3-117">SilentlyContinue</span></span>
- <span data-ttu-id="9f3e3-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="9f3e3-118">Stop</span></span>
- <span data-ttu-id="9f3e3-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="9f3e3-119">Suspend</span></span>

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

### <span data-ttu-id="9f3e3-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9f3e3-120">-InformationVariable</span></span>
<span data-ttu-id="9f3e3-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="9f3e3-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9f3e3-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="9f3e3-122">-Profile</span></span>
<span data-ttu-id="9f3e3-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="9f3e3-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9f3e3-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="9f3e3-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9f3e3-125">-VM</span><span class="sxs-lookup"><span data-stu-id="9f3e3-125">-VM</span></span>
<span data-ttu-id="9f3e3-126">Gibt das Objekt des beständigen virtuellen Computers an, von dem dieses Cmdlet die VMAccess-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="9f3e3-126">Specifies the persistent virtual machine object that this cmdlet removes the VMAccess extension from.</span></span>

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

### <span data-ttu-id="9f3e3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f3e3-127">CommonParameters</span></span>
<span data-ttu-id="9f3e3-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f3e3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f3e3-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f3e3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f3e3-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9f3e3-130">INPUTS</span></span>

## <span data-ttu-id="9f3e3-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9f3e3-131">OUTPUTS</span></span>

## <span data-ttu-id="9f3e3-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="9f3e3-132">NOTES</span></span>

## <span data-ttu-id="9f3e3-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9f3e3-133">RELATED LINKS</span></span>

[<span data-ttu-id="9f3e3-134">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9f3e3-134">Get-AzureVMAccessExtension</span></span>](./Get-AzureVMAccessExtension.md)

[<span data-ttu-id="9f3e3-135">Satz-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9f3e3-135">Set-AzureVMAccessExtension</span></span>](./Set-AzureVMAccessExtension.md)


