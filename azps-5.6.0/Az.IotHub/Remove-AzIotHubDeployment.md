---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
ms.openlocfilehash: a125bd402a58bc138e1fa74ec2f68d659f2a1d1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928008"
---
# <span data-ttu-id="fcd9f-101">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="fcd9f-101">Remove-AzIotHubDeployment</span></span>

## <span data-ttu-id="fcd9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcd9f-102">SYNOPSIS</span></span>
<span data-ttu-id="fcd9f-103">Löschen Sie eine IoT Edge-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="fcd9f-103">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="fcd9f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcd9f-104">SYNTAX</span></span>

### <span data-ttu-id="fcd9f-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fcd9f-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcd9f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fcd9f-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcd9f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fcd9f-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcd9f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fcd9f-108">DESCRIPTION</span></span>
<span data-ttu-id="fcd9f-109">Weitere https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring Informationen finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="fcd9f-109">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="fcd9f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fcd9f-110">EXAMPLES</span></span>

### <span data-ttu-id="fcd9f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fcd9f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="fcd9f-112">Löschen Sie eine IoT Edge-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="fcd9f-112">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="fcd9f-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fcd9f-113">PARAMETERS</span></span>

### <span data-ttu-id="fcd9f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcd9f-114">-DefaultProfile</span></span>
<span data-ttu-id="fcd9f-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fcd9f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcd9f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcd9f-116">-InputObject</span></span>
<span data-ttu-id="fcd9f-117">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="fcd9f-117">IotHub object</span></span>

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

### <span data-ttu-id="fcd9f-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fcd9f-118">-IotHubName</span></span>
<span data-ttu-id="fcd9f-119">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="fcd9f-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fcd9f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fcd9f-120">-Name</span></span>
<span data-ttu-id="fcd9f-121">Bezeichner für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="fcd9f-121">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="fcd9f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcd9f-122">-PassThru</span></span>
<span data-ttu-id="fcd9f-123">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="fcd9f-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="fcd9f-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="fcd9f-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fcd9f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcd9f-125">-ResourceGroupName</span></span>
<span data-ttu-id="fcd9f-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="fcd9f-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fcd9f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fcd9f-127">-ResourceId</span></span>
<span data-ttu-id="fcd9f-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="fcd9f-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fcd9f-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fcd9f-129">-Confirm</span></span>
<span data-ttu-id="fcd9f-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fcd9f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcd9f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcd9f-131">-WhatIf</span></span>
<span data-ttu-id="fcd9f-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fcd9f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcd9f-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fcd9f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcd9f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcd9f-134">CommonParameters</span></span>
<span data-ttu-id="fcd9f-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcd9f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcd9f-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcd9f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcd9f-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fcd9f-137">INPUTS</span></span>

### <span data-ttu-id="fcd9f-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fcd9f-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fcd9f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="fcd9f-139">System.String</span></span>

## <span data-ttu-id="fcd9f-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fcd9f-140">OUTPUTS</span></span>

### <span data-ttu-id="fcd9f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fcd9f-141">System.Boolean</span></span>

## <span data-ttu-id="fcd9f-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fcd9f-142">NOTES</span></span>

## <span data-ttu-id="fcd9f-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fcd9f-143">RELATED LINKS</span></span>
