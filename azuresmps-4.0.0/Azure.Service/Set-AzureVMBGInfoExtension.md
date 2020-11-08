---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 377716B6-8B8C-4CAE-A8FA-835DA24F04C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9610c6b8abaf4d59d6a363253d0b90a0dfcecad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006249"
---
# <span data-ttu-id="9493e-101">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="9493e-101">Set-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="9493e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9493e-102">SYNOPSIS</span></span>
<span data-ttu-id="9493e-103">Legt die BGInfo-Erweiterung für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="9493e-103">Sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="9493e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9493e-104">SYNTAX</span></span>

### <span data-ttu-id="9493e-105">SetBGInfoExtension (Standard)</span><span class="sxs-lookup"><span data-stu-id="9493e-105">SetBGInfoExtension (Default)</span></span>
```
Set-AzureVMBGInfoExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="9493e-106">UninstallBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="9493e-106">UninstallBGInfoExtension</span></span>
```
Set-AzureVMBGInfoExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="9493e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9493e-107">DESCRIPTION</span></span>
<span data-ttu-id="9493e-108">Das Cmdlet " **Set-AzureVMBGInfoExtension** " legt die BGInfo-Erweiterung für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="9493e-108">The **Set-AzureVMBGInfoExtension** cmdlet sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="9493e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9493e-109">EXAMPLES</span></span>

### <span data-ttu-id="9493e-110">Beispiel 1: Einrichten der BGInfo-Erweiterung für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="9493e-110">Example 1: Set the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMBGInfoExtension -VM $VM
```

<span data-ttu-id="9493e-111">Mit diesem Befehl wird die BGInfo-Erweiterung für den angegebenen virtuellen Computer so festgelegt, wie er in der Variablen $VM gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="9493e-111">This command sets the BGInfo extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="9493e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9493e-112">PARAMETERS</span></span>

### <span data-ttu-id="9493e-113">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="9493e-113">-Disable</span></span>
<span data-ttu-id="9493e-114">Gibt an, dass dieses Cmdlet den Erweiterungszustand deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="9493e-114">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9493e-115">-Information</span><span class="sxs-lookup"><span data-stu-id="9493e-115">-InformationAction</span></span>
<span data-ttu-id="9493e-116">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="9493e-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9493e-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9493e-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9493e-118">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="9493e-118">Continue</span></span>
- <span data-ttu-id="9493e-119">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="9493e-119">Ignore</span></span>
- <span data-ttu-id="9493e-120">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="9493e-120">Inquire</span></span>
- <span data-ttu-id="9493e-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9493e-121">SilentlyContinue</span></span>
- <span data-ttu-id="9493e-122">Beenden</span><span class="sxs-lookup"><span data-stu-id="9493e-122">Stop</span></span>
- <span data-ttu-id="9493e-123">Anhalten</span><span class="sxs-lookup"><span data-stu-id="9493e-123">Suspend</span></span>

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

### <span data-ttu-id="9493e-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9493e-124">-InformationVariable</span></span>
<span data-ttu-id="9493e-125">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="9493e-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9493e-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="9493e-126">-Profile</span></span>
<span data-ttu-id="9493e-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="9493e-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9493e-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="9493e-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9493e-129">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="9493e-129">-ReferenceName</span></span>
<span data-ttu-id="9493e-130">Gibt den Verweisnamen der BGInfo-Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="9493e-130">Specifies the reference name of the BGInfo extension.</span></span>

<span data-ttu-id="9493e-131">Dieser Parameter ist eine benutzerdefinierte Zeichenfolge, die verwendet werden kann, um auf eine Erweiterung zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="9493e-131">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="9493e-132">Sie wird angegeben, wenn die Erweiterung zum ersten Mal dem virtuellen Computer hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="9493e-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="9493e-133">Sie können den zuvor verwendeten Verweisnamen beim Aktualisieren der Erweiterung angeben.</span><span class="sxs-lookup"><span data-stu-id="9493e-133">You can specify the previously used reference name while updating the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9493e-134">-Deinstallieren</span><span class="sxs-lookup"><span data-stu-id="9493e-134">-Uninstall</span></span>
<span data-ttu-id="9493e-135">Gibt an, dass dieses Cmdlet die BGInfo-Erweiterung deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="9493e-135">Indicates that this cmdlet uninstalls the BGInfo extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9493e-136">-Version</span><span class="sxs-lookup"><span data-stu-id="9493e-136">-Version</span></span>
<span data-ttu-id="9493e-137">Gibt die Version der BGInfo-Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="9493e-137">Specifies the version of the BGInfo extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9493e-138">-VM</span><span class="sxs-lookup"><span data-stu-id="9493e-138">-VM</span></span>
<span data-ttu-id="9493e-139">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="9493e-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="9493e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9493e-140">CommonParameters</span></span>
<span data-ttu-id="9493e-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9493e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9493e-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9493e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9493e-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9493e-143">INPUTS</span></span>

## <span data-ttu-id="9493e-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9493e-144">OUTPUTS</span></span>

## <span data-ttu-id="9493e-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="9493e-145">NOTES</span></span>

## <span data-ttu-id="9493e-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9493e-146">RELATED LINKS</span></span>

[<span data-ttu-id="9493e-147">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="9493e-147">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="9493e-148">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="9493e-148">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)


