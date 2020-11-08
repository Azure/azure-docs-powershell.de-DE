---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FE31EE5C-830F-4B5E-82DB-C881032EF05C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c1160478da2c84f2d792ab570b05d544f4537bc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006600"
---
# <span data-ttu-id="c7e8e-101">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="c7e8e-101">Add-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="c7e8e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7e8e-102">SYNOPSIS</span></span>

## <span data-ttu-id="c7e8e-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7e8e-103">SYNTAX</span></span>

```
Add-AzureNetworkInterfaceConfig [-Name] <String> [-SubnetName] <String> [[-StaticVNetIPAddress] <String>]
 [[-NetworkSecurityGroup] <String>] [[-IPForwarding] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c7e8e-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7e8e-104">DESCRIPTION</span></span>

## <span data-ttu-id="c7e8e-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7e8e-105">EXAMPLES</span></span>

### <span data-ttu-id="c7e8e-106">1:</span><span class="sxs-lookup"><span data-stu-id="c7e8e-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="c7e8e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7e8e-107">PARAMETERS</span></span>

### <span data-ttu-id="c7e8e-108">-Information</span><span class="sxs-lookup"><span data-stu-id="c7e8e-108">-InformationAction</span></span>
<span data-ttu-id="c7e8e-109">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="c7e8e-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c7e8e-110">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c7e8e-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7e8e-111">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="c7e8e-111">Continue</span></span>
- <span data-ttu-id="c7e8e-112">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="c7e8e-112">Ignore</span></span>
- <span data-ttu-id="c7e8e-113">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="c7e8e-113">Inquire</span></span>
- <span data-ttu-id="c7e8e-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c7e8e-114">SilentlyContinue</span></span>
- <span data-ttu-id="c7e8e-115">Beenden</span><span class="sxs-lookup"><span data-stu-id="c7e8e-115">Stop</span></span>
- <span data-ttu-id="c7e8e-116">Anhalten</span><span class="sxs-lookup"><span data-stu-id="c7e8e-116">Suspend</span></span>

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

### <span data-ttu-id="c7e8e-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c7e8e-117">-InformationVariable</span></span>
<span data-ttu-id="c7e8e-118">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="c7e8e-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c7e8e-119">-IPForwarding</span><span class="sxs-lookup"><span data-stu-id="c7e8e-119">-IPForwarding</span></span>
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

### <span data-ttu-id="c7e8e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c7e8e-120">-Name</span></span>
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

### <span data-ttu-id="c7e8e-121">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c7e8e-121">-NetworkSecurityGroup</span></span>
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

### <span data-ttu-id="c7e8e-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="c7e8e-122">-Profile</span></span>
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

### <span data-ttu-id="c7e8e-123">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="c7e8e-123">-StaticVNetIPAddress</span></span>
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

### <span data-ttu-id="c7e8e-124">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="c7e8e-124">-SubnetName</span></span>
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

### <span data-ttu-id="c7e8e-125">-VM</span><span class="sxs-lookup"><span data-stu-id="c7e8e-125">-VM</span></span>
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

### <span data-ttu-id="c7e8e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7e8e-126">CommonParameters</span></span>
<span data-ttu-id="c7e8e-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7e8e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7e8e-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7e8e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7e8e-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7e8e-129">INPUTS</span></span>

## <span data-ttu-id="c7e8e-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7e8e-130">OUTPUTS</span></span>

## <span data-ttu-id="c7e8e-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7e8e-131">NOTES</span></span>

## <span data-ttu-id="c7e8e-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7e8e-132">RELATED LINKS</span></span>

[<span data-ttu-id="c7e8e-133">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="c7e8e-133">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="c7e8e-134">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="c7e8e-134">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="c7e8e-135">Satz-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="c7e8e-135">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


