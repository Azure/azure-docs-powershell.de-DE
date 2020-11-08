---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 40AE50AA-6807-4481-8B77-A038914D462E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a4c6997a7ae70a72a21800cce1d4f5f32475a85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006653"
---
# <span data-ttu-id="91fcd-101">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="91fcd-101">Remove-AzureVMDscExtension</span></span>

## <span data-ttu-id="91fcd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91fcd-102">SYNOPSIS</span></span>
<span data-ttu-id="91fcd-103">Entfernt eine Azure DSC-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="91fcd-103">Removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="91fcd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91fcd-104">SYNTAX</span></span>

```
Remove-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91fcd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91fcd-105">DESCRIPTION</span></span>
<span data-ttu-id="91fcd-106">Das Cmdlet **Remove-AzureVMDscExtension** entfernt eine Azure DSC-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="91fcd-106">The **Remove-AzureVMDscExtension** cmdlet removes an Azure DSC extension from a virtual machine.</span></span>
<span data-ttu-id="91fcd-107">Die Ausgabe dieses Cmdlets muss an das Cmdlet **Update-AzureVM** umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="91fcd-107">The output of this cmdlet needs to be piped to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="91fcd-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91fcd-108">EXAMPLES</span></span>

### <span data-ttu-id="91fcd-109">Beispiel 1: Entfernen einer DSC-Erweiterung von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="91fcd-109">Example 1: Remove a DSC extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDscExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="91fcd-110">Mit diesem Befehl wird eine Azure DSC-Erweiterung von einem virtuellen Computer entfernt.</span><span class="sxs-lookup"><span data-stu-id="91fcd-110">This command removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="91fcd-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="91fcd-111">PARAMETERS</span></span>

### <span data-ttu-id="91fcd-112">-Information</span><span class="sxs-lookup"><span data-stu-id="91fcd-112">-InformationAction</span></span>
<span data-ttu-id="91fcd-113">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="91fcd-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="91fcd-114">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="91fcd-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91fcd-115">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="91fcd-115">Continue</span></span>
- <span data-ttu-id="91fcd-116">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="91fcd-116">Ignore</span></span>
- <span data-ttu-id="91fcd-117">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="91fcd-117">Inquire</span></span>
- <span data-ttu-id="91fcd-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="91fcd-118">SilentlyContinue</span></span>
- <span data-ttu-id="91fcd-119">Beenden</span><span class="sxs-lookup"><span data-stu-id="91fcd-119">Stop</span></span>
- <span data-ttu-id="91fcd-120">Anhalten</span><span class="sxs-lookup"><span data-stu-id="91fcd-120">Suspend</span></span>

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

### <span data-ttu-id="91fcd-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="91fcd-121">-InformationVariable</span></span>
<span data-ttu-id="91fcd-122">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="91fcd-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="91fcd-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="91fcd-123">-Profile</span></span>
<span data-ttu-id="91fcd-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="91fcd-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="91fcd-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="91fcd-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="91fcd-126">-VM</span><span class="sxs-lookup"><span data-stu-id="91fcd-126">-VM</span></span>
<span data-ttu-id="91fcd-127">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="91fcd-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="91fcd-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="91fcd-128">-Confirm</span></span>
<span data-ttu-id="91fcd-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91fcd-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91fcd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91fcd-130">-WhatIf</span></span>
<span data-ttu-id="91fcd-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91fcd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91fcd-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91fcd-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91fcd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91fcd-133">CommonParameters</span></span>
<span data-ttu-id="91fcd-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91fcd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91fcd-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91fcd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91fcd-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91fcd-136">INPUTS</span></span>

## <span data-ttu-id="91fcd-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91fcd-137">OUTPUTS</span></span>

## <span data-ttu-id="91fcd-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="91fcd-138">NOTES</span></span>

## <span data-ttu-id="91fcd-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91fcd-139">RELATED LINKS</span></span>

[<span data-ttu-id="91fcd-140">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="91fcd-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="91fcd-141">Satz-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="91fcd-141">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="91fcd-142">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="91fcd-142">Update-AzureVM</span></span>](./Update-AzureVM.md)


