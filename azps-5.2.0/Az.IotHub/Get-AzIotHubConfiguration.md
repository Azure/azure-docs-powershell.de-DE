---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: 616fface9f20609c043884754e9b3904ffc83e67
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292757"
---
# <span data-ttu-id="1c8f6-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c8f6-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="1c8f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c8f6-102">SYNOPSIS</span></span>
<span data-ttu-id="1c8f6-103">Listet die automatische Geräteverwaltungskonfiguration von IoT auf.</span><span class="sxs-lookup"><span data-stu-id="1c8f6-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="1c8f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c8f6-104">SYNTAX</span></span>

### <span data-ttu-id="1c8f6-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1c8f6-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c8f6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1c8f6-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c8f6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1c8f6-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c8f6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c8f6-108">DESCRIPTION</span></span>
<span data-ttu-id="1c8f6-109">Erfahren Sie mehr über die Details einer automatischen Geräteverwaltungskonfiguration von IoT, oder listen Sie die Konfigurationen der automatischen Geräteverwaltung von IoT in einem IoT Hub auf.</span><span class="sxs-lookup"><span data-stu-id="1c8f6-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="1c8f6-110">Weitere https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management Informationen finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="1c8f6-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="1c8f6-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1c8f6-111">EXAMPLES</span></span>

### <span data-ttu-id="1c8f6-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1c8f6-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="1c8f6-113">Erfahren Sie mehr über die Details einer automatischen Geräteverwaltungskonfiguration von IoT.</span><span class="sxs-lookup"><span data-stu-id="1c8f6-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="1c8f6-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1c8f6-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="1c8f6-115">Auflisten der automatischen Geräteverwaltungskonfigurationen von IoT in einem IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="1c8f6-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="1c8f6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c8f6-116">PARAMETERS</span></span>

### <span data-ttu-id="1c8f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c8f6-117">-DefaultProfile</span></span>
<span data-ttu-id="1c8f6-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c8f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c8f6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c8f6-119">-InputObject</span></span>
<span data-ttu-id="1c8f6-120">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="1c8f6-120">IotHub object</span></span>

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

### <span data-ttu-id="1c8f6-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1c8f6-121">-IotHubName</span></span>
<span data-ttu-id="1c8f6-122">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="1c8f6-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1c8f6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1c8f6-123">-Name</span></span>
<span data-ttu-id="1c8f6-124">Id für die Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1c8f6-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="1c8f6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c8f6-125">-ResourceGroupName</span></span>
<span data-ttu-id="1c8f6-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="1c8f6-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1c8f6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c8f6-127">-ResourceId</span></span>
<span data-ttu-id="1c8f6-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="1c8f6-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1c8f6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c8f6-129">CommonParameters</span></span>
<span data-ttu-id="1c8f6-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c8f6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c8f6-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c8f6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c8f6-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1c8f6-132">INPUTS</span></span>

### <span data-ttu-id="1c8f6-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1c8f6-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1c8f6-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1c8f6-134">System.String</span></span>

## <span data-ttu-id="1c8f6-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1c8f6-135">OUTPUTS</span></span>

### <span data-ttu-id="1c8f6-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c8f6-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="1c8f6-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span><span class="sxs-lookup"><span data-stu-id="1c8f6-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="1c8f6-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1c8f6-138">NOTES</span></span>

## <span data-ttu-id="1c8f6-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1c8f6-139">RELATED LINKS</span></span>
