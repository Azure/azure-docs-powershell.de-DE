---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A4E88106-1B47-4ACD-8F35-027D16EA7791
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b3422581fa884245807f258adcc31d52404c53
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006011"
---
# <span data-ttu-id="85696-101">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="85696-101">Set-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="85696-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85696-102">SYNOPSIS</span></span>

## <span data-ttu-id="85696-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="85696-103">SYNTAX</span></span>

```
Set-AzureNetworkInterfaceConfig [-Name] <String> [-SubnetName] <String> [[-StaticVNetIPAddress] <String>]
 [[-NetworkSecurityGroup] <String>] [[-IPForwarding] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="85696-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85696-104">DESCRIPTION</span></span>

## <span data-ttu-id="85696-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85696-105">EXAMPLES</span></span>

### <span data-ttu-id="85696-106">1:</span><span class="sxs-lookup"><span data-stu-id="85696-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="85696-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="85696-107">PARAMETERS</span></span>

### <span data-ttu-id="85696-108">-Information</span><span class="sxs-lookup"><span data-stu-id="85696-108">-InformationAction</span></span>
<span data-ttu-id="85696-109">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="85696-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="85696-110">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="85696-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="85696-111">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="85696-111">Continue</span></span>
- <span data-ttu-id="85696-112">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="85696-112">Ignore</span></span>
- <span data-ttu-id="85696-113">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="85696-113">Inquire</span></span>
- <span data-ttu-id="85696-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="85696-114">SilentlyContinue</span></span>
- <span data-ttu-id="85696-115">Beenden</span><span class="sxs-lookup"><span data-stu-id="85696-115">Stop</span></span>
- <span data-ttu-id="85696-116">Anhalten</span><span class="sxs-lookup"><span data-stu-id="85696-116">Suspend</span></span>

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

### <span data-ttu-id="85696-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="85696-117">-InformationVariable</span></span>
<span data-ttu-id="85696-118">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="85696-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="85696-119">-IPForwarding</span><span class="sxs-lookup"><span data-stu-id="85696-119">-IPForwarding</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85696-120">-Name</span><span class="sxs-lookup"><span data-stu-id="85696-120">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85696-121">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="85696-121">-NetworkSecurityGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85696-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="85696-122">-Profile</span></span>
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

### <span data-ttu-id="85696-123">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="85696-123">-StaticVNetIPAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85696-124">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="85696-124">-SubnetName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85696-125">-VM</span><span class="sxs-lookup"><span data-stu-id="85696-125">-VM</span></span>
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

### <span data-ttu-id="85696-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85696-126">CommonParameters</span></span>
<span data-ttu-id="85696-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85696-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85696-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85696-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85696-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85696-129">INPUTS</span></span>

## <span data-ttu-id="85696-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85696-130">OUTPUTS</span></span>

## <span data-ttu-id="85696-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="85696-131">NOTES</span></span>

## <span data-ttu-id="85696-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85696-132">RELATED LINKS</span></span>

[<span data-ttu-id="85696-133">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="85696-133">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="85696-134">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="85696-134">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="85696-135">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="85696-135">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)


