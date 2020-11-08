---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A513B7CA-182E-46A2-8181-020C5DFC7DE9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 316e7c182025171d2f1ba66ead1a0c0f5de120b1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005710"
---
# <span data-ttu-id="bc6c9-101">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bc6c9-101">Remove-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="bc6c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bc6c9-102">SYNOPSIS</span></span>
<span data-ttu-id="bc6c9-103">Entfernt die Azure Diagnostics-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="bc6c9-103">Removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="bc6c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc6c9-104">SYNTAX</span></span>

```
Remove-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bc6c9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc6c9-105">DESCRIPTION</span></span>
<span data-ttu-id="bc6c9-106">Das Cmdlet **Remove-AzureVMDiagnosticsExtension** entfernt eine Microsoft Azure Diagnostics-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="bc6c9-106">The **Remove-AzureVMDiagnosticsExtension** cmdlet removes a Microsoft Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="bc6c9-107">Sie müssen die Ausgabe dieses Cmdlets an das Cmdlet **Update-AzureVM** übergeben.</span><span class="sxs-lookup"><span data-stu-id="bc6c9-107">You must pass the output of this cmdlet to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="bc6c9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc6c9-108">EXAMPLES</span></span>

### <span data-ttu-id="bc6c9-109">Beispiel 1: Entfernen der Azure Diagnostics-Erweiterung von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="bc6c9-109">Example 1: Remove the Azure Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDiagnosticsExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="bc6c9-110">Mit diesem Befehl wird die Azure Diagnostics-Erweiterung von einem virtuellen Computer entfernt.</span><span class="sxs-lookup"><span data-stu-id="bc6c9-110">This command removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="bc6c9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc6c9-111">PARAMETERS</span></span>

### <span data-ttu-id="bc6c9-112">-Information</span><span class="sxs-lookup"><span data-stu-id="bc6c9-112">-InformationAction</span></span>
<span data-ttu-id="bc6c9-113">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="bc6c9-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bc6c9-114">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bc6c9-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bc6c9-115">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="bc6c9-115">Continue</span></span>
- <span data-ttu-id="bc6c9-116">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="bc6c9-116">Ignore</span></span>
- <span data-ttu-id="bc6c9-117">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="bc6c9-117">Inquire</span></span>
- <span data-ttu-id="bc6c9-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bc6c9-118">SilentlyContinue</span></span>
- <span data-ttu-id="bc6c9-119">Beenden</span><span class="sxs-lookup"><span data-stu-id="bc6c9-119">Stop</span></span>
- <span data-ttu-id="bc6c9-120">Anhalten</span><span class="sxs-lookup"><span data-stu-id="bc6c9-120">Suspend</span></span>

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

### <span data-ttu-id="bc6c9-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bc6c9-121">-InformationVariable</span></span>
<span data-ttu-id="bc6c9-122">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="bc6c9-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bc6c9-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="bc6c9-123">-Profile</span></span>
<span data-ttu-id="bc6c9-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="bc6c9-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bc6c9-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="bc6c9-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bc6c9-126">-VM</span><span class="sxs-lookup"><span data-stu-id="bc6c9-126">-VM</span></span>
<span data-ttu-id="bc6c9-127">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="bc6c9-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="bc6c9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc6c9-128">CommonParameters</span></span>
<span data-ttu-id="bc6c9-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc6c9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc6c9-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc6c9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc6c9-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bc6c9-131">INPUTS</span></span>

## <span data-ttu-id="bc6c9-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bc6c9-132">OUTPUTS</span></span>

## <span data-ttu-id="bc6c9-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="bc6c9-133">NOTES</span></span>

## <span data-ttu-id="bc6c9-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bc6c9-134">RELATED LINKS</span></span>

[<span data-ttu-id="bc6c9-135">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bc6c9-135">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="bc6c9-136">Satz-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bc6c9-136">Set-AzureVMDiagnosticsExtension</span></span>](./Set-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="bc6c9-137">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="bc6c9-137">Update-AzureVM</span></span>](./Update-AzureVM.md)


