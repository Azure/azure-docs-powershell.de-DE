---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRoutePort.md
ms.openlocfilehash: 46f73d2a58fe5f1109de6a15a5cb39e3b568a4b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500165"
---
# <span data-ttu-id="ca8e7-101">Set-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ca8e7-101">Set-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="ca8e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ca8e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ca8e7-103">Ändert eine ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-103">Modifies an ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca8e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca8e7-104">SYNTAX</span></span>

```
Set-AzureRmExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca8e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca8e7-105">DESCRIPTION</span></span>
<span data-ttu-id="ca8e7-106">Das Cmdlet " **Satz-AzureRmExpressRoutePort** " speichert das geänderte ExpressRoutePort in Azure.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-106">The **Set-AzureRmExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="ca8e7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca8e7-107">EXAMPLES</span></span>

### <span data-ttu-id="ca8e7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ca8e7-108">Example 1</span></span>
```powershell
$erport = Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzureRmExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="ca8e7-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ca8e7-109">Example 2</span></span>
```powershell
$erport = Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzureRmExpressRoutePort -InputObject $erport
```

<span data-ttu-id="ca8e7-110">Ändert den Administratorstatus eines Links einer ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ca8e7-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="ca8e7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca8e7-111">PARAMETERS</span></span>

### <span data-ttu-id="ca8e7-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca8e7-112">-AsJob</span></span>
<span data-ttu-id="ca8e7-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ca8e7-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca8e7-114">-DefaultProfile</span></span>
<span data-ttu-id="ca8e7-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8e7-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ca8e7-116">-ExpressRoutePort</span></span>
<span data-ttu-id="ca8e7-117">Das ExpressRoutePort-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-117">The ExpressRoutePort object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8e7-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ca8e7-118">-Confirm</span></span>
<span data-ttu-id="ca8e7-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8e7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca8e7-120">-WhatIf</span></span>
<span data-ttu-id="ca8e7-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca8e7-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8e7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca8e7-123">CommonParameters</span></span>
<span data-ttu-id="ca8e7-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca8e7-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca8e7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca8e7-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ca8e7-126">INPUTS</span></span>

### <span data-ttu-id="ca8e7-127">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ca8e7-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="ca8e7-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ca8e7-128">OUTPUTS</span></span>

### <span data-ttu-id="ca8e7-129">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ca8e7-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="ca8e7-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ca8e7-130">NOTES</span></span>

## <span data-ttu-id="ca8e7-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ca8e7-131">RELATED LINKS</span></span>
