---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3DCA1502-9528-458D-A9EA-762A4BD2726B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284fcf4bd31eeb9437b8cc7669fff0824155180f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006654"
---
# <span data-ttu-id="72e6b-101">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="72e6b-101">Remove-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="72e6b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="72e6b-103">Entfernt die benutzerdefinierte Skripterweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="72e6b-103">Removes the custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="72e6b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72e6b-104">SYNTAX</span></span>

```
Remove-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="72e6b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72e6b-105">DESCRIPTION</span></span>
<span data-ttu-id="72e6b-106">Das Cmdlet **Remove-AzureVMCustomScriptExtension** entfernt die benutzerdefinierte Skripterweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="72e6b-106">The **Remove-AzureVMCustomScriptExtension** cmdlet removes the custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="72e6b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72e6b-107">EXAMPLES</span></span>

### <span data-ttu-id="72e6b-108">Beispiel 1: Entfernen einer benutzerdefinierten Skripterweiterung eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="72e6b-108">Example 1: Remove a virtual machine custom script extension</span></span>
```
PS C:\> Remove-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="72e6b-109">Mit diesem Befehl wird die benutzerdefinierte Skripterweiterung Azure Virtual Machine vom angegebenen virtuellen Computer entfernt, wie Sie in der Variablen $VM gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="72e6b-109">This command removes the Azure virtual machine custom script extension from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="72e6b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="72e6b-110">PARAMETERS</span></span>

### <span data-ttu-id="72e6b-111">-Information</span><span class="sxs-lookup"><span data-stu-id="72e6b-111">-InformationAction</span></span>
<span data-ttu-id="72e6b-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="72e6b-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="72e6b-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="72e6b-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="72e6b-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="72e6b-114">Continue</span></span>
- <span data-ttu-id="72e6b-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="72e6b-115">Ignore</span></span>
- <span data-ttu-id="72e6b-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="72e6b-116">Inquire</span></span>
- <span data-ttu-id="72e6b-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="72e6b-117">SilentlyContinue</span></span>
- <span data-ttu-id="72e6b-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="72e6b-118">Stop</span></span>
- <span data-ttu-id="72e6b-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="72e6b-119">Suspend</span></span>

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

### <span data-ttu-id="72e6b-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="72e6b-120">-InformationVariable</span></span>
<span data-ttu-id="72e6b-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="72e6b-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="72e6b-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="72e6b-122">-Profile</span></span>
<span data-ttu-id="72e6b-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="72e6b-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="72e6b-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="72e6b-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="72e6b-125">-VM</span><span class="sxs-lookup"><span data-stu-id="72e6b-125">-VM</span></span>
<span data-ttu-id="72e6b-126">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="72e6b-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="72e6b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e6b-127">CommonParameters</span></span>
<span data-ttu-id="72e6b-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72e6b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e6b-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72e6b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e6b-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72e6b-130">INPUTS</span></span>

## <span data-ttu-id="72e6b-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72e6b-131">OUTPUTS</span></span>

## <span data-ttu-id="72e6b-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="72e6b-132">NOTES</span></span>

## <span data-ttu-id="72e6b-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72e6b-133">RELATED LINKS</span></span>

[<span data-ttu-id="72e6b-134">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="72e6b-134">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="72e6b-135">Satz-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="72e6b-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


