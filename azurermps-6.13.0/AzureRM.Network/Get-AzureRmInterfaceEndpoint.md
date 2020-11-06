---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurerminterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
ms.openlocfilehash: 8759546c9d7161f2bea139845c7d291c6d7832b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495954"
---
# <span data-ttu-id="e5411-101">Get-AzureRmInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5411-101">Get-AzureRmInterfaceEndpoint</span></span>

## <span data-ttu-id="e5411-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5411-102">SYNOPSIS</span></span>
<span data-ttu-id="e5411-103">Das Get-AzureRmInterfaceEndpoint-Cmdlet ruft einen Schnittstellen Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="e5411-103">The Get-AzureRmInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5411-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5411-104">SYNTAX</span></span>

### <span data-ttu-id="e5411-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5411-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmInterfaceEndpoint [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5411-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5411-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5411-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5411-107">DESCRIPTION</span></span>
<span data-ttu-id="e5411-108">Das Cmdlet " **Get-AzureRmInterfaceEndpoint** " Ruft einen Schnittstellen Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="e5411-108">The **Get-AzureRmInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="e5411-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5411-109">EXAMPLES</span></span>

### <span data-ttu-id="e5411-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5411-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e5411-111">Dieser Befehl ruft den Schnittstellen Endpunkt mit dem Namen InterfaceEndpoint1 ab, der zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert ihn in der $interfaceendpoint Variablen.</span><span class="sxs-lookup"><span data-stu-id="e5411-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="e5411-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e5411-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"

```

<span data-ttu-id="e5411-113">Dieser Befehl ruft den Schnittstellen Endpunkt mit der/Subscriptions/Sub1/resourceGroups/chsriniIEtest1/Providers/Microsoft.Network/interfaceEndpoints/IE1.10-Funktion ab und speichert ihn in der $interfaceendpoint-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e5411-113">This command gets the interface endpoint with resourceId  /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>


## <span data-ttu-id="e5411-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5411-114">PARAMETERS</span></span>

### <span data-ttu-id="e5411-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5411-115">-DefaultProfile</span></span>
<span data-ttu-id="e5411-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5411-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5411-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e5411-117">-Name</span></span>
<span data-ttu-id="e5411-118">Der Name des Schnittstellen Endpunkts</span><span class="sxs-lookup"><span data-stu-id="e5411-118">The name of the interface endpoint</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5411-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5411-119">-ResourceGroupName</span></span>
<span data-ttu-id="e5411-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e5411-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5411-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e5411-121">-ResourceId</span></span>
<span data-ttu-id="e5411-122">{{Fill resourcel Description}}</span><span class="sxs-lookup"><span data-stu-id="e5411-122">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5411-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e5411-123">-Confirm</span></span>
<span data-ttu-id="e5411-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5411-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5411-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5411-125">-WhatIf</span></span>
<span data-ttu-id="e5411-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5411-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5411-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5411-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5411-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5411-128">CommonParameters</span></span>
<span data-ttu-id="e5411-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5411-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e5411-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5411-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5411-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5411-131">INPUTS</span></span>

### <span data-ttu-id="e5411-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e5411-132">System.String</span></span>


## <span data-ttu-id="e5411-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5411-133">OUTPUTS</span></span>

### <span data-ttu-id="e5411-134">Microsoft. Azure. Commands. Network. Models. PSInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5411-134">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>


## <span data-ttu-id="e5411-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5411-135">NOTES</span></span>

## <span data-ttu-id="e5411-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5411-136">RELATED LINKS</span></span>
