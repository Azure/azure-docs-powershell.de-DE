---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B98FCF46-A5D6-4CC9-B82A-60B429A21A8B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8079844a931debee5b9338e98d405697cc4336f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005707"
---
# <span data-ttu-id="8ad9c-101">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="8ad9c-101">Remove-AzureVMExtension</span></span>

## <span data-ttu-id="8ad9c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ad9c-102">SYNOPSIS</span></span>
<span data-ttu-id="8ad9c-103">Entfernt Ressourcenerweiterungen von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-103">Removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="8ad9c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ad9c-104">SYNTAX</span></span>

### <span data-ttu-id="8ad9c-105">RemoveByExtensionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8ad9c-105">RemoveByExtensionName (Default)</span></span>
```
Remove-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ad9c-106">RemoveByReferenceName</span><span class="sxs-lookup"><span data-stu-id="8ad9c-106">RemoveByReferenceName</span></span>
```
Remove-AzureVMExtension [-ReferenceName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8ad9c-107">Entfernenalles</span><span class="sxs-lookup"><span data-stu-id="8ad9c-107">RemoveAll</span></span>
```
Remove-AzureVMExtension [-RemoveAll] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8ad9c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ad9c-108">DESCRIPTION</span></span>
<span data-ttu-id="8ad9c-109">Das Cmdlet **Remove-AzureVMExtension** entfernt Ressourcenerweiterungen von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-109">The **Remove-AzureVMExtension** cmdlet removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="8ad9c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ad9c-110">EXAMPLES</span></span>

### <span data-ttu-id="8ad9c-111">Beispiel 1: Entfernen einer Erweiterung mit einem bestimmten Namen und Publisher</span><span class="sxs-lookup"><span data-stu-id="8ad9c-111">Example 1: Remove an extension using a specific name and publisher</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -ExtensionName $EXT -Publisher $PUB;
```

<span data-ttu-id="8ad9c-112">Mit diesem Befehl wird eine Erweiterung mit dem angegebenen Namen und Publisher entfernt.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-112">This command removes an extension with the specified name and publisher.</span></span>

### <span data-ttu-id="8ad9c-113">Beispiel 2: Entfernen aller Erweiterungen von einem bestimmten virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="8ad9c-113">Example 2: Remove all extensions from a specific virtual machine</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -RemoveAll;
```

<span data-ttu-id="8ad9c-114">Mit diesem Befehl werden alle Erweiterungen vom angegebenen virtuellen Computer entfernt, wie Sie in der Variablen $VM gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-114">This command removes all extensions from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="8ad9c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ad9c-115">PARAMETERS</span></span>

### <span data-ttu-id="8ad9c-116">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="8ad9c-116">-ExtensionName</span></span>
<span data-ttu-id="8ad9c-117">Gibt den Namen der Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-117">Specifies the extension name that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ad9c-118">-Information</span><span class="sxs-lookup"><span data-stu-id="8ad9c-118">-InformationAction</span></span>
<span data-ttu-id="8ad9c-119">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8ad9c-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8ad9c-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8ad9c-121">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="8ad9c-121">Continue</span></span>
- <span data-ttu-id="8ad9c-122">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="8ad9c-122">Ignore</span></span>
- <span data-ttu-id="8ad9c-123">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="8ad9c-123">Inquire</span></span>
- <span data-ttu-id="8ad9c-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8ad9c-124">SilentlyContinue</span></span>
- <span data-ttu-id="8ad9c-125">Beenden</span><span class="sxs-lookup"><span data-stu-id="8ad9c-125">Stop</span></span>
- <span data-ttu-id="8ad9c-126">Anhalten</span><span class="sxs-lookup"><span data-stu-id="8ad9c-126">Suspend</span></span>

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

### <span data-ttu-id="8ad9c-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8ad9c-127">-InformationVariable</span></span>
<span data-ttu-id="8ad9c-128">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8ad9c-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="8ad9c-129">-Profile</span></span>
<span data-ttu-id="8ad9c-130">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8ad9c-131">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8ad9c-132">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8ad9c-132">-Publisher</span></span>
<span data-ttu-id="8ad9c-133">Gibt den Erweiterungs Herausgeber an.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-133">Specifies the extension publisher.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ad9c-134">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="8ad9c-134">-ReferenceName</span></span>
<span data-ttu-id="8ad9c-135">Gibt den Verweisnamen der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-135">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByReferenceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ad9c-136">-Entfernenalles</span><span class="sxs-lookup"><span data-stu-id="8ad9c-136">-RemoveAll</span></span>
<span data-ttu-id="8ad9c-137">Gibt an, dass mit diesem Cmdlet alle Ressourcenerweiterungen vom virtuellen Computer entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-137">Indicates that this cmdlet removes all resource extensions from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAll
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ad9c-138">-VM</span><span class="sxs-lookup"><span data-stu-id="8ad9c-138">-VM</span></span>
<span data-ttu-id="8ad9c-139">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="8ad9c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ad9c-140">CommonParameters</span></span>
<span data-ttu-id="8ad9c-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ad9c-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ad9c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ad9c-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ad9c-143">INPUTS</span></span>

## <span data-ttu-id="8ad9c-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ad9c-144">OUTPUTS</span></span>

## <span data-ttu-id="8ad9c-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ad9c-145">NOTES</span></span>

## <span data-ttu-id="8ad9c-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ad9c-146">RELATED LINKS</span></span>

[<span data-ttu-id="8ad9c-147">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="8ad9c-147">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="8ad9c-148">Satz-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="8ad9c-148">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)


