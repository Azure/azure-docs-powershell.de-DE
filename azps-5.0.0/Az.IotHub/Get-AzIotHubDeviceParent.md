---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 14e5bbc222bf92f95d77277c6f8d82f578efd0b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177956"
---
# <span data-ttu-id="7f496-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="7f496-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="7f496-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f496-102">SYNOPSIS</span></span>
<span data-ttu-id="7f496-103">Rufen Sie das übergeordnete Gerät des angegebenen Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="7f496-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="7f496-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f496-104">SYNTAX</span></span>

### <span data-ttu-id="7f496-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7f496-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f496-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7f496-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f496-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7f496-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f496-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f496-108">DESCRIPTION</span></span>
<span data-ttu-id="7f496-109">Rufen Sie das übergeordnete Gerät des angegebenen nicht-Edge-Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="7f496-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="7f496-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f496-110">EXAMPLES</span></span>

### <span data-ttu-id="7f496-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7f496-111">Example 1</span></span>
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

<span data-ttu-id="7f496-112">Rufen Sie das übergeordnete Gerät des angegebenen nicht-Edge-Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="7f496-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="7f496-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f496-113">PARAMETERS</span></span>

### <span data-ttu-id="7f496-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f496-114">-DefaultProfile</span></span>
<span data-ttu-id="7f496-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f496-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f496-116">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="7f496-116">-DeviceId</span></span>
<span data-ttu-id="7f496-117">Die ID des nicht-Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="7f496-117">Id of non-edge device.</span></span>

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

### <span data-ttu-id="7f496-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7f496-118">-InputObject</span></span>
<span data-ttu-id="7f496-119">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="7f496-119">IotHub object</span></span>

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

### <span data-ttu-id="7f496-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7f496-120">-IotHubName</span></span>
<span data-ttu-id="7f496-121">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="7f496-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7f496-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f496-122">-ResourceGroupName</span></span>
<span data-ttu-id="7f496-123">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7f496-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7f496-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7f496-124">-ResourceId</span></span>
<span data-ttu-id="7f496-125">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="7f496-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7f496-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f496-126">CommonParameters</span></span>
<span data-ttu-id="7f496-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f496-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f496-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f496-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f496-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f496-129">INPUTS</span></span>

### <span data-ttu-id="7f496-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7f496-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7f496-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7f496-131">System.String</span></span>

## <span data-ttu-id="7f496-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f496-132">OUTPUTS</span></span>

### <span data-ttu-id="7f496-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="7f496-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="7f496-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f496-134">NOTES</span></span>

## <span data-ttu-id="7f496-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f496-135">RELATED LINKS</span></span>
