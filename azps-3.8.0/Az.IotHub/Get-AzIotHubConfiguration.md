---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: 616fface9f20609c043884754e9b3904ffc83e67
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995152"
---
# <span data-ttu-id="ed623-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed623-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="ed623-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed623-102">SYNOPSIS</span></span>
<span data-ttu-id="ed623-103">Listet alle oder eine bestimmte viel automatische Geräte Verwaltungskonfiguration auf.</span><span class="sxs-lookup"><span data-stu-id="ed623-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="ed623-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed623-104">SYNTAX</span></span>

### <span data-ttu-id="ed623-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed623-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed623-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ed623-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed623-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ed623-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed623-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed623-108">DESCRIPTION</span></span>
<span data-ttu-id="ed623-109">Besorgen Sie sich die Details einer viel automatischen Device Management-Konfiguration, oder Listen Sie viel automatische Device Management-Konfigurationen in einem viel Hub auf.</span><span class="sxs-lookup"><span data-stu-id="ed623-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="ed623-110">Weitere Informationen finden Sie unter https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management .</span><span class="sxs-lookup"><span data-stu-id="ed623-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="ed623-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed623-111">EXAMPLES</span></span>

### <span data-ttu-id="ed623-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ed623-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="ed623-113">Rufen Sie die Details einer viel automatischen Geräte Verwaltungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="ed623-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="ed623-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ed623-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="ed623-115">Listen Sie viele automatische Geräte Verwaltungs Konfigurationen in einem viel Hub auf.</span><span class="sxs-lookup"><span data-stu-id="ed623-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="ed623-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed623-116">PARAMETERS</span></span>

### <span data-ttu-id="ed623-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed623-117">-DefaultProfile</span></span>
<span data-ttu-id="ed623-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed623-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed623-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ed623-119">-InputObject</span></span>
<span data-ttu-id="ed623-120">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="ed623-120">IotHub object</span></span>

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

### <span data-ttu-id="ed623-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ed623-121">-IotHubName</span></span>
<span data-ttu-id="ed623-122">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="ed623-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ed623-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ed623-123">-Name</span></span>
<span data-ttu-id="ed623-124">Bezeichner für die Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ed623-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="ed623-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed623-125">-ResourceGroupName</span></span>
<span data-ttu-id="ed623-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ed623-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ed623-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ed623-127">-ResourceId</span></span>
<span data-ttu-id="ed623-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="ed623-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ed623-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed623-129">CommonParameters</span></span>
<span data-ttu-id="ed623-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed623-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed623-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed623-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed623-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed623-132">INPUTS</span></span>

### <span data-ttu-id="ed623-133">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ed623-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ed623-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ed623-134">System.String</span></span>

## <span data-ttu-id="ed623-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed623-135">OUTPUTS</span></span>

### <span data-ttu-id="ed623-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed623-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="ed623-137">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfigurations []</span><span class="sxs-lookup"><span data-stu-id="ed623-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="ed623-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed623-138">NOTES</span></span>

## <span data-ttu-id="ed623-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed623-139">RELATED LINKS</span></span>
