---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 1440b77d753a27b1c2a7176be5b44ef69fca2e50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292750"
---
# <span data-ttu-id="b5ba7-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="b5ba7-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="b5ba7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ba7-103">Listet alle oder eine bestimmte IoT Edge-Bereitstellung auf.</span><span class="sxs-lookup"><span data-stu-id="b5ba7-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="b5ba7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5ba7-104">SYNTAX</span></span>

### <span data-ttu-id="b5ba7-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b5ba7-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5ba7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b5ba7-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5ba7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b5ba7-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5ba7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5ba7-108">DESCRIPTION</span></span>
<span data-ttu-id="b5ba7-109">Erfahren Sie mehr über die Details einer IoT Edge-Bereitstellung oder listet IoT -Edge-Bereitstellungen in einem IoT Hub auf.</span><span class="sxs-lookup"><span data-stu-id="b5ba7-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="b5ba7-110">Weitere https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring Informationen finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="b5ba7-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="b5ba7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b5ba7-111">EXAMPLES</span></span>

### <span data-ttu-id="b5ba7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b5ba7-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="b5ba7-113">Erfahren Sie mehr über die Details einer IoT Edge-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="b5ba7-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="b5ba7-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b5ba7-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="b5ba7-115">Listen Sie alle IoT -Edge-Bereitstellungen in einem IoT Hub auf.</span><span class="sxs-lookup"><span data-stu-id="b5ba7-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="b5ba7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5ba7-116">PARAMETERS</span></span>

### <span data-ttu-id="b5ba7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ba7-117">-DefaultProfile</span></span>
<span data-ttu-id="b5ba7-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5ba7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5ba7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5ba7-119">-InputObject</span></span>
<span data-ttu-id="b5ba7-120">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="b5ba7-120">IotHub object</span></span>

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

### <span data-ttu-id="b5ba7-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b5ba7-121">-IotHubName</span></span>
<span data-ttu-id="b5ba7-122">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="b5ba7-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b5ba7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b5ba7-123">-Name</span></span>
<span data-ttu-id="b5ba7-124">Id für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="b5ba7-124">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="b5ba7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5ba7-125">-ResourceGroupName</span></span>
<span data-ttu-id="b5ba7-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b5ba7-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b5ba7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5ba7-127">-ResourceId</span></span>
<span data-ttu-id="b5ba7-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b5ba7-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b5ba7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ba7-129">CommonParameters</span></span>
<span data-ttu-id="b5ba7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5ba7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ba7-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5ba7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ba7-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b5ba7-132">INPUTS</span></span>

### <span data-ttu-id="b5ba7-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b5ba7-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b5ba7-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b5ba7-134">System.String</span></span>

## <span data-ttu-id="b5ba7-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b5ba7-135">OUTPUTS</span></span>

### <span data-ttu-id="b5ba7-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="b5ba7-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="b5ba7-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDLoyments[]</span><span class="sxs-lookup"><span data-stu-id="b5ba7-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="b5ba7-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b5ba7-138">NOTES</span></span>

## <span data-ttu-id="b5ba7-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b5ba7-139">RELATED LINKS</span></span>
