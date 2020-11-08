---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A46832F2-CA94-43A4-AFF9-70D02851713F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1146cee245693c19b333af5a4efd9fcc1bebc725
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005711"
---
# <span data-ttu-id="f1f57-101">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f1f57-101">Remove-AzureVMChefExtension</span></span>

## <span data-ttu-id="f1f57-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1f57-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f57-103">Entfernt die auf dem virtuellen Computer angewendete Erweiterung des Chefkochs.</span><span class="sxs-lookup"><span data-stu-id="f1f57-103">Removes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="f1f57-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1f57-104">SYNTAX</span></span>

```
Remove-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f1f57-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1f57-105">DESCRIPTION</span></span>
<span data-ttu-id="f1f57-106">Das Cmdlet **Remove-AzureVMChefExtension** löscht die auf dem virtuellen Computer angewendete Chefkoch-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="f1f57-106">The **Remove-AzureVMChefExtension** cmdlet deletes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="f1f57-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1f57-107">EXAMPLES</span></span>

### <span data-ttu-id="f1f57-108">Beispiel 1: Entfernen der auf dem angegebenen virtuellen Computer angewendeten Chefkoch-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="f1f57-108">Example 1: Remove the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Remove-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="f1f57-109">Mit diesem Befehl wird die auf dem virtuellen Computer angewendete Erweiterung "Chef" entfernt.</span><span class="sxs-lookup"><span data-stu-id="f1f57-109">This command removes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="f1f57-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1f57-110">PARAMETERS</span></span>

### <span data-ttu-id="f1f57-111">-Information</span><span class="sxs-lookup"><span data-stu-id="f1f57-111">-InformationAction</span></span>
<span data-ttu-id="f1f57-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="f1f57-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f1f57-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f1f57-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1f57-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="f1f57-114">Continue</span></span>
- <span data-ttu-id="f1f57-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="f1f57-115">Ignore</span></span>
- <span data-ttu-id="f1f57-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="f1f57-116">Inquire</span></span>
- <span data-ttu-id="f1f57-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f1f57-117">SilentlyContinue</span></span>
- <span data-ttu-id="f1f57-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="f1f57-118">Stop</span></span>
- <span data-ttu-id="f1f57-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="f1f57-119">Suspend</span></span>

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

### <span data-ttu-id="f1f57-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f1f57-120">-InformationVariable</span></span>
<span data-ttu-id="f1f57-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="f1f57-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f1f57-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="f1f57-122">-Profile</span></span>
<span data-ttu-id="f1f57-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="f1f57-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f1f57-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f1f57-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f1f57-125">-VM</span><span class="sxs-lookup"><span data-stu-id="f1f57-125">-VM</span></span>
<span data-ttu-id="f1f57-126">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="f1f57-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="f1f57-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f57-127">CommonParameters</span></span>
<span data-ttu-id="f1f57-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1f57-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f57-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1f57-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f57-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1f57-130">INPUTS</span></span>

## <span data-ttu-id="f1f57-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1f57-131">OUTPUTS</span></span>

## <span data-ttu-id="f1f57-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1f57-132">NOTES</span></span>

## <span data-ttu-id="f1f57-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1f57-133">RELATED LINKS</span></span>

[<span data-ttu-id="f1f57-134">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f1f57-134">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="f1f57-135">Satz-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f1f57-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


