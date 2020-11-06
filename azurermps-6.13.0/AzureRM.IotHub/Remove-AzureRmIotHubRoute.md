---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoute.md
ms.openlocfilehash: 9af711bd449bc8c69808f30dc99ceea806dee00d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503657"
---
# <span data-ttu-id="198b6-101">Remove-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="198b6-101">Remove-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="198b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="198b6-102">SYNOPSIS</span></span>
<span data-ttu-id="198b6-103">Löschen einer Route in "viel Hub"</span><span class="sxs-lookup"><span data-stu-id="198b6-103">Delete a route in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="198b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="198b6-104">SYNTAX</span></span>

### <span data-ttu-id="198b6-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="198b6-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="198b6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="198b6-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="198b6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="198b6-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="198b6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="198b6-108">DESCRIPTION</span></span>
<span data-ttu-id="198b6-109">Löschen von Routen zu einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="198b6-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="198b6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="198b6-110">EXAMPLES</span></span>

### <span data-ttu-id="198b6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="198b6-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="198b6-112">Löschen Sie die Route "R1" vom Hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="198b6-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="198b6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="198b6-113">PARAMETERS</span></span>

### <span data-ttu-id="198b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="198b6-114">-DefaultProfile</span></span>
<span data-ttu-id="198b6-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="198b6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="198b6-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="198b6-116">-InputObject</span></span>
<span data-ttu-id="198b6-117">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="198b6-117">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="198b6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="198b6-118">-Name</span></span>
<span data-ttu-id="198b6-119">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="198b6-119">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="198b6-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="198b6-120">-PassThru</span></span>
<span data-ttu-id="198b6-121">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="198b6-121">Allows to return the boolean object.</span></span> <span data-ttu-id="198b6-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="198b6-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="198b6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="198b6-123">-ResourceGroupName</span></span>
<span data-ttu-id="198b6-124">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="198b6-124">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="198b6-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="198b6-125">-ResourceId</span></span>
<span data-ttu-id="198b6-126">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="198b6-126">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="198b6-127">-Routename</span><span class="sxs-lookup"><span data-stu-id="198b6-127">-RouteName</span></span>
<span data-ttu-id="198b6-128">Name der Route</span><span class="sxs-lookup"><span data-stu-id="198b6-128">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="198b6-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="198b6-129">-Confirm</span></span>
<span data-ttu-id="198b6-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="198b6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="198b6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="198b6-131">-WhatIf</span></span>
<span data-ttu-id="198b6-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="198b6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="198b6-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="198b6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="198b6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="198b6-134">CommonParameters</span></span>
<span data-ttu-id="198b6-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="198b6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="198b6-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="198b6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="198b6-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="198b6-137">INPUTS</span></span>

### <span data-ttu-id="198b6-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="198b6-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="198b6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="198b6-139">System.String</span></span>

## <span data-ttu-id="198b6-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="198b6-140">OUTPUTS</span></span>

### <span data-ttu-id="198b6-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="198b6-141">System.Boolean</span></span>

## <span data-ttu-id="198b6-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="198b6-142">NOTES</span></span>

## <span data-ttu-id="198b6-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="198b6-143">RELATED LINKS</span></span>
