---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 07a29a17a1a7c17a0bbf7b202b019e7d833a5050
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178144"
---
# <span data-ttu-id="2372b-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2372b-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="2372b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2372b-102">SYNOPSIS</span></span>
<span data-ttu-id="2372b-103">Speichert einen geänderten Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="2372b-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="2372b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2372b-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2372b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2372b-105">DESCRIPTION</span></span>
<span data-ttu-id="2372b-106">Das Cmdlet " **Satz-AzSecurityPartnerProvider** " aktualisiert ein Azure-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2372b-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="2372b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2372b-107">EXAMPLES</span></span>

### <span data-ttu-id="2372b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2372b-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="2372b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2372b-109">PARAMETERS</span></span>

### <span data-ttu-id="2372b-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2372b-110">-AsJob</span></span>
<span data-ttu-id="2372b-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2372b-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2372b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2372b-112">-DefaultProfile</span></span>
<span data-ttu-id="2372b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2372b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2372b-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2372b-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="2372b-115">Die SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2372b-115">The SecurityPartnerProvider</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2372b-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2372b-116">-Confirm</span></span>
<span data-ttu-id="2372b-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2372b-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2372b-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2372b-118">-WhatIf</span></span>
<span data-ttu-id="2372b-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2372b-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2372b-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2372b-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2372b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2372b-121">CommonParameters</span></span>
<span data-ttu-id="2372b-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2372b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2372b-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2372b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2372b-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2372b-124">INPUTS</span></span>

### <span data-ttu-id="2372b-125">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2372b-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="2372b-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2372b-126">OUTPUTS</span></span>

### <span data-ttu-id="2372b-127">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2372b-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="2372b-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="2372b-128">NOTES</span></span>

## <span data-ttu-id="2372b-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2372b-129">RELATED LINKS</span></span>
