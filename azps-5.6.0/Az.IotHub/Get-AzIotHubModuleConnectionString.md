---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 739153aebdaf8b089c0d180643056725a85f450a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936843"
---
# <span data-ttu-id="b710e-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="b710e-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="b710e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b710e-102">SYNOPSIS</span></span>
<span data-ttu-id="b710e-103">Holen Sie sich die Verbindungszeichenfolge eines IoT-Zielgerätmoduls in einem Iot Hub.</span><span class="sxs-lookup"><span data-stu-id="b710e-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="b710e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b710e-104">SYNTAX</span></span>

### <span data-ttu-id="b710e-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b710e-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b710e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b710e-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b710e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b710e-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b710e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b710e-108">DESCRIPTION</span></span>
<span data-ttu-id="b710e-109">Listen Sie die Verbindungszeichenfolge aller Module oder eines angegebenen Moduls eines IoT-Zielgeräts auf, das in einem Azure IoT Hub enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="b710e-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="b710e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b710e-110">EXAMPLES</span></span>

### <span data-ttu-id="b710e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b710e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="b710e-112">Anzeigen aller Modulverbindungszeichenfolgen eines IoT-Zielgeräts in einem Iot Hub.</span><span class="sxs-lookup"><span data-stu-id="b710e-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="b710e-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b710e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="b710e-114">Holen Sie sich die Verbindungszeichenfolge des sekundären Moduls eines IoT-Zielgeräts in einem Iot Hub.</span><span class="sxs-lookup"><span data-stu-id="b710e-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="b710e-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b710e-115">PARAMETERS</span></span>

### <span data-ttu-id="b710e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b710e-116">-DefaultProfile</span></span>
<span data-ttu-id="b710e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b710e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b710e-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="b710e-118">-DeviceId</span></span>
<span data-ttu-id="b710e-119">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="b710e-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b710e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b710e-120">-InputObject</span></span>
<span data-ttu-id="b710e-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="b710e-121">IotHub object</span></span>

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

### <span data-ttu-id="b710e-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b710e-122">-IotHubName</span></span>
<span data-ttu-id="b710e-123">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="b710e-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b710e-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="b710e-124">-KeyType</span></span>
<span data-ttu-id="b710e-125">Richtlinienschlüsseltyp für den freigegebenen Zugriff für die Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="b710e-125">Shared access policy key type for auth.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b710e-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="b710e-126">-ModuleId</span></span>
<span data-ttu-id="b710e-127">Zielmodul-ID.</span><span class="sxs-lookup"><span data-stu-id="b710e-127">Target Module Id.</span></span>

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

### <span data-ttu-id="b710e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b710e-128">-ResourceGroupName</span></span>
<span data-ttu-id="b710e-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b710e-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b710e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b710e-130">-ResourceId</span></span>
<span data-ttu-id="b710e-131">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b710e-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b710e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b710e-132">CommonParameters</span></span>
<span data-ttu-id="b710e-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b710e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b710e-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b710e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b710e-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b710e-135">INPUTS</span></span>

### <span data-ttu-id="b710e-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b710e-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b710e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b710e-137">System.String</span></span>

## <span data-ttu-id="b710e-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b710e-138">OUTPUTS</span></span>

### <span data-ttu-id="b710e-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="b710e-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="b710e-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b710e-140">NOTES</span></span>

## <span data-ttu-id="b710e-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b710e-141">RELATED LINKS</span></span>
