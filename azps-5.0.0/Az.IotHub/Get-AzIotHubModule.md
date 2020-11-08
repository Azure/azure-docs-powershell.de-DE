---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
ms.openlocfilehash: ca2381ecff9822bac7a4613566e2da42e79cc5b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180492"
---
# <span data-ttu-id="66a6a-101">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="66a6a-101">Get-AzIotHubModule</span></span>

## <span data-ttu-id="66a6a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66a6a-102">SYNOPSIS</span></span>
<span data-ttu-id="66a6a-103">Rufen Sie die Details eines viel Geräte Moduls oder Listen Moduls ab, das sich auf einem viel Gerät in einem viel Hub befindet.</span><span class="sxs-lookup"><span data-stu-id="66a6a-103">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="66a6a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66a6a-104">SYNTAX</span></span>

### <span data-ttu-id="66a6a-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="66a6a-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66a6a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="66a6a-106">InputObjectSet</span></span>
```
Get-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66a6a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="66a6a-107">ResourceIdSet</span></span>
```
Get-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66a6a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66a6a-108">DESCRIPTION</span></span>
<span data-ttu-id="66a6a-109">Rufen Sie die Details eines viel Geräte Moduls oder Listen Moduls ab, das sich auf einem viel Gerät in einem viel Hub befindet.</span><span class="sxs-lookup"><span data-stu-id="66a6a-109">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="66a6a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66a6a-110">EXAMPLES</span></span>

### <span data-ttu-id="66a6a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="66a6a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  :
```

<span data-ttu-id="66a6a-112">Rufen Sie die Details eines viel Geräte Moduls in einem viel Hub ab.</span><span class="sxs-lookup"><span data-stu-id="66a6a-112">Get the details of an IoT device module in an IoT Hub.</span></span>

### <span data-ttu-id="66a6a-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="66a6a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" 

Module Id Device Id Connection State Authentication Last Activity Time
--------- --------- ---------------- -------------- ------------------
module1   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
module2   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
```

<span data-ttu-id="66a6a-114">Alle Module anzeigen, die sich auf einem viel Gerät in einem viel Hub befinden.</span><span class="sxs-lookup"><span data-stu-id="66a6a-114">Show all modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="66a6a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="66a6a-115">PARAMETERS</span></span>

### <span data-ttu-id="66a6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a6a-116">-DefaultProfile</span></span>
<span data-ttu-id="66a6a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66a6a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66a6a-118">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="66a6a-118">-DeviceId</span></span>
<span data-ttu-id="66a6a-119">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="66a6a-119">Target Device Id.</span></span>

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

### <span data-ttu-id="66a6a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="66a6a-120">-InputObject</span></span>
<span data-ttu-id="66a6a-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="66a6a-121">IotHub object</span></span>

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

### <span data-ttu-id="66a6a-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="66a6a-122">-IotHubName</span></span>
<span data-ttu-id="66a6a-123">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="66a6a-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="66a6a-124">-Modul-Nr</span><span class="sxs-lookup"><span data-stu-id="66a6a-124">-ModuleId</span></span>
<span data-ttu-id="66a6a-125">Ziel Modul-ID.</span><span class="sxs-lookup"><span data-stu-id="66a6a-125">Target Module Id.</span></span>

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

### <span data-ttu-id="66a6a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a6a-126">-ResourceGroupName</span></span>
<span data-ttu-id="66a6a-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="66a6a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="66a6a-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="66a6a-128">-ResourceId</span></span>
<span data-ttu-id="66a6a-129">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="66a6a-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="66a6a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a6a-130">CommonParameters</span></span>
<span data-ttu-id="66a6a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66a6a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a6a-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66a6a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a6a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66a6a-133">INPUTS</span></span>

### <span data-ttu-id="66a6a-134">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="66a6a-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="66a6a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="66a6a-135">System.String</span></span>

## <span data-ttu-id="66a6a-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66a6a-136">OUTPUTS</span></span>

### <span data-ttu-id="66a6a-137">Microsoft. Azure. Commands. Management. IotHub. Models. PSModule</span><span class="sxs-lookup"><span data-stu-id="66a6a-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

### <span data-ttu-id="66a6a-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSModules []</span><span class="sxs-lookup"><span data-stu-id="66a6a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="66a6a-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="66a6a-139">NOTES</span></span>

## <span data-ttu-id="66a6a-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66a6a-140">RELATED LINKS</span></span>
