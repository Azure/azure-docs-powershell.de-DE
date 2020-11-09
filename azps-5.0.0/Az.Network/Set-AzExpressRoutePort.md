---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: b5170ef175b93bc977ba047d4188d51de2858e63
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301396"
---
# <span data-ttu-id="a063e-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a063e-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="a063e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a063e-102">SYNOPSIS</span></span>
<span data-ttu-id="a063e-103">Ändert eine ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a063e-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="a063e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a063e-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a063e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a063e-105">DESCRIPTION</span></span>
<span data-ttu-id="a063e-106">Das Cmdlet " **Satz-AzExpressRoutePort** " speichert das geänderte ExpressRoutePort in Azure.</span><span class="sxs-lookup"><span data-stu-id="a063e-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="a063e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a063e-107">EXAMPLES</span></span>

### <span data-ttu-id="a063e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a063e-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="a063e-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a063e-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="a063e-110">Ändert den Administratorstatus eines Links einer ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a063e-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="a063e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a063e-111">PARAMETERS</span></span>

### <span data-ttu-id="a063e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a063e-112">-AsJob</span></span>
<span data-ttu-id="a063e-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a063e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a063e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a063e-114">-DefaultProfile</span></span>
<span data-ttu-id="a063e-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a063e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a063e-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a063e-116">-ExpressRoutePort</span></span>
<span data-ttu-id="a063e-117">Das ExpressRoutePort-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a063e-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="a063e-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a063e-118">-Confirm</span></span>
<span data-ttu-id="a063e-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a063e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a063e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a063e-120">-WhatIf</span></span>
<span data-ttu-id="a063e-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a063e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a063e-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a063e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a063e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a063e-123">CommonParameters</span></span>
<span data-ttu-id="a063e-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a063e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a063e-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a063e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a063e-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a063e-126">INPUTS</span></span>

### <span data-ttu-id="a063e-127">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a063e-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="a063e-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a063e-128">OUTPUTS</span></span>

### <span data-ttu-id="a063e-129">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a063e-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="a063e-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="a063e-130">NOTES</span></span>

## <span data-ttu-id="a063e-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a063e-131">RELATED LINKS</span></span>

[<span data-ttu-id="a063e-132">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a063e-132">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="a063e-133">Neu – AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a063e-133">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="a063e-134">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a063e-134">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
