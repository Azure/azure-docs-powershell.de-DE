---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: 4fbc1729debb7f5cf822f152107797e10b1f7ba9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473464"
---
# <span data-ttu-id="16fa3-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="16fa3-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="16fa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="16fa3-103">Erstellt eine Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="16fa3-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="16fa3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16fa3-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16fa3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16fa3-105">DESCRIPTION</span></span>
<span data-ttu-id="16fa3-106">Das **Cmdlet "New-AzServiceEndpointPolicy"** erstellt eine Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="16fa3-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="16fa3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="16fa3-107">EXAMPLES</span></span>

### <span data-ttu-id="16fa3-108">Beispiel 1: Erstellen einer Dienstendpunktrichtlinie</span><span class="sxs-lookup"><span data-stu-id="16fa3-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="16fa3-109">Mit diesem Befehl wird eine Dienstendpunktrichtlinie namens "Richtlinie1" mit Definitionen erstellt, die vom Objektobjekt definiert $serviceEndpointDefinition und diese in der variablen $serviceEndpointPolicy gespeichert.</span><span class="sxs-lookup"><span data-stu-id="16fa3-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="16fa3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16fa3-110">PARAMETERS</span></span>

### <span data-ttu-id="16fa3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16fa3-111">-DefaultProfile</span></span>
<span data-ttu-id="16fa3-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="16fa3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16fa3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="16fa3-113">-Force</span></span>
<span data-ttu-id="16fa3-114">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="16fa3-114">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="16fa3-115">-Location</span><span class="sxs-lookup"><span data-stu-id="16fa3-115">-Location</span></span>
<span data-ttu-id="16fa3-116">aus.</span><span class="sxs-lookup"><span data-stu-id="16fa3-116">location.</span></span>

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

### <span data-ttu-id="16fa3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="16fa3-117">-Name</span></span>
<span data-ttu-id="16fa3-118">Der Name des Subnetzes</span><span class="sxs-lookup"><span data-stu-id="16fa3-118">The name of the subnet</span></span>

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

### <span data-ttu-id="16fa3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16fa3-119">-ResourceGroupName</span></span>
<span data-ttu-id="16fa3-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="16fa3-120">The resource group name.</span></span>

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

### <span data-ttu-id="16fa3-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="16fa3-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="16fa3-122">Liste der Endpunktdefinitionen für Dienste</span><span class="sxs-lookup"><span data-stu-id="16fa3-122">List of service endpoint definitions</span></span>

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

### <span data-ttu-id="16fa3-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16fa3-123">-Confirm</span></span>
<span data-ttu-id="16fa3-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="16fa3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16fa3-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="16fa3-125">-WhatIf</span></span>
<span data-ttu-id="16fa3-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16fa3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16fa3-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16fa3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16fa3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16fa3-128">CommonParameters</span></span>
<span data-ttu-id="16fa3-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16fa3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16fa3-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16fa3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16fa3-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="16fa3-131">INPUTS</span></span>

### <span data-ttu-id="16fa3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="16fa3-132">System.String</span></span>

## <span data-ttu-id="16fa3-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="16fa3-133">OUTPUTS</span></span>

### <span data-ttu-id="16fa3-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="16fa3-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="16fa3-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="16fa3-135">NOTES</span></span>

## <span data-ttu-id="16fa3-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="16fa3-136">RELATED LINKS</span></span>

[<span data-ttu-id="16fa3-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="16fa3-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="16fa3-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="16fa3-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="16fa3-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="16fa3-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
