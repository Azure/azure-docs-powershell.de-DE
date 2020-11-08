---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 846B9EB8-8EC2-4BDA-90EF-59098696F460
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c4e1dedb02286ceaab182e0912198c23ec03ee5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005999"
---
# <span data-ttu-id="fe4d6-101">Set-AzureVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="fe4d6-101">Set-AzureVMBootDiagnostics</span></span>

## <span data-ttu-id="fe4d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fe4d6-102">SYNOPSIS</span></span>

## <span data-ttu-id="fe4d6-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe4d6-103">SYNTAX</span></span>

### <span data-ttu-id="fe4d6-104">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="fe4d6-104">EnableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Enable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fe4d6-105">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="fe4d6-105">DisableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fe4d6-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe4d6-106">DESCRIPTION</span></span>

## <span data-ttu-id="fe4d6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe4d6-107">EXAMPLES</span></span>

### <span data-ttu-id="fe4d6-108">1:</span><span class="sxs-lookup"><span data-stu-id="fe4d6-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="fe4d6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe4d6-109">PARAMETERS</span></span>

### <span data-ttu-id="fe4d6-110">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="fe4d6-110">-Disable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4d6-111">-Enable</span><span class="sxs-lookup"><span data-stu-id="fe4d6-111">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4d6-112">-Information</span><span class="sxs-lookup"><span data-stu-id="fe4d6-112">-InformationAction</span></span>
<span data-ttu-id="fe4d6-113">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="fe4d6-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fe4d6-114">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fe4d6-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fe4d6-115">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="fe4d6-115">Continue</span></span>
- <span data-ttu-id="fe4d6-116">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="fe4d6-116">Ignore</span></span>
- <span data-ttu-id="fe4d6-117">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="fe4d6-117">Inquire</span></span>
- <span data-ttu-id="fe4d6-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fe4d6-118">SilentlyContinue</span></span>
- <span data-ttu-id="fe4d6-119">Beenden</span><span class="sxs-lookup"><span data-stu-id="fe4d6-119">Stop</span></span>
- <span data-ttu-id="fe4d6-120">Anhalten</span><span class="sxs-lookup"><span data-stu-id="fe4d6-120">Suspend</span></span>

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

### <span data-ttu-id="fe4d6-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fe4d6-121">-InformationVariable</span></span>
<span data-ttu-id="fe4d6-122">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="fe4d6-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fe4d6-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="fe4d6-123">-Profile</span></span>
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

### <span data-ttu-id="fe4d6-124">-VM</span><span class="sxs-lookup"><span data-stu-id="fe4d6-124">-VM</span></span>
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

### <span data-ttu-id="fe4d6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe4d6-125">CommonParameters</span></span>
<span data-ttu-id="fe4d6-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe4d6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe4d6-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe4d6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe4d6-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fe4d6-128">INPUTS</span></span>

## <span data-ttu-id="fe4d6-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fe4d6-129">OUTPUTS</span></span>

## <span data-ttu-id="fe4d6-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="fe4d6-130">NOTES</span></span>

## <span data-ttu-id="fe4d6-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fe4d6-131">RELATED LINKS</span></span>

