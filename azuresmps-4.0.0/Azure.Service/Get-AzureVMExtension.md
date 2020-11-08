---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7ED074F0-1E9E-40C2-A543-D19A49831DD3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f0b8ca9acfe5a62b002944bd44e11acfcd38ec1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006739"
---
# <span data-ttu-id="08fa3-101">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="08fa3-101">Get-AzureVMExtension</span></span>

## <span data-ttu-id="08fa3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="08fa3-103">Ruft Ressourcenerweiterungen ab, die auf virtuelle Computer angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="08fa3-103">Gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="08fa3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08fa3-104">SYNTAX</span></span>

### <span data-ttu-id="08fa3-105">ListByReferenceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="08fa3-105">ListByReferenceName (Default)</span></span>
```
Get-AzureVMExtension [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="08fa3-106">ListByExtensionName</span><span class="sxs-lookup"><span data-stu-id="08fa3-106">ListByExtensionName</span></span>
```
Get-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="08fa3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08fa3-107">DESCRIPTION</span></span>
<span data-ttu-id="08fa3-108">Das Cmdlet " **Get-AzureVMExtension** " ruft Ressourcenerweiterungen auf, die auf virtuelle Computer angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="08fa3-108">The **Get-AzureVMExtension** cmdlet gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="08fa3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08fa3-109">EXAMPLES</span></span>

### <span data-ttu-id="08fa3-110">Beispiel 1: Abrufen der auf einen virtuellen Computer angewendeten Ressourcenerweiterungen</span><span class="sxs-lookup"><span data-stu-id="08fa3-110">Example 1: Get the resource extensions applied to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName $SVC -Name $VM | Get-AzureVMExtension;
```

<span data-ttu-id="08fa3-111">Dieser Befehl ruft die auf den angegebenen virtuellen Computer angewendeten Ressourcenerweiterungen ab, wie Sie in der Variablen $VM gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="08fa3-111">This command gets the resource extensions applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="08fa3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="08fa3-112">PARAMETERS</span></span>

### <span data-ttu-id="08fa3-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="08fa3-113">-ExtensionName</span></span>
<span data-ttu-id="08fa3-114">Gibt den Namen der Erweiterung der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="08fa3-114">Specifies the virtual machine extension name.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08fa3-115">-Information</span><span class="sxs-lookup"><span data-stu-id="08fa3-115">-InformationAction</span></span>
<span data-ttu-id="08fa3-116">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="08fa3-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="08fa3-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="08fa3-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="08fa3-118">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="08fa3-118">Continue</span></span>
- <span data-ttu-id="08fa3-119">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="08fa3-119">Ignore</span></span>
- <span data-ttu-id="08fa3-120">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="08fa3-120">Inquire</span></span>
- <span data-ttu-id="08fa3-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="08fa3-121">SilentlyContinue</span></span>
- <span data-ttu-id="08fa3-122">Beenden</span><span class="sxs-lookup"><span data-stu-id="08fa3-122">Stop</span></span>
- <span data-ttu-id="08fa3-123">Anhalten</span><span class="sxs-lookup"><span data-stu-id="08fa3-123">Suspend</span></span>

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

### <span data-ttu-id="08fa3-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="08fa3-124">-InformationVariable</span></span>
<span data-ttu-id="08fa3-125">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="08fa3-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="08fa3-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="08fa3-126">-Profile</span></span>
<span data-ttu-id="08fa3-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="08fa3-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="08fa3-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="08fa3-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="08fa3-129">-Publisher</span><span class="sxs-lookup"><span data-stu-id="08fa3-129">-Publisher</span></span>
<span data-ttu-id="08fa3-130">Gibt den Herausgeber der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="08fa3-130">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08fa3-131">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="08fa3-131">-ReferenceName</span></span>
<span data-ttu-id="08fa3-132">Gibt den Verweisnamen der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="08fa3-132">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByReferenceName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08fa3-133">-Version</span><span class="sxs-lookup"><span data-stu-id="08fa3-133">-Version</span></span>
<span data-ttu-id="08fa3-134">Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="08fa3-134">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08fa3-135">-VM</span><span class="sxs-lookup"><span data-stu-id="08fa3-135">-VM</span></span>
<span data-ttu-id="08fa3-136">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="08fa3-136">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="08fa3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08fa3-137">CommonParameters</span></span>
<span data-ttu-id="08fa3-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08fa3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08fa3-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08fa3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08fa3-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08fa3-140">INPUTS</span></span>

## <span data-ttu-id="08fa3-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08fa3-141">OUTPUTS</span></span>

## <span data-ttu-id="08fa3-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="08fa3-142">NOTES</span></span>

## <span data-ttu-id="08fa3-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08fa3-143">RELATED LINKS</span></span>

[<span data-ttu-id="08fa3-144">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="08fa3-144">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="08fa3-145">Satz-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="08fa3-145">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)


