---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 657c18a02f05f2e318fe676a672e894a4aec9e50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502006"
---
# <span data-ttu-id="084a9-101">New-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="084a9-101">New-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="084a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="084a9-102">SYNOPSIS</span></span>
<span data-ttu-id="084a9-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="084a9-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="084a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="084a9-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicy -Name <String>
 [-ServiceEndpointDefinitions <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]>]
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="084a9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="084a9-105">DESCRIPTION</span></span>
<span data-ttu-id="084a9-106">Mit dem Cmdlet **New-AzureRmServiceEndpointPolicy** können Sie eine Dienstendpunkt Richtlinie erstellen.</span><span class="sxs-lookup"><span data-stu-id="084a9-106">The **New-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="084a9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="084a9-107">EXAMPLES</span></span>

### <span data-ttu-id="084a9-108">Beispiel 1: Erstellen einer Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="084a9-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="084a9-109">Mit diesem Befehl wird eine Dienstendpunkt Richtlinie mit dem Namen "Fischereipolitik1" erstellt, deren Definitionen vom Objekt $serviceEndpointDefinition und in der $serviceEndpointPolicy-Variablen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="084a9-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="084a9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="084a9-110">PARAMETERS</span></span>

### <span data-ttu-id="084a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="084a9-111">-DefaultProfile</span></span>
<span data-ttu-id="084a9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="084a9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084a9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="084a9-113">-Force</span></span>
<span data-ttu-id="084a9-114">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="084a9-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="084a9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="084a9-115">-Name</span></span>
<span data-ttu-id="084a9-116">Der Name des Subnets</span><span class="sxs-lookup"><span data-stu-id="084a9-116">The name of the subnet</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084a9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="084a9-117">-ResourceGroupName</span></span>
<span data-ttu-id="084a9-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="084a9-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="084a9-119">-ServiceEndpointDefinitions</span><span class="sxs-lookup"><span data-stu-id="084a9-119">-ServiceEndpointDefinitions</span></span>
<span data-ttu-id="084a9-120">Liste der Dienstendpunkt Definitionen</span><span class="sxs-lookup"><span data-stu-id="084a9-120">List of service endpoint definitions</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084a9-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="084a9-121">-Confirm</span></span>
<span data-ttu-id="084a9-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="084a9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="084a9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="084a9-123">-WhatIf</span></span>
<span data-ttu-id="084a9-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="084a9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="084a9-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="084a9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="084a9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="084a9-126">CommonParameters</span></span>
<span data-ttu-id="084a9-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="084a9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="084a9-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="084a9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="084a9-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="084a9-129">INPUTS</span></span>

### <span data-ttu-id="084a9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="084a9-130">System.String</span></span>


## <span data-ttu-id="084a9-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="084a9-131">OUTPUTS</span></span>

### <span data-ttu-id="084a9-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="084a9-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="084a9-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="084a9-133">NOTES</span></span>

## <span data-ttu-id="084a9-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="084a9-134">RELATED LINKS</span></span>
