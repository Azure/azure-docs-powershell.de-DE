---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 734C98C1-0EF7-43E5-AB6F-A1C625FF9CE7
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9713c8b39fa4e2842cdf1cfcbfe962ead86d729
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005741"
---
# <span data-ttu-id="c8984-101">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="c8984-101">Get-AzureVMAccessExtension</span></span>

## <span data-ttu-id="c8984-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8984-102">SYNOPSIS</span></span>
<span data-ttu-id="c8984-103">Ruft die VMAccess-Erweiterung ab, die auf einem virtuellen Computer angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c8984-103">Gets the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="c8984-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8984-104">SYNTAX</span></span>

```
Get-AzureVMAccessExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c8984-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8984-105">DESCRIPTION</span></span>
<span data-ttu-id="c8984-106">Das Cmdlet " **Get-AzureVMAccessExtension** " Ruft die VMAccess-Erweiterung ab, die auf einem virtuellen Computer angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c8984-106">The **Get-AzureVMAccessExtension** cmdlet gets the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="c8984-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8984-107">EXAMPLES</span></span>

### <span data-ttu-id="c8984-108">Beispiel 1: Abrufen der VMAccess-Erweiterung für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="c8984-108">Example 1: Get the VMAccess extension for a virtual machine</span></span>
```
PS C:\> Get-AzureVMAccessExtension -VM $VM;
```

<span data-ttu-id="c8984-109">Dieser Befehl ruft die VMAccess-Erweiterung für einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="c8984-109">This command gets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="c8984-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8984-110">PARAMETERS</span></span>

### <span data-ttu-id="c8984-111">-Information</span><span class="sxs-lookup"><span data-stu-id="c8984-111">-InformationAction</span></span>
<span data-ttu-id="c8984-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="c8984-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c8984-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c8984-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8984-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="c8984-114">Continue</span></span>
- <span data-ttu-id="c8984-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="c8984-115">Ignore</span></span>
- <span data-ttu-id="c8984-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="c8984-116">Inquire</span></span>
- <span data-ttu-id="c8984-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c8984-117">SilentlyContinue</span></span>
- <span data-ttu-id="c8984-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="c8984-118">Stop</span></span>
- <span data-ttu-id="c8984-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="c8984-119">Suspend</span></span>

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

### <span data-ttu-id="c8984-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c8984-120">-InformationVariable</span></span>
<span data-ttu-id="c8984-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="c8984-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c8984-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="c8984-122">-Profile</span></span>
<span data-ttu-id="c8984-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c8984-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c8984-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c8984-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c8984-125">-VM</span><span class="sxs-lookup"><span data-stu-id="c8984-125">-VM</span></span>
<span data-ttu-id="c8984-126">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="c8984-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="c8984-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8984-127">CommonParameters</span></span>
<span data-ttu-id="c8984-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8984-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8984-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8984-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8984-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8984-130">INPUTS</span></span>

## <span data-ttu-id="c8984-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8984-131">OUTPUTS</span></span>

## <span data-ttu-id="c8984-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8984-132">NOTES</span></span>

## <span data-ttu-id="c8984-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8984-133">RELATED LINKS</span></span>

[<span data-ttu-id="c8984-134">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="c8984-134">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)

[<span data-ttu-id="c8984-135">Satz-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="c8984-135">Set-AzureVMAccessExtension</span></span>](./Set-AzureVMAccessExtension.md)


