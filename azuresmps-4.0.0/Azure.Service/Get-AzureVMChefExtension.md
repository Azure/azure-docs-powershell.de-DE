---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1721107D-22FF-4A42-93C6-FD812DF81C33
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac1bb63645b8db9e6a66971ad4ecd3b545a39100
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006751"
---
# <span data-ttu-id="2e017-101">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2e017-101">Get-AzureVMChefExtension</span></span>

## <span data-ttu-id="2e017-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2e017-102">SYNOPSIS</span></span>
<span data-ttu-id="2e017-103">Ruft die auf einem virtuellen Computer angewendete Chefkoch-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="2e017-103">Gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="2e017-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e017-104">SYNTAX</span></span>

```
Get-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2e017-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e017-105">DESCRIPTION</span></span>
<span data-ttu-id="2e017-106">Das Cmdlet " **Get-AzureVMChefExtension** " Ruft die auf einem virtuellen Computer angewendete Chefkoch-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="2e017-106">The **Get-AzureVMChefExtension** cmdlet gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="2e017-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e017-107">EXAMPLES</span></span>

### <span data-ttu-id="2e017-108">Beispiel 1: Abrufen der auf dem angegebenen virtuellen Computer angewendeten Chef Erweiterung</span><span class="sxs-lookup"><span data-stu-id="2e017-108">Example 1: Get the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Get-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="2e017-109">Mit diesem Befehl wird die auf dem angegebenen virtuellen Computer angewendete Chefkoch-Erweiterung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2e017-109">This command gets the Chef extension applied on the specified virtual machine.</span></span>

## <span data-ttu-id="2e017-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e017-110">PARAMETERS</span></span>

### <span data-ttu-id="2e017-111">-Information</span><span class="sxs-lookup"><span data-stu-id="2e017-111">-InformationAction</span></span>
<span data-ttu-id="2e017-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="2e017-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2e017-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2e017-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2e017-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="2e017-114">Continue</span></span>
- <span data-ttu-id="2e017-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="2e017-115">Ignore</span></span>
- <span data-ttu-id="2e017-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="2e017-116">Inquire</span></span>
- <span data-ttu-id="2e017-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2e017-117">SilentlyContinue</span></span>
- <span data-ttu-id="2e017-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="2e017-118">Stop</span></span>
- <span data-ttu-id="2e017-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="2e017-119">Suspend</span></span>

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

### <span data-ttu-id="2e017-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2e017-120">-InformationVariable</span></span>
<span data-ttu-id="2e017-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="2e017-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2e017-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="2e017-122">-Profile</span></span>
<span data-ttu-id="2e017-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="2e017-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2e017-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="2e017-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2e017-125">-VM</span><span class="sxs-lookup"><span data-stu-id="2e017-125">-VM</span></span>
<span data-ttu-id="2e017-126">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="2e017-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="2e017-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e017-127">CommonParameters</span></span>
<span data-ttu-id="2e017-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e017-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e017-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e017-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e017-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e017-130">INPUTS</span></span>

## <span data-ttu-id="2e017-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2e017-131">OUTPUTS</span></span>

## <span data-ttu-id="2e017-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="2e017-132">NOTES</span></span>

## <span data-ttu-id="2e017-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2e017-133">RELATED LINKS</span></span>

[<span data-ttu-id="2e017-134">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2e017-134">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)

[<span data-ttu-id="2e017-135">Satz-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2e017-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


