---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EE96AC92-02A8-4A40-A26D-0882673E51A5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2dca85290564217f5c4c319ef3531d4c31500fcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006790"
---
# <span data-ttu-id="1bf69-101">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="1bf69-101">Get-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="1bf69-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1bf69-102">SYNOPSIS</span></span>

## <span data-ttu-id="1bf69-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bf69-103">SYNTAX</span></span>

```
Get-AzureNetworkInterfaceConfig [[-Name] <String>] -VM <PersistentVMRoleContext>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1bf69-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1bf69-104">DESCRIPTION</span></span>

## <span data-ttu-id="1bf69-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1bf69-105">EXAMPLES</span></span>

### <span data-ttu-id="1bf69-106">1:</span><span class="sxs-lookup"><span data-stu-id="1bf69-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="1bf69-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bf69-107">PARAMETERS</span></span>

### <span data-ttu-id="1bf69-108">-Information</span><span class="sxs-lookup"><span data-stu-id="1bf69-108">-InformationAction</span></span>
<span data-ttu-id="1bf69-109">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="1bf69-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1bf69-110">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1bf69-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1bf69-111">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="1bf69-111">Continue</span></span>
- <span data-ttu-id="1bf69-112">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="1bf69-112">Ignore</span></span>
- <span data-ttu-id="1bf69-113">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="1bf69-113">Inquire</span></span>
- <span data-ttu-id="1bf69-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1bf69-114">SilentlyContinue</span></span>
- <span data-ttu-id="1bf69-115">Beenden</span><span class="sxs-lookup"><span data-stu-id="1bf69-115">Stop</span></span>
- <span data-ttu-id="1bf69-116">Anhalten</span><span class="sxs-lookup"><span data-stu-id="1bf69-116">Suspend</span></span>

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

### <span data-ttu-id="1bf69-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1bf69-117">-InformationVariable</span></span>
<span data-ttu-id="1bf69-118">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="1bf69-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1bf69-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1bf69-119">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf69-120">-VM</span><span class="sxs-lookup"><span data-stu-id="1bf69-120">-VM</span></span>
```yaml
Type: PersistentVMRoleContext
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf69-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf69-121">CommonParameters</span></span>
<span data-ttu-id="1bf69-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf69-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf69-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bf69-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf69-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1bf69-124">INPUTS</span></span>

## <span data-ttu-id="1bf69-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1bf69-125">OUTPUTS</span></span>

## <span data-ttu-id="1bf69-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="1bf69-126">NOTES</span></span>

## <span data-ttu-id="1bf69-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1bf69-127">RELATED LINKS</span></span>

[<span data-ttu-id="1bf69-128">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="1bf69-128">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="1bf69-129">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="1bf69-129">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="1bf69-130">Satz-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="1bf69-130">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


