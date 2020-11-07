---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azinterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
ms.openlocfilehash: 55133225b380e16112301620a52f857fca50dc0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660769"
---
# <span data-ttu-id="a6217-101">Get-AzInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6217-101">Get-AzInterfaceEndpoint</span></span>

## <span data-ttu-id="a6217-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a6217-102">SYNOPSIS</span></span>
<span data-ttu-id="a6217-103">Das Get-AzInterfaceEndpoint-Cmdlet ruft einen Schnittstellen Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="a6217-103">The Get-AzInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="a6217-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6217-104">SYNTAX</span></span>

### <span data-ttu-id="a6217-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a6217-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzInterfaceEndpoint [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6217-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6217-106">GetByResourceIdParameterSet</span></span>
```
Get-AzInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6217-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6217-107">DESCRIPTION</span></span>
<span data-ttu-id="a6217-108">Das Cmdlet " **Get-AzInterfaceEndpoint** " Ruft einen Schnittstellen Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="a6217-108">The **Get-AzInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="a6217-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6217-109">EXAMPLES</span></span>

### <span data-ttu-id="a6217-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a6217-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a6217-111">Dieser Befehl ruft den Schnittstellen Endpunkt mit dem Namen InterfaceEndpoint1 ab, der zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert ihn in der $interfaceendpoint Variablen.</span><span class="sxs-lookup"><span data-stu-id="a6217-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="a6217-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a6217-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"
```

<span data-ttu-id="a6217-113">Dieser Befehl ruft den Schnittstellen Endpunkt mit der/Subscriptions/Sub1/resourceGroups/chsriniIEtest1/Providers/Microsoft.Network/interfaceEndpoints/IE1.10-Funktion ab und speichert ihn in der $interfaceendpoint-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a6217-113">This command gets the interface endpoint with resourceId /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="a6217-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a6217-114">Example 3</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name InterfaceEndpoint*
```

<span data-ttu-id="a6217-115">Dieser Befehl ruft die Endpunkte der Schnittstelle ab, die mit "InterfaceEndpoint" beginnen.</span><span class="sxs-lookup"><span data-stu-id="a6217-115">This command gets the interface endpoints that start with "InterfaceEndpoint"</span></span>

## <span data-ttu-id="a6217-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6217-116">PARAMETERS</span></span>

### <span data-ttu-id="a6217-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6217-117">-DefaultProfile</span></span>
<span data-ttu-id="a6217-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a6217-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6217-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a6217-119">-Name</span></span>
<span data-ttu-id="a6217-120">Der Name des Schnittstellen Endpunkts</span><span class="sxs-lookup"><span data-stu-id="a6217-120">The name of the interface endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="a6217-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6217-121">-ResourceGroupName</span></span>
<span data-ttu-id="a6217-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a6217-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a6217-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a6217-123">-ResourceId</span></span>
<span data-ttu-id="a6217-124">Die ID des Schnittstellen Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="a6217-124">The ID of the interface endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6217-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a6217-125">-Confirm</span></span>
<span data-ttu-id="a6217-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6217-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6217-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6217-127">-WhatIf</span></span>
<span data-ttu-id="a6217-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6217-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6217-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6217-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6217-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6217-130">CommonParameters</span></span>
<span data-ttu-id="a6217-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6217-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6217-132">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6217-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6217-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a6217-133">INPUTS</span></span>

### <span data-ttu-id="a6217-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a6217-134">System.String</span></span>

## <span data-ttu-id="a6217-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a6217-135">OUTPUTS</span></span>

### <span data-ttu-id="a6217-136">Microsoft. Azure. Commands. Network. Models. PSInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6217-136">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>

## <span data-ttu-id="a6217-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="a6217-137">NOTES</span></span>

## <span data-ttu-id="a6217-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a6217-138">RELATED LINKS</span></span>
