---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9AAEDD44-D11E-47A3-BF0F-D8445A018759
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46dbd7ec58cc112e6573fa3d9c6a52fe0ee14b33
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006649"
---
# <span data-ttu-id="aec38-101">Remove-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="aec38-101">Remove-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="aec38-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aec38-102">SYNOPSIS</span></span>
<span data-ttu-id="aec38-103">Entfernt die auf einem virtuellen Computer angewendete Marionetten Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="aec38-103">Removes the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="aec38-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aec38-104">SYNTAX</span></span>

```
Remove-AzureVMPuppetExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="aec38-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aec38-105">DESCRIPTION</span></span>
<span data-ttu-id="aec38-106">Das Cmdlet **Remove-AzureVMPuppetExtension** entfernt die auf einem virtuellen Computer angewendete Marionetten Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="aec38-106">The **Remove-AzureVMPuppetExtension** cmdlet removes the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="aec38-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aec38-107">EXAMPLES</span></span>

### <span data-ttu-id="aec38-108">Beispiel 1: Entfernen der auf einem virtuellen Computer angewendeten Marionetten Erweiterung</span><span class="sxs-lookup"><span data-stu-id="aec38-108">Example 1: Remove the Puppet extension applied on a virtual machine</span></span>
```
PS C:\> Remove-AzureVMPuppetExtension -VM $VM;
```

<span data-ttu-id="aec38-109">Mit diesem Befehl wird die auf dem angegebenen virtuellen Computer angewendete Marionetten Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="aec38-109">This command removes the Puppet extension applied on the specified virtual machine.</span></span>

## <span data-ttu-id="aec38-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="aec38-110">PARAMETERS</span></span>

### <span data-ttu-id="aec38-111">-Information</span><span class="sxs-lookup"><span data-stu-id="aec38-111">-InformationAction</span></span>
<span data-ttu-id="aec38-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="aec38-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="aec38-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="aec38-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aec38-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="aec38-114">Continue</span></span>
- <span data-ttu-id="aec38-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="aec38-115">Ignore</span></span>
- <span data-ttu-id="aec38-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="aec38-116">Inquire</span></span>
- <span data-ttu-id="aec38-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="aec38-117">SilentlyContinue</span></span>
- <span data-ttu-id="aec38-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="aec38-118">Stop</span></span>
- <span data-ttu-id="aec38-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="aec38-119">Suspend</span></span>

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

### <span data-ttu-id="aec38-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="aec38-120">-InformationVariable</span></span>
<span data-ttu-id="aec38-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="aec38-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="aec38-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="aec38-122">-Profile</span></span>
<span data-ttu-id="aec38-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="aec38-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aec38-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="aec38-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aec38-125">-VM</span><span class="sxs-lookup"><span data-stu-id="aec38-125">-VM</span></span>
<span data-ttu-id="aec38-126">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="aec38-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="aec38-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec38-127">CommonParameters</span></span>
<span data-ttu-id="aec38-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aec38-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec38-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aec38-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec38-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aec38-130">INPUTS</span></span>

## <span data-ttu-id="aec38-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aec38-131">OUTPUTS</span></span>

## <span data-ttu-id="aec38-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="aec38-132">NOTES</span></span>

## <span data-ttu-id="aec38-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aec38-133">RELATED LINKS</span></span>

[<span data-ttu-id="aec38-134">Get-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="aec38-134">Get-AzureVMPuppetExtension</span></span>](./Get-AzureVMPuppetExtension.md)

[<span data-ttu-id="aec38-135">Satz-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="aec38-135">Set-AzureVMPuppetExtension</span></span>](./Set-AzureVMPuppetExtension.md)


