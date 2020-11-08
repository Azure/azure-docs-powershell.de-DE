---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DBB8EC31-877C-4DB1-8197-CA7A4148AE06
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f8767c9477db41251eb4732a2eb96d8dd782c20
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005737"
---
# <span data-ttu-id="20a37-101">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="20a37-101">Get-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="20a37-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20a37-102">SYNOPSIS</span></span>
<span data-ttu-id="20a37-103">Ruft Informationen aus der benutzerdefinierten Skripterweiterung Azure Virtual Machine ab.</span><span class="sxs-lookup"><span data-stu-id="20a37-103">Gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="20a37-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20a37-104">SYNTAX</span></span>

```
Get-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="20a37-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20a37-105">DESCRIPTION</span></span>
<span data-ttu-id="20a37-106">Das Cmdlet " **Get-AzureVMCustomScriptExtension** " Ruft Informationen aus einer benutzerdefinierten Azure-Skripterweiterung für virtuelle Maschinen ab.</span><span class="sxs-lookup"><span data-stu-id="20a37-106">The **Get-AzureVMCustomScriptExtension** cmdlet gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="20a37-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20a37-107">EXAMPLES</span></span>

### <span data-ttu-id="20a37-108">Beispiel 1: Abrufen einer Azure Virtual Machine-Skripterweiterung</span><span class="sxs-lookup"><span data-stu-id="20a37-108">Example 1: Get an Azure virtual machine script extension</span></span>
```
PS C:\> Get-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="20a37-109">Dieser Befehl ruft eine Azure Virtual Machine-Skripterweiterung ab, die in der Variablen $VM gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="20a37-109">This command gets an Azure virtual machine script extension stored in the variable $VM.</span></span>

## <span data-ttu-id="20a37-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="20a37-110">PARAMETERS</span></span>

### <span data-ttu-id="20a37-111">-Information</span><span class="sxs-lookup"><span data-stu-id="20a37-111">-InformationAction</span></span>
<span data-ttu-id="20a37-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="20a37-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="20a37-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="20a37-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="20a37-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="20a37-114">Continue</span></span>
- <span data-ttu-id="20a37-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="20a37-115">Ignore</span></span>
- <span data-ttu-id="20a37-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="20a37-116">Inquire</span></span>
- <span data-ttu-id="20a37-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="20a37-117">SilentlyContinue</span></span>
- <span data-ttu-id="20a37-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="20a37-118">Stop</span></span>
- <span data-ttu-id="20a37-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="20a37-119">Suspend</span></span>

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

### <span data-ttu-id="20a37-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="20a37-120">-InformationVariable</span></span>
<span data-ttu-id="20a37-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="20a37-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="20a37-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="20a37-122">-Profile</span></span>
<span data-ttu-id="20a37-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="20a37-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="20a37-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="20a37-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="20a37-125">-VM</span><span class="sxs-lookup"><span data-stu-id="20a37-125">-VM</span></span>
<span data-ttu-id="20a37-126">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="20a37-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="20a37-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a37-127">CommonParameters</span></span>
<span data-ttu-id="20a37-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20a37-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a37-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20a37-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a37-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20a37-130">INPUTS</span></span>

## <span data-ttu-id="20a37-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20a37-131">OUTPUTS</span></span>

## <span data-ttu-id="20a37-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="20a37-132">NOTES</span></span>

## <span data-ttu-id="20a37-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20a37-133">RELATED LINKS</span></span>

[<span data-ttu-id="20a37-134">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="20a37-134">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="20a37-135">Satz-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="20a37-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


