---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: 9b03a33ebea52e57950e46c894e95ffefe520b4e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821503"
---
# <span data-ttu-id="b04bd-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b04bd-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="b04bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b04bd-102">SYNOPSIS</span></span>
<span data-ttu-id="b04bd-103">Erstellt eine Dienstendpunkt Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="b04bd-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="b04bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b04bd-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b04bd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b04bd-105">DESCRIPTION</span></span>
<span data-ttu-id="b04bd-106">Mit dem Cmdlet **New-AzServiceEndpointPolicy** können Sie eine Dienstendpunkt Richtlinie erstellen.</span><span class="sxs-lookup"><span data-stu-id="b04bd-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="b04bd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b04bd-107">EXAMPLES</span></span>

### <span data-ttu-id="b04bd-108">Beispiel 1: Erstellen einer Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="b04bd-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="b04bd-109">Mit diesem Befehl wird eine Dienstendpunkt Richtlinie mit dem Namen "Fischereipolitik1" erstellt, deren Definitionen vom Objekt $serviceEndpointDefinition und in der $serviceEndpointPolicy-Variablen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b04bd-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="b04bd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b04bd-110">PARAMETERS</span></span>

### <span data-ttu-id="b04bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b04bd-111">-DefaultProfile</span></span>
<span data-ttu-id="b04bd-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b04bd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b04bd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b04bd-113">-Force</span></span>
<span data-ttu-id="b04bd-114">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="b04bd-114">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b04bd-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="b04bd-115">-Location</span></span>
<span data-ttu-id="b04bd-116">Lage.</span><span class="sxs-lookup"><span data-stu-id="b04bd-116">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b04bd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b04bd-117">-Name</span></span>
<span data-ttu-id="b04bd-118">Der Name des Subnets</span><span class="sxs-lookup"><span data-stu-id="b04bd-118">The name of the subnet</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b04bd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b04bd-119">-ResourceGroupName</span></span>
<span data-ttu-id="b04bd-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b04bd-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b04bd-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b04bd-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="b04bd-122">Liste der Dienstendpunkt Definitionen</span><span class="sxs-lookup"><span data-stu-id="b04bd-122">List of service endpoint definitions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b04bd-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b04bd-123">-Confirm</span></span>
<span data-ttu-id="b04bd-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b04bd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b04bd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b04bd-125">-WhatIf</span></span>
<span data-ttu-id="b04bd-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b04bd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b04bd-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b04bd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b04bd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b04bd-128">CommonParameters</span></span>
<span data-ttu-id="b04bd-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b04bd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b04bd-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b04bd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b04bd-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b04bd-131">INPUTS</span></span>

### <span data-ttu-id="b04bd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b04bd-132">System.String</span></span>

## <span data-ttu-id="b04bd-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b04bd-133">OUTPUTS</span></span>

### <span data-ttu-id="b04bd-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b04bd-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="b04bd-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b04bd-135">NOTES</span></span>

## <span data-ttu-id="b04bd-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b04bd-136">RELATED LINKS</span></span>

[<span data-ttu-id="b04bd-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b04bd-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="b04bd-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b04bd-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="b04bd-139">Satz-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b04bd-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
