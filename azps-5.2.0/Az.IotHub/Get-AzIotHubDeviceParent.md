---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 14e5bbc222bf92f95d77277c6f8d82f578efd0b3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364130"
---
# <span data-ttu-id="0e295-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="0e295-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="0e295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e295-102">SYNOPSIS</span></span>
<span data-ttu-id="0e295-103">Holen Sie sich das übergeordnete Gerät des angegebenen Geräts.</span><span class="sxs-lookup"><span data-stu-id="0e295-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="0e295-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e295-104">SYNTAX</span></span>

### <span data-ttu-id="0e295-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0e295-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e295-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0e295-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e295-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0e295-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e295-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e295-108">DESCRIPTION</span></span>
<span data-ttu-id="0e295-109">Holen Sie sich das übergeordnete Gerät des angegebenen Nicht-Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="0e295-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="0e295-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0e295-110">EXAMPLES</span></span>

### <span data-ttu-id="0e295-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0e295-111">Example 1</span></span>
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

<span data-ttu-id="0e295-112">Holen Sie sich das übergeordnete Gerät des angegebenen Nicht-Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="0e295-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="0e295-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e295-113">PARAMETERS</span></span>

### <span data-ttu-id="0e295-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e295-114">-DefaultProfile</span></span>
<span data-ttu-id="0e295-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0e295-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e295-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="0e295-116">-DeviceId</span></span>
<span data-ttu-id="0e295-117">ID eines Nicht-Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="0e295-117">Id of non-edge device.</span></span>

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

### <span data-ttu-id="0e295-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e295-118">-InputObject</span></span>
<span data-ttu-id="0e295-119">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="0e295-119">IotHub object</span></span>

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

### <span data-ttu-id="0e295-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="0e295-120">-IotHubName</span></span>
<span data-ttu-id="0e295-121">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="0e295-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0e295-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e295-122">-ResourceGroupName</span></span>
<span data-ttu-id="0e295-123">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0e295-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0e295-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e295-124">-ResourceId</span></span>
<span data-ttu-id="0e295-125">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="0e295-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0e295-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e295-126">CommonParameters</span></span>
<span data-ttu-id="0e295-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e295-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e295-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e295-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e295-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0e295-129">INPUTS</span></span>

### <span data-ttu-id="0e295-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0e295-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0e295-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0e295-131">System.String</span></span>

## <span data-ttu-id="0e295-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0e295-132">OUTPUTS</span></span>

### <span data-ttu-id="0e295-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEntfernung</span><span class="sxs-lookup"><span data-stu-id="0e295-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="0e295-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0e295-134">NOTES</span></span>

## <span data-ttu-id="0e295-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0e295-135">RELATED LINKS</span></span>
