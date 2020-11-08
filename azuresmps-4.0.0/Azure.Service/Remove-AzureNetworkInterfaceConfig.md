---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 185C2680-501F-497D-81B2-5F6E30A91F16
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55e9f6f026e7e524613a0e070767bc2ab26f6d66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006672"
---
# <span data-ttu-id="2ddbf-101">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="2ddbf-101">Remove-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="2ddbf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ddbf-102">SYNOPSIS</span></span>

## <span data-ttu-id="2ddbf-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ddbf-103">SYNTAX</span></span>

```
Remove-AzureNetworkInterfaceConfig [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2ddbf-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ddbf-104">DESCRIPTION</span></span>

## <span data-ttu-id="2ddbf-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ddbf-105">EXAMPLES</span></span>

### <span data-ttu-id="2ddbf-106">1:</span><span class="sxs-lookup"><span data-stu-id="2ddbf-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="2ddbf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ddbf-107">PARAMETERS</span></span>

### <span data-ttu-id="2ddbf-108">-Information</span><span class="sxs-lookup"><span data-stu-id="2ddbf-108">-InformationAction</span></span>
<span data-ttu-id="2ddbf-109">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="2ddbf-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2ddbf-110">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2ddbf-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2ddbf-111">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="2ddbf-111">Continue</span></span>
- <span data-ttu-id="2ddbf-112">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="2ddbf-112">Ignore</span></span>
- <span data-ttu-id="2ddbf-113">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="2ddbf-113">Inquire</span></span>
- <span data-ttu-id="2ddbf-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2ddbf-114">SilentlyContinue</span></span>
- <span data-ttu-id="2ddbf-115">Beenden</span><span class="sxs-lookup"><span data-stu-id="2ddbf-115">Stop</span></span>
- <span data-ttu-id="2ddbf-116">Anhalten</span><span class="sxs-lookup"><span data-stu-id="2ddbf-116">Suspend</span></span>

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

### <span data-ttu-id="2ddbf-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2ddbf-117">-InformationVariable</span></span>
<span data-ttu-id="2ddbf-118">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="2ddbf-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2ddbf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2ddbf-119">-Name</span></span>
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

### <span data-ttu-id="2ddbf-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="2ddbf-120">-Profile</span></span>
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

### <span data-ttu-id="2ddbf-121">-VM</span><span class="sxs-lookup"><span data-stu-id="2ddbf-121">-VM</span></span>
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

### <span data-ttu-id="2ddbf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ddbf-122">CommonParameters</span></span>
<span data-ttu-id="2ddbf-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ddbf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ddbf-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ddbf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ddbf-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ddbf-125">INPUTS</span></span>

## <span data-ttu-id="2ddbf-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ddbf-126">OUTPUTS</span></span>

## <span data-ttu-id="2ddbf-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ddbf-127">NOTES</span></span>

## <span data-ttu-id="2ddbf-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ddbf-128">RELATED LINKS</span></span>

[<span data-ttu-id="2ddbf-129">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="2ddbf-129">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="2ddbf-130">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="2ddbf-130">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="2ddbf-131">Satz-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="2ddbf-131">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


