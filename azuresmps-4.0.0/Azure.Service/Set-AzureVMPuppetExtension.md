---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 268D3E91-AB0F-451F-93B2-9226985910B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41648470b76d889c1ee9d47e4200f843e9f11522
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006055"
---
# <span data-ttu-id="fe9d4-101">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="fe9d4-101">Set-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="fe9d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fe9d4-102">SYNOPSIS</span></span>
<span data-ttu-id="fe9d4-103">Legt die Marionetten Erweiterung für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="fe9d4-103">Sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="fe9d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe9d4-104">SYNTAX</span></span>

```
Set-AzureVMPuppetExtension [-PuppetMasterServer] <String> [[-Version] <String>] [-Disable]
 [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fe9d4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe9d4-105">DESCRIPTION</span></span>
<span data-ttu-id="fe9d4-106">Das Cmdlet " **Set-AzureVMPuppetExtension** " legt die Marionetten Erweiterung für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="fe9d4-106">The **Set-AzureVMPuppetExtension** cmdlet sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="fe9d4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe9d4-107">EXAMPLES</span></span>

### <span data-ttu-id="fe9d4-108">Beispiel 1: Einrichten der Marionetten Erweiterung für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="fe9d4-108">Example 1: Set the Puppet extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMPuppetExtension -VM $VM
```

<span data-ttu-id="fe9d4-109">In diesem Beispiel wird die Marionetten Erweiterung für den angegebenen virtuellen Computer so festgelegt, wie er in der Variablen $VM gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="fe9d4-109">This example sets the Puppet extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="fe9d4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe9d4-110">PARAMETERS</span></span>

### <span data-ttu-id="fe9d4-111">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="fe9d4-111">-Disable</span></span>
<span data-ttu-id="fe9d4-112">Gibt an, dass dieses Cmdlet den Erweiterungszustand deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fe9d4-112">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9d4-113">-Information</span><span class="sxs-lookup"><span data-stu-id="fe9d4-113">-InformationAction</span></span>
<span data-ttu-id="fe9d4-114">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="fe9d4-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fe9d4-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fe9d4-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fe9d4-116">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="fe9d4-116">Continue</span></span>
- <span data-ttu-id="fe9d4-117">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="fe9d4-117">Ignore</span></span>
- <span data-ttu-id="fe9d4-118">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="fe9d4-118">Inquire</span></span>
- <span data-ttu-id="fe9d4-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fe9d4-119">SilentlyContinue</span></span>
- <span data-ttu-id="fe9d4-120">Beenden</span><span class="sxs-lookup"><span data-stu-id="fe9d4-120">Stop</span></span>
- <span data-ttu-id="fe9d4-121">Anhalten</span><span class="sxs-lookup"><span data-stu-id="fe9d4-121">Suspend</span></span>

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

### <span data-ttu-id="fe9d4-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fe9d4-122">-InformationVariable</span></span>
<span data-ttu-id="fe9d4-123">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="fe9d4-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fe9d4-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="fe9d4-124">-Profile</span></span>
<span data-ttu-id="fe9d4-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="fe9d4-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fe9d4-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="fe9d4-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fe9d4-127">-PuppetMasterServer</span><span class="sxs-lookup"><span data-stu-id="fe9d4-127">-PuppetMasterServer</span></span>
<span data-ttu-id="fe9d4-128">Gibt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Marionetten Masterservers an.</span><span class="sxs-lookup"><span data-stu-id="fe9d4-128">Specifies the fully qualified domain name (FQDN) of puppet master server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9d4-129">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="fe9d4-129">-ReferenceName</span></span>
<span data-ttu-id="fe9d4-130">Gibt den Verweisnamen der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="fe9d4-130">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="fe9d4-131">Hierbei handelt es sich um eine benutzerdefinierte Zeichenfolge, die verwendet wird, um auf eine Erweiterung zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="fe9d4-131">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="fe9d4-132">Sie wird angegeben, wenn die Erweiterung zum ersten Mal dem virtuellen Computer hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="fe9d4-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="fe9d4-133">Für nachfolgende Updates müssen Sie den zuvor verwendeten Verweisnamen angeben, wenn Sie die Erweiterung aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="fe9d4-133">For subsequent updates, you need to specify the previously used reference name when you update the extension.</span></span>
<span data-ttu-id="fe9d4-134">Der Verweisname, der einer Erweiterung zugewiesen ist, wird mit dem Cmdlet **Get-AzureVM** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fe9d4-134">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9d4-135">-Version</span><span class="sxs-lookup"><span data-stu-id="fe9d4-135">-Version</span></span>
<span data-ttu-id="fe9d4-136">Gibt die Erweiterungsversion an.</span><span class="sxs-lookup"><span data-stu-id="fe9d4-136">Specifies the extension version.</span></span>

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

### <span data-ttu-id="fe9d4-137">-VM</span><span class="sxs-lookup"><span data-stu-id="fe9d4-137">-VM</span></span>
<span data-ttu-id="fe9d4-138">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="fe9d4-138">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="fe9d4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe9d4-139">CommonParameters</span></span>
<span data-ttu-id="fe9d4-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe9d4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe9d4-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe9d4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe9d4-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fe9d4-142">INPUTS</span></span>

## <span data-ttu-id="fe9d4-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fe9d4-143">OUTPUTS</span></span>

## <span data-ttu-id="fe9d4-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="fe9d4-144">NOTES</span></span>

## <span data-ttu-id="fe9d4-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fe9d4-145">RELATED LINKS</span></span>

[<span data-ttu-id="fe9d4-146">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fe9d4-146">Get-AzureVM</span></span>](./Get-AzureVM.md)


