---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 06eb84ea854e9c0262f6f3e00e3e13e90f630baa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936907"
---
# <span data-ttu-id="25e7f-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="25e7f-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="25e7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25e7f-102">SYNOPSIS</span></span>
<span data-ttu-id="25e7f-103">Holen Sie sich das übergeordnete Gerät des angegebenen Geräts.</span><span class="sxs-lookup"><span data-stu-id="25e7f-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="25e7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25e7f-104">SYNTAX</span></span>

### <span data-ttu-id="25e7f-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="25e7f-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25e7f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="25e7f-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25e7f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="25e7f-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25e7f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25e7f-108">DESCRIPTION</span></span>
<span data-ttu-id="25e7f-109">Holen Sie sich das übergeordnete Gerät des angegebenen Nicht-Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="25e7f-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="25e7f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="25e7f-110">EXAMPLES</span></span>

### <span data-ttu-id="25e7f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="25e7f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myParentDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Enabled
StatusReason               : 
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : True
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

<span data-ttu-id="25e7f-112">Holen Sie sich das übergeordnete Gerät des angegebenen Nicht-Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="25e7f-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="25e7f-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="25e7f-113">PARAMETERS</span></span>

### <span data-ttu-id="25e7f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e7f-114">-DefaultProfile</span></span>
<span data-ttu-id="25e7f-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25e7f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25e7f-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="25e7f-116">-DeviceId</span></span>
<span data-ttu-id="25e7f-117">ID eines Nicht-Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="25e7f-117">Id of non-edge device.</span></span>

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

### <span data-ttu-id="25e7f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25e7f-118">-InputObject</span></span>
<span data-ttu-id="25e7f-119">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="25e7f-119">IotHub object</span></span>

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

### <span data-ttu-id="25e7f-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="25e7f-120">-IotHubName</span></span>
<span data-ttu-id="25e7f-121">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="25e7f-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="25e7f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25e7f-122">-ResourceGroupName</span></span>
<span data-ttu-id="25e7f-123">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="25e7f-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="25e7f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25e7f-124">-ResourceId</span></span>
<span data-ttu-id="25e7f-125">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="25e7f-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="25e7f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e7f-126">CommonParameters</span></span>
<span data-ttu-id="25e7f-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25e7f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e7f-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25e7f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e7f-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="25e7f-129">INPUTS</span></span>

### <span data-ttu-id="25e7f-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="25e7f-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="25e7f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="25e7f-131">System.String</span></span>

## <span data-ttu-id="25e7f-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="25e7f-132">OUTPUTS</span></span>

### <span data-ttu-id="25e7f-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEvice</span><span class="sxs-lookup"><span data-stu-id="25e7f-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="25e7f-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="25e7f-134">NOTES</span></span>

## <span data-ttu-id="25e7f-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="25e7f-135">RELATED LINKS</span></span>
