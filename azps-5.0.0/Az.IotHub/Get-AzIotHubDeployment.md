---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 1440b77d753a27b1c2a7176be5b44ef69fca2e50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177962"
---
# <span data-ttu-id="6fefc-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="6fefc-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="6fefc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6fefc-102">SYNOPSIS</span></span>
<span data-ttu-id="6fefc-103">Listet alle oder eine bestimmte viel Edge-Bereitstellung auf.</span><span class="sxs-lookup"><span data-stu-id="6fefc-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="6fefc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fefc-104">SYNTAX</span></span>

### <span data-ttu-id="6fefc-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6fefc-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fefc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6fefc-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6fefc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6fefc-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6fefc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6fefc-108">DESCRIPTION</span></span>
<span data-ttu-id="6fefc-109">Holen Sie sich die Details einer viel Edge-Bereitstellung, oder führen Sie viel Edge-Bereitstellungen in einem viel Hub aus.</span><span class="sxs-lookup"><span data-stu-id="6fefc-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="6fefc-110">Weitere Informationen finden Sie unter https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring .</span><span class="sxs-lookup"><span data-stu-id="6fefc-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="6fefc-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6fefc-111">EXAMPLES</span></span>

### <span data-ttu-id="6fefc-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6fefc-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="6fefc-113">Abrufen der Details einer viel Edge-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="6fefc-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="6fefc-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6fefc-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="6fefc-115">Auflisten aller viel Edge-Bereitstellungen in einem viel Hub.</span><span class="sxs-lookup"><span data-stu-id="6fefc-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="6fefc-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fefc-116">PARAMETERS</span></span>

### <span data-ttu-id="6fefc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fefc-117">-DefaultProfile</span></span>
<span data-ttu-id="6fefc-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6fefc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fefc-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6fefc-119">-InputObject</span></span>
<span data-ttu-id="6fefc-120">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="6fefc-120">IotHub object</span></span>

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

### <span data-ttu-id="6fefc-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6fefc-121">-IotHubName</span></span>
<span data-ttu-id="6fefc-122">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="6fefc-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6fefc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6fefc-123">-Name</span></span>
<span data-ttu-id="6fefc-124">Bezeichner für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="6fefc-124">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="6fefc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fefc-125">-ResourceGroupName</span></span>
<span data-ttu-id="6fefc-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6fefc-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6fefc-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6fefc-127">-ResourceId</span></span>
<span data-ttu-id="6fefc-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="6fefc-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6fefc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fefc-129">CommonParameters</span></span>
<span data-ttu-id="6fefc-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fefc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fefc-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fefc-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fefc-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6fefc-132">INPUTS</span></span>

### <span data-ttu-id="6fefc-133">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6fefc-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6fefc-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6fefc-134">System.String</span></span>

## <span data-ttu-id="6fefc-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6fefc-135">OUTPUTS</span></span>

### <span data-ttu-id="6fefc-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="6fefc-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="6fefc-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments []</span><span class="sxs-lookup"><span data-stu-id="6fefc-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="6fefc-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="6fefc-138">NOTES</span></span>

## <span data-ttu-id="6fefc-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6fefc-139">RELATED LINKS</span></span>
