---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
ms.openlocfilehash: 0b87bece7bca0ea3f534746dd20a163f69f21262
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008447"
---
# <span data-ttu-id="0b6d4-101">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b6d4-101">Remove-AzIotHubConfiguration</span></span>

## <span data-ttu-id="0b6d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b6d4-102">SYNOPSIS</span></span>
<span data-ttu-id="0b6d4-103">Löschen Sie eine viel Gerätekonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0b6d4-103">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="0b6d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b6d4-104">SYNTAX</span></span>

### <span data-ttu-id="0b6d4-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b6d4-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b6d4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0b6d4-106">InputObjectSet</span></span>
```
Remove-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b6d4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0b6d4-107">ResourceIdSet</span></span>
```
Remove-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b6d4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b6d4-108">DESCRIPTION</span></span>
<span data-ttu-id="0b6d4-109">Weitere Informationen finden Sie unter https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management .</span><span class="sxs-lookup"><span data-stu-id="0b6d4-109">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="0b6d4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b6d4-110">EXAMPLES</span></span>

### <span data-ttu-id="0b6d4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0b6d4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="0b6d4-112">Löschen Sie eine viel Gerätekonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0b6d4-112">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="0b6d4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b6d4-113">PARAMETERS</span></span>

### <span data-ttu-id="0b6d4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b6d4-114">-DefaultProfile</span></span>
<span data-ttu-id="0b6d4-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b6d4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b6d4-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0b6d4-116">-InputObject</span></span>
<span data-ttu-id="0b6d4-117">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="0b6d4-117">IotHub object</span></span>

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

### <span data-ttu-id="0b6d4-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="0b6d4-118">-IotHubName</span></span>
<span data-ttu-id="0b6d4-119">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="0b6d4-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0b6d4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0b6d4-120">-Name</span></span>
<span data-ttu-id="0b6d4-121">Bezeichner für die Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0b6d4-121">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="0b6d4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b6d4-122">-PassThru</span></span>
<span data-ttu-id="0b6d4-123">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="0b6d4-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="0b6d4-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="0b6d4-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0b6d4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b6d4-125">-ResourceGroupName</span></span>
<span data-ttu-id="0b6d4-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0b6d4-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0b6d4-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0b6d4-127">-ResourceId</span></span>
<span data-ttu-id="0b6d4-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="0b6d4-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0b6d4-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b6d4-129">-Confirm</span></span>
<span data-ttu-id="0b6d4-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b6d4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b6d4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b6d4-131">-WhatIf</span></span>
<span data-ttu-id="0b6d4-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b6d4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b6d4-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b6d4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b6d4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b6d4-134">CommonParameters</span></span>
<span data-ttu-id="0b6d4-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b6d4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b6d4-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b6d4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b6d4-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b6d4-137">INPUTS</span></span>

### <span data-ttu-id="0b6d4-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0b6d4-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0b6d4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0b6d4-139">System.String</span></span>

## <span data-ttu-id="0b6d4-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b6d4-140">OUTPUTS</span></span>

### <span data-ttu-id="0b6d4-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0b6d4-141">System.Boolean</span></span>

## <span data-ttu-id="0b6d4-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b6d4-142">NOTES</span></span>

## <span data-ttu-id="0b6d4-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b6d4-143">RELATED LINKS</span></span>
