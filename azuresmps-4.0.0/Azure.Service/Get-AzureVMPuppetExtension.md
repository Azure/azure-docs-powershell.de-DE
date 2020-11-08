---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9AC28E79-0E3F-4AED-8BFE-8D1C4DCB7715
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd7ece4f8f414df7be6e2d38920f516119f4b82a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006732"
---
# <span data-ttu-id="1c41a-101">Get-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="1c41a-101">Get-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="1c41a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c41a-102">SYNOPSIS</span></span>
<span data-ttu-id="1c41a-103">Ruft die auf einem virtuellen Computer angewendete Marionetten Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="1c41a-103">Gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="1c41a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c41a-104">SYNTAX</span></span>

```
Get-AzureVMPuppetExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1c41a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c41a-105">DESCRIPTION</span></span>
<span data-ttu-id="1c41a-106">Das Cmdlet " **Get-AzureVMPuppetExtension** " Ruft die auf einem virtuellen Computer angewendete Marionetten Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="1c41a-106">The **Get-AzureVMPuppetExtension** cmdlet gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="1c41a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c41a-107">EXAMPLES</span></span>

### <span data-ttu-id="1c41a-108">Beispiel 1: Abrufen der auf einem virtuellen Computer angewendeten Marionetten Erweiterung</span><span class="sxs-lookup"><span data-stu-id="1c41a-108">Example 1: Get the Puppet extension applied on a virtual machine</span></span>
```
PS C:\> Get-AzureVMPuppetExtension -VM $VM
```

<span data-ttu-id="1c41a-109">Mit diesem Befehl wird die auf einem virtuellen Computer angewendete Marionetten Erweiterung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1c41a-109">This command gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="1c41a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c41a-110">PARAMETERS</span></span>

### <span data-ttu-id="1c41a-111">-Information</span><span class="sxs-lookup"><span data-stu-id="1c41a-111">-InformationAction</span></span>
<span data-ttu-id="1c41a-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="1c41a-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1c41a-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1c41a-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1c41a-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="1c41a-114">Continue</span></span>
- <span data-ttu-id="1c41a-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="1c41a-115">Ignore</span></span>
- <span data-ttu-id="1c41a-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="1c41a-116">Inquire</span></span>
- <span data-ttu-id="1c41a-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1c41a-117">SilentlyContinue</span></span>
- <span data-ttu-id="1c41a-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="1c41a-118">Stop</span></span>
- <span data-ttu-id="1c41a-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="1c41a-119">Suspend</span></span>

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

### <span data-ttu-id="1c41a-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1c41a-120">-InformationVariable</span></span>
<span data-ttu-id="1c41a-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="1c41a-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1c41a-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="1c41a-122">-Profile</span></span>
<span data-ttu-id="1c41a-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="1c41a-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1c41a-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="1c41a-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1c41a-125">-VM</span><span class="sxs-lookup"><span data-stu-id="1c41a-125">-VM</span></span>
<span data-ttu-id="1c41a-126">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="1c41a-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="1c41a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c41a-127">CommonParameters</span></span>
<span data-ttu-id="1c41a-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c41a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c41a-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c41a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c41a-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c41a-130">INPUTS</span></span>

## <span data-ttu-id="1c41a-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c41a-131">OUTPUTS</span></span>

## <span data-ttu-id="1c41a-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c41a-132">NOTES</span></span>

## <span data-ttu-id="1c41a-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c41a-133">RELATED LINKS</span></span>

[<span data-ttu-id="1c41a-134">Remove-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="1c41a-134">Remove-AzureVMPuppetExtension</span></span>](./Remove-AzureVMPuppetExtension.md)

[<span data-ttu-id="1c41a-135">Satz-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="1c41a-135">Set-AzureVMPuppetExtension</span></span>](./Set-AzureVMPuppetExtension.md)


