---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8E64309-7AF6-4439-841E-922B11C072AA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15dd195b86e70ad0a95484417d8cf87b0e544920
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005962"
---
# <span data-ttu-id="86818-101">Set-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="86818-101">Set-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="86818-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86818-102">SYNOPSIS</span></span>

## <span data-ttu-id="86818-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="86818-103">SYNTAX</span></span>

```
Set-AzureNetworkSecurityGroupConfig [-NetworkSecurityGroupName] <String> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="86818-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86818-104">DESCRIPTION</span></span>

## <span data-ttu-id="86818-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86818-105">EXAMPLES</span></span>

### <span data-ttu-id="86818-106">1:</span><span class="sxs-lookup"><span data-stu-id="86818-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="86818-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="86818-107">PARAMETERS</span></span>

### <span data-ttu-id="86818-108">-Information</span><span class="sxs-lookup"><span data-stu-id="86818-108">-InformationAction</span></span>
<span data-ttu-id="86818-109">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="86818-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="86818-110">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="86818-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="86818-111">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="86818-111">Continue</span></span>
- <span data-ttu-id="86818-112">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="86818-112">Ignore</span></span>
- <span data-ttu-id="86818-113">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="86818-113">Inquire</span></span>
- <span data-ttu-id="86818-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="86818-114">SilentlyContinue</span></span>
- <span data-ttu-id="86818-115">Beenden</span><span class="sxs-lookup"><span data-stu-id="86818-115">Stop</span></span>
- <span data-ttu-id="86818-116">Anhalten</span><span class="sxs-lookup"><span data-stu-id="86818-116">Suspend</span></span>

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

### <span data-ttu-id="86818-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="86818-117">-InformationVariable</span></span>
<span data-ttu-id="86818-118">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="86818-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="86818-119">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="86818-119">-NetworkSecurityGroupName</span></span>
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

### <span data-ttu-id="86818-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="86818-120">-Profile</span></span>
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

### <span data-ttu-id="86818-121">-VM</span><span class="sxs-lookup"><span data-stu-id="86818-121">-VM</span></span>
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

### <span data-ttu-id="86818-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86818-122">CommonParameters</span></span>
<span data-ttu-id="86818-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86818-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86818-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86818-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86818-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86818-125">INPUTS</span></span>

## <span data-ttu-id="86818-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86818-126">OUTPUTS</span></span>

## <span data-ttu-id="86818-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="86818-127">NOTES</span></span>

## <span data-ttu-id="86818-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86818-128">RELATED LINKS</span></span>

[<span data-ttu-id="86818-129">Remove-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="86818-129">Remove-AzureNetworkSecurityGroupConfig</span></span>](./Remove-AzureNetworkSecurityGroupConfig.md)


