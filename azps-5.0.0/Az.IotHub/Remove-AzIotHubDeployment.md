---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
ms.openlocfilehash: f5463015b93c209c6cf8952c566e9656da2fba18
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175535"
---
# <span data-ttu-id="229f0-101">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="229f0-101">Remove-AzIotHubDeployment</span></span>

## <span data-ttu-id="229f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="229f0-102">SYNOPSIS</span></span>
<span data-ttu-id="229f0-103">Löschen Sie eine viel Edge-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="229f0-103">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="229f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="229f0-104">SYNTAX</span></span>

### <span data-ttu-id="229f0-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="229f0-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="229f0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="229f0-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="229f0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="229f0-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="229f0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="229f0-108">DESCRIPTION</span></span>
<span data-ttu-id="229f0-109">Weitere Informationen finden Sie unter https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring .</span><span class="sxs-lookup"><span data-stu-id="229f0-109">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="229f0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="229f0-110">EXAMPLES</span></span>

### <span data-ttu-id="229f0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="229f0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="229f0-112">Löschen Sie eine viel Edge-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="229f0-112">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="229f0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="229f0-113">PARAMETERS</span></span>

### <span data-ttu-id="229f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="229f0-114">-DefaultProfile</span></span>
<span data-ttu-id="229f0-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="229f0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="229f0-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="229f0-116">-InputObject</span></span>
<span data-ttu-id="229f0-117">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="229f0-117">IotHub object</span></span>

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

### <span data-ttu-id="229f0-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="229f0-118">-IotHubName</span></span>
<span data-ttu-id="229f0-119">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="229f0-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="229f0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="229f0-120">-Name</span></span>
<span data-ttu-id="229f0-121">Bezeichner für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="229f0-121">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="229f0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="229f0-122">-PassThru</span></span>
<span data-ttu-id="229f0-123">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="229f0-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="229f0-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="229f0-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="229f0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="229f0-125">-ResourceGroupName</span></span>
<span data-ttu-id="229f0-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="229f0-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="229f0-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="229f0-127">-ResourceId</span></span>
<span data-ttu-id="229f0-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="229f0-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="229f0-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="229f0-129">-Confirm</span></span>
<span data-ttu-id="229f0-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="229f0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="229f0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="229f0-131">-WhatIf</span></span>
<span data-ttu-id="229f0-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="229f0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="229f0-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="229f0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="229f0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="229f0-134">CommonParameters</span></span>
<span data-ttu-id="229f0-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="229f0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="229f0-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="229f0-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="229f0-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="229f0-137">INPUTS</span></span>

### <span data-ttu-id="229f0-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="229f0-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="229f0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="229f0-139">System.String</span></span>

## <span data-ttu-id="229f0-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="229f0-140">OUTPUTS</span></span>

### <span data-ttu-id="229f0-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="229f0-141">System.Boolean</span></span>

## <span data-ttu-id="229f0-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="229f0-142">NOTES</span></span>

## <span data-ttu-id="229f0-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="229f0-143">RELATED LINKS</span></span>
