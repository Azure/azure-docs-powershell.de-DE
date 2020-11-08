---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
ms.openlocfilehash: f5463015b93c209c6cf8952c566e9656da2fba18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008445"
---
# <span data-ttu-id="6783c-101">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="6783c-101">Remove-AzIotHubDeployment</span></span>

## <span data-ttu-id="6783c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6783c-102">SYNOPSIS</span></span>
<span data-ttu-id="6783c-103">Löschen Sie eine viel Edge-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="6783c-103">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="6783c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6783c-104">SYNTAX</span></span>

### <span data-ttu-id="6783c-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6783c-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6783c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6783c-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6783c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6783c-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6783c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6783c-108">DESCRIPTION</span></span>
<span data-ttu-id="6783c-109">Weitere Informationen finden Sie unter https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring .</span><span class="sxs-lookup"><span data-stu-id="6783c-109">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="6783c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6783c-110">EXAMPLES</span></span>

### <span data-ttu-id="6783c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6783c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="6783c-112">Löschen Sie eine viel Edge-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="6783c-112">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="6783c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6783c-113">PARAMETERS</span></span>

### <span data-ttu-id="6783c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6783c-114">-DefaultProfile</span></span>
<span data-ttu-id="6783c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6783c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6783c-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6783c-116">-InputObject</span></span>
<span data-ttu-id="6783c-117">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="6783c-117">IotHub object</span></span>

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

### <span data-ttu-id="6783c-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6783c-118">-IotHubName</span></span>
<span data-ttu-id="6783c-119">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="6783c-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6783c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6783c-120">-Name</span></span>
<span data-ttu-id="6783c-121">Bezeichner für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="6783c-121">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="6783c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6783c-122">-PassThru</span></span>
<span data-ttu-id="6783c-123">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="6783c-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="6783c-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="6783c-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6783c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6783c-125">-ResourceGroupName</span></span>
<span data-ttu-id="6783c-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6783c-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6783c-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6783c-127">-ResourceId</span></span>
<span data-ttu-id="6783c-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="6783c-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6783c-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6783c-129">-Confirm</span></span>
<span data-ttu-id="6783c-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6783c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6783c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6783c-131">-WhatIf</span></span>
<span data-ttu-id="6783c-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6783c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6783c-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6783c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6783c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6783c-134">CommonParameters</span></span>
<span data-ttu-id="6783c-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6783c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6783c-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6783c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6783c-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6783c-137">INPUTS</span></span>

### <span data-ttu-id="6783c-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6783c-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6783c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6783c-139">System.String</span></span>

## <span data-ttu-id="6783c-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6783c-140">OUTPUTS</span></span>

### <span data-ttu-id="6783c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6783c-141">System.Boolean</span></span>

## <span data-ttu-id="6783c-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="6783c-142">NOTES</span></span>

## <span data-ttu-id="6783c-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6783c-143">RELATED LINKS</span></span>
